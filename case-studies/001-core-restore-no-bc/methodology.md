# Methodology — Case Study 001

## Data source

All data was pulled from my personal WHOOP 4.0 account on **2026-04-23** using the [whoop-ai-mcp](https://github.com/shashankswe2020-ux/whoop-mcp) open-source MCP server + the `scripts/pull-whoop.mjs` wrapper in this repository. The 45-day window captures 27 days of pre-detox baseline, the 14 days of Core Restore (with infrared sauna sessions throughout), and the immediate post-detox clean window.

Blood-work data comes from two Quest Diagnostics panels ordered through Parsley Health (January 20, 2026 baseline + April 23, 2026 post-cycle). See [`biomarker-results.md`](biomarker-results.md) for the full directional summary.

## ⚠️ Concurrent medications and hormonal status

**During the entire 45-day case-study window (and during the June 2025 7-day cycle), the author was not using:**

- ❌ Hormonal contraception (combined OCP, progestin-only methods, hormonal IUDs, etc.)
- ❌ Hormonal endometriosis suppression (GnRH agonists, danazol, progestins, aromatase inhibitors)
- ❌ Hormone replacement therapy

**Natural menstrual cycles were ongoing throughout.** This was a deliberate root-cause exploration of how the body responds to liver-clearance support without a hormonally suppressed baseline.

**Cycle phases were confirmed two ways:**
1. **Hormone testing** — progesterone 19.1 ng/mL (Jan 20, 2026, fasted morning draw) anchors that timepoint to mid-luteal phase
2. **WHOOP physiological signature** — sharp HRV + recovery drop paired with elevated resting HR and skin-temperature peak appears on January 24, 2026 and April 22–23, 2026, consistent with ~28-day cycle interval

**Cross-mapping to the protocol window:**

| Phase | Date range | Estimated cycle days | Cycle phase |
|---|---|---|---|
| Pre-detox baseline | Mar 9 → Apr 4 | Full cycle cross-section | Mixed |
| 14-day Core Restore | Apr 5 → Apr 18 | ~cycle day 14 → 27 | Ovulation + full luteal |
| Post-detox / Lab 2 draw | Apr 19 → Apr 23 | ~cycle day 28 → menses transition | Late luteal / pre-menses |

**Why this is methodologically important:** baseline HRV is typically *lower* in luteal phase than follicular. The 14-day cycle's HRV improvement happened during the cycle window where HRV would naturally be suppressed — meaning the protocol effect is, if anything, **understated** relative to a cycle-phase-controlled comparison.

See [`research/birth-control-context.md`](../../research/birth-control-context.md) for full scientific rationale of why this choice matters for data interpretation, and why the protocol may behave differently for readers on hormonal contraception.

### Tools used

- **WHOOP 4.0 strap** (worn 24/7)
- **WHOOP API v2** via OAuth2 + PKCE
- **[whoop-ai-mcp](https://github.com/shashankswe2020-ux/whoop-mcp)** as the auth + API client wrapper
- **Node 20+** to run the analysis scripts

### Endpoints used

- `/v2/recovery` — daily recovery score, HRV (rmssd), resting heart rate, SpO2, skin temperature
- `/v2/activity/sleep` — sleep stage breakdown, duration, performance, respiratory rate
- `/v2/activity/workout` — individual workouts with strain and HR zones
- `/v2/cycle` — daily physiological cycle with aggregate strain

## Phase definitions

See [`phases.json`](phases.json). Phases are date ranges I assigned based on my own calendar:

| Phase | Range | Days | Definition |
|---|---|---|---|
| Pre-detox baseline | 2026-03-09 → 2026-04-04 | 27 | Normal eating, normal training, normal life |
| Core Restore | 2026-04-05 → 2026-04-18 | 14 | On-protocol: elimination diet + supplements + 2 shakes/day + infrared sauna sessions throughout |
| Post-detox clean | 2026-04-19 | 1 | Immediate rest day following the 14-day cycle |

## Statistical approach

**I did not run significance tests.** The sample size is too small, phases are unequal length, and the variables are highly autocorrelated day-to-day. Running a t-test would be dressing up a case study as a trial. Instead, I report:

- **Medians** per phase (less sensitive to single bad nights than means)
- **Percent change** for HRV specifically (log-distributed, percent is more interpretable than absolute ms)
- **Direction and magnitude**, framed as observations, not conclusions

Confounders are listed explicitly in the main case study post.

## What I didn't do (on purpose)

- **Withhold data.** All 45 days of daily summaries are in [`data/daily-summary.csv`](data/daily-summary.csv). If you want to run your own analysis, the CSV is the source.
- **Cherry-pick windows.** The phase boundaries are my calendar dates, not the dates that make the effect look biggest.
- **Subtract training load.** I considered normalizing HRV against cycle strain, but the strain variation during the window is within a small enough range that the correction wouldn't change the direction of the effect. If you're a more elite athlete reading this and want the strain-adjusted analysis, the raw data is public — please DIY and publish your version.

## Data pipeline reproducibility

```bash
# 1. Pull raw data (outputs ~/Documents/Dev Projects/diet-signal/whoop-raw.json by default)
node scripts/pull-whoop.mjs --days 45 --out /tmp/whoop-raw.json

# 2. Export anonymized daily summary
node scripts/export-csv.mjs \
  --in /tmp/whoop-raw.json \
  --out case-studies/001-core-restore/data/daily-summary.csv

# 3. Generate phase comparison table + daily detail
node scripts/analyze-phases.mjs \
  --data /tmp/whoop-raw.json \
  --config case-studies/001-core-restore/phases.json \
  --detail 14
```

The `/tmp/whoop-raw.json` file contains `user_id` and email — it **must not** be committed. Only the anonymized CSV ships in this repo.

## What would make future case studies better

- **Longer baseline windows** (60+ days) to reduce sensitivity to any single outlier
- **Training-load matching** between phases — if strain spikes during a test phase, isolate that
- **Menstrual cycle phase logging** so HRV is compared across similar cycle stages
- **Concurrent symptom diary** (already addressed via `templates/reintro-tracker.md`)
- **Bloodwork bookends** — Parsley runs labs periodically; pairing liver enzymes and inflammatory markers (hs-CRP, ferritin, homocysteine) with WHOOP data before/after would add a mechanistic layer
