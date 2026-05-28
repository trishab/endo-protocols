# endo-protocols

> **Evidence-based, replicable protocols and rigorous n=1 case studies for living with endometriosis and adenomyosis — built on a root-cause framework: understanding *why* the inflammation, hormonal dysregulation, and pain persist, and what protocols address the underlying mechanism rather than only the symptoms.**

Part of the [**EndEndo.io**](https://endendo.io) ecosystem.

---

## ⚠️ Important context: no hormonal contraception or suppression

**All case studies and protocols in this repository were developed without hormonal contraception, hormonal endometriosis suppression, or HRT.**

This was a deliberate choice to understand root-cause physiology — what the body does on its own — rather than measure interventions on top of a hormonally suppressed baseline. Natural menstrual cycles were ongoing throughout. Cycle phases were confirmed via hormone testing and WHOOP physiological signatures (skin temperature, HRV, resting HR patterns).

**This is not a recommendation against birth control.** Hormonal contraception is a valid tool many people with endo use successfully, and this protocol is generally still compatible with it. But it's critical context for interpreting the data here: cycle phases, hormonal markers, and protocol effects shown in this repo reflect natural endogenous hormonal cycles. If you are on hormonal contraception or hormonal suppression, your physiological signatures will differ — and a few supplements (notably DIM, calcium-D-glucarate, sulforaphane extracts) can theoretically interact with synthetic hormones via the CYP450 system. **Talk to your prescriber before starting any protocol if you are on hormonal medication.** See [`research/birth-control-context.md`](research/birth-control-context.md) for the detailed scientific framing.

---

## 🚪 Three doors — pick your entry point

This repo is built for three audiences and three depths of engagement. Pick whichever fits where you are.

### 🩺 Door 1: **Read the case study** *(start here if you want the story + the data)*

→ [**`case-studies/001-core-restore-no-bc/`**](case-studies/001-core-restore-no-bc/) — the lead case study. One person with endometriosis, two cycles of the same liver-cleanse protocol (a 7-day cycle in June 2025 and a 14-day cycle in April 2026), full WHOOP + Garmin + bloodwork data, honest caveats, peer-reviewed mechanism citations.

### 🛠️ Door 2: **Try the protocol** *(start here if you want to do what worked)*

→ [**`protocols/01-estrogen-clearance/`**](protocols/01-estrogen-clearance/) — the 30-day estrogen clearance protocol, derived from the case study. Includes three audience-specific entry points:

- 🔪 [**For people preparing for surgery**](protocols/01-estrogen-clearance/for-pre-surgery.md) — lower inflammatory baseline going in, recover faster
- 🩹 [**For people recovering from surgery**](protocols/01-estrogen-clearance/for-post-surgery.md) — reduce recurrence risk during the healing window
- 🤔 [**For people on the fence about surgery**](protocols/01-estrogen-clearance/for-surgery-hesitant.md) — try the root-cause approach for 90 days and re-evaluate with data in hand

### 🔬 Door 3: **Read the research** *(start here if you want the mechanism)*

→ [**`research/`**](research/) — consolidated peer-reviewed literature on estrogen metabolism, methylation cycles, the endometriosis-biomarker connection, vaginal microbiome research, sauna therapy, and the scientific framing of the no-BC choice. Every claim in every case study and protocol traces back to a citation here.

---

## 🧭 The root-cause framework — a dual-axis thesis

Endometriosis and adenomyosis are estrogen-driven inflammatory conditions.[^1] The mainstream treatment paradigm — hormonal suppression and surgical excision — addresses symptoms and visible lesions, but does not always address the underlying biochemistry that drives lesion formation and recurrence: **impaired estrogen clearance, systemic inflammation, and gut/vaginal microbial dysbiosis.**

The integrative thesis of this repository — explained in detail in [`case-studies/001-core-restore-no-bc/microbiome-estrogen-axis.md`](case-studies/001-core-restore-no-bc/microbiome-estrogen-axis.md) — is that **estrogen clearance in endometriosis is a shared liver-and-microbiome problem**, not just a liver problem. The liver does Phase 2 conjugation work to clear estrogens. Gut and vaginal bacteria with β-glucuronidase and sulfatase activity simultaneously deconjugate and reactivate cleared estrogens, returning them to circulation. **A Phase 2 hepatic intervention without a parallel microbiome-side intervention addresses only half the mechanism.** This dual-axis framing structures both the case study and the citizen-science Study 001.

This repository explores those underlying drivers:

| Root-cause driver | What contributes | What the protocol targets |
|---|---|---|
| **Impaired liver Phase 2 estrogen clearance** | Methylation cycle dysfunction (elevated homocysteine), depleted glutathione, environmental toxicant load | Methylation-cycle nutrients (B12, B6, folate, magnesium), Phase 2 enzyme inducers (sulforaphane, DIM, milk thistle), reduced inbound toxicant load |
| **Systemic inflammation** | Inflammatory food triggers, sedentary lifestyle, sleep debt, alcohol | Elimination diet, anti-inflammatory foods, sauna therapy, sleep optimization |
| **Reactive estrogen metabolites (4-OH)** | COMT enzyme bottleneck, low SAMe | Methylation cycle restoration, COMT cofactor support |
| **Vaginal/gut microbial dysbiosis** | β-glucuronidase-producing bacteria, low *L. crispatus* dominance, BV-associated species | Fiber intake, fermented foods, calcium-D-glucarate, vaginal microbiome tracking (Evvy) |
| **Chronic stress / cortisol dysregulation** | Steals progesterone precursors, worsens estrogen dominance | Sleep, breathing protocols, restorative movement |
| **Reduced autonomic capacity** | Documented reduced HRV in endo patients[^4] | Heat therapy, breath work, recovery-prioritized training |

---

## 🩺 Who this is for

- **People with endometriosis or adenomyosis** seeking evidence-based, non-hormonal approaches to root-cause inflammation and estrogen clearance
- **People preparing for, recovering from, or considering surgery** for endo/adeno — including those trying to delay or avoid it
- **Clinicians and functional medicine practitioners** looking for structured case reports + protocols to share with patients
- **Quantified-self readers** curious about whether wearables can detect protocol effects on inflammation
- **Researchers** interested in transparent n=1 pilot data to generate hypotheses

---

## 📂 Repo structure

```
endo-protocols/
├── README.md                          ← you are here
├── disclosures.md                     ← affiliates · medical disclaimers · BC note
│
├── case-studies/                      ← n=1 personal case reports (the story + data)
│   └── 001-core-restore-no-bc/        ← the lead case study
│
├── protocols/                         ← actionable, replicable protocols (the how)
│   └── 01-estrogen-clearance/         ← 30-day root-cause protocol + 3 surgery paths
│
├── studies/                           ← multi-subject citizen science
│   └── 001-evvy-surgery-recovery/     ← vaginal microbiome × surgical recovery
│
├── research/                          ← consolidated peer-reviewed bibliography (the why)
│
├── templates/                         ← reusable trackers
└── scripts/                           ← WHOOP/Garmin data pipeline
```

---

## 🛠️ Using the scripts

```bash
# Install (Node 20+)
npm install

# --- WHOOP ---
node scripts/pull-whoop.mjs --days 45 --out /tmp/whoop-raw.json
node scripts/export-csv.mjs --in /tmp/whoop-raw.json --out case-studies/001-core-restore-no-bc/data/daily-summary.csv
node scripts/analyze-phases.mjs --data /tmp/whoop-raw.json --config case-studies/001-core-restore-no-bc/phases.json

# --- Garmin longitudinal ---
node scripts/parse-garmin-export.mjs --export-dir ~/Downloads/garmin-export --out /tmp/garmin-daily.csv
node scripts/merge-longitudinal.mjs --whoop case-studies/001-core-restore-no-bc/data/daily-summary.csv --garmin /tmp/garmin-daily.csv --out case-studies/001-core-restore-no-bc/data/longitudinal-summary.csv
```

---

## 📜 License

- **Code (`scripts/`)**: MIT
- **Content (`case-studies/`, `protocols/`, `research/`, `templates/`, `*.md`)**: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) — share and adapt with attribution

## ⚠️ Not medical advice

Everything here is n=1 personal tracking + research aggregation by the author. Nothing here is a recommendation for you. If you have endometriosis, adenomyosis, or any chronic condition, decisions about diet, supplements, detoxification protocols, surgery, or hormonal medication should be made with qualified practitioners who know your history. See [`disclosures.md`](disclosures.md) for affiliate relationships and the full medical disclaimer.

---

## References

[^1]: Zondervan KT, Becker CM, Missmer SA. "Endometriosis." *N Engl J Med.* 2020;382(13):1244-1256. [PMID: 32212520](https://pubmed.ncbi.nlm.nih.gov/32212520/)
[^4]: Kulshrestha R, Pandey A, Jain A, et al. "Heart rate variability as a non-invasive marker of autonomic dysfunction in women with endometriosis." *Indian J Physiol Pharmacol.* 2022;66(4):263-270.
