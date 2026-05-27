# Birth Control Context — Why the No-Hormonal-Contraception Choice Matters

> 🚺 **All case studies and protocols in this repository were developed without hormonal contraception, hormonal endometriosis suppression, or HRT.** This was a deliberate root-cause choice. This document explains the scientific framing — why it matters for data interpretation, what it does NOT imply about birth control as a clinical tool, and how the protocol applies if you ARE on hormonal medication.

---

## The choice and why

### What "no hormonal contraception or suppression" means

During every case study and protocol-development period in this repo, the author was NOT using:

- ❌ Combined oral contraceptives (estrogen + progestin pills)
- ❌ Progestin-only pills, implants, or injections
- ❌ Hormonal IUDs (levonorgestrel-releasing)
- ❌ GnRH agonists (Lupron, Orilissa/elagolix, etc.)
- ❌ Aromatase inhibitors (letrozole, anastrozole) used off-label for endo
- ❌ Danazol
- ❌ Other hormonal endometriosis suppression
- ❌ Hormone replacement therapy

**Natural menstrual cycles were ongoing.** Cycle phases were confirmed via hormone testing (progesterone at known timepoints) and WHOOP physiological signatures (skin temperature, HRV, resting HR patterns).

### Why root-cause investigation often requires this baseline

Hormonal contraception works in part by **suppressing the natural HPO (hypothalamic-pituitary-ovarian) axis** — preventing ovulation, suppressing endogenous estrogen and progesterone production, and creating an artificial hormonal state. This is *clinically valuable* for many conditions including endometriosis-related pain. But it also makes it difficult to:

1. **See what your body does on its own.** Suppressed cycles don't reveal what your natural physiology looks like.
2. **Track cycle-phase effects in wearable data.** On most hormonal contraception, you don't have a natural cycle to track.
3. **Test interventions on the natural hormonal axis.** If you're measuring whether a protocol improves estrogen clearance, but you're also exogenously controlling estrogen levels, the data is confounded.
4. **Identify cycle-dependent food sensitivities or symptoms.** Many endo symptoms cluster around specific cycle phases. Hormonal contraception flattens that signal.

The author's case studies are explicitly an attempt to characterize **root-cause physiology** — what the body does, what biomarkers shift, what wearable signals appear — on a natural-cycle baseline.

### What this is NOT

This is not a recommendation against birth control. Hormonal contraception is:

✅ **Effective** for pregnancy prevention
✅ **Often clinically beneficial** for endometriosis-related pain (multiple RCT-level evidence)
✅ **Often preferred over surgery** for managing symptoms
✅ **Appropriate** for many patients given their goals, severity, and life context
✅ **Compatible with most of this protocol** (with some supplement considerations — see below)

The author's choice to not use hormonal contraception reflects a personal research-oriented choice, not a clinical recommendation. **Do not stop your hormonal medication without medical supervision.** It is dangerous to make that decision based on what one person did in their case study.

---

## How birth control affects the physiological signals in this repo

If you're on hormonal contraception and considering this protocol, here's what differs:

### Cycle-phase data does not apply directly

Most of the case studies use cycle phase (follicular, ovulation, luteal, menses) as a key analytical variable. On hormonal contraception:

- **Combined OCPs** (estrogen + progestin) typically suppress ovulation entirely; you have a "withdrawal bleed" during the placebo week, not a true period
- **Progestin-only methods** create variable patterns — sometimes ovulation, sometimes not; cycles may be irregular or absent
- **Hormonal IUDs** typically continue to allow some ovulation but greatly thin the endometrium
- **GnRH agonists** create a near-menopausal state with no cycle

The cycle-phase analysis shown in [Case Study 001](../case-studies/001-core-restore-no-bc/) cannot be directly applied if you don't have a natural cycle. WHOOP and Garmin will not show the same patterns.

### Hormonal contraception affects liver function

The liver metabolizes synthetic hormones in birth control via the **same Phase 1 and Phase 2 pathways** that clear endogenous estrogens. This means:

1. **Your liver is working harder on baseline** — processing synthetic estrogen/progestin in addition to your residual endogenous hormones
2. **The protocol may still help** — supporting Phase 2 capacity benefits both endogenous and synthetic hormone clearance
3. **Some markers may behave differently** — e.g., ferritin can be lower on combined OCPs (lighter or no periods); CRP can be slightly elevated on some BC formulations

This is well-documented in the literature; see Sitruk-Ware & Nath 2013 and similar pharmacological reviews on hormonal contraception and hepatic metabolism.

### HRV and recovery patterns differ

Some research suggests hormonal contraception alters HRV patterns compared to natural cycles:

- The cycle-phase HRV variation (follicular ⬆, luteal ⬇) is dampened or absent on combined OCPs
- Resting heart rate may run slightly higher on combined OCPs (likely related to slightly altered autonomic tone)
- Sleep architecture may differ (synthetic progestin has different effects than endogenous progesterone)

**Implication:** if you're on combined OCPs and you do this protocol, expect the wearable signal to be **less dramatic** than what the case study showed, because (a) your hormones aren't naturally cycling, so the protocol's effect doesn't have a cycle-phase amplifier, and (b) the synthetic hormones are creating their own baseline that the protocol can shift only partially.

---

## Supplement interactions with hormonal medication

> ⚠️ **Always discuss with your prescribing physician before starting any supplement while on hormonal medication.**

### Supplements that can theoretically REDUCE hormonal contraception levels

These work via the CYP450 enzyme system (especially CYP3A4) or by altering enterohepatic recirculation of conjugated steroids:

| Supplement | Mechanism | Practical guidance |
|---|---|---|
| **St. John's Wort** | Strong CYP3A4 inducer | ⛔ **Not in this protocol due to extensive interactions.** Definitively reduces oral contraceptive levels. |
| **DIM (diindolylmethane)** | Modulates CYP1A1/1A2/3A4 | ⚠️ Theoretically reduces synthetic estrogen levels. **Practitioner-only.** Some sources recommend pausing combined OCPs or using backup contraception. |
| **Calcium-D-glucarate** | Inhibits β-glucuronidase | ⚠️ Theoretically lowers reabsorption of conjugated synthetic estrogens. **Practitioner-required.** |
| **Sulforaphane extracts** (concentrated) | Nrf2 inducer; can affect CYP activity | ⚠️ Cruciferous **foods** are fine. Concentrated extracts: practitioner discussion. |
| **High-dose milk thistle (silymarin)** | Modulates CYP3A4 | ⚠️ Practitioner-confirmed dose |

### Supplements typically fine on hormonal contraception

| Supplement | Notes |
|---|---|
| **Vitamin D₃ + K₂** | Generally safe; useful regardless of BC status |
| **Omega-3 (EPA/DHA)** | Generally safe; supports anti-inflammatory baseline |
| **Magnesium glycinate** | Generally safe; combined OCPs can lower magnesium status — supplementation often beneficial |
| **B-complex with methylated forms** | Generally safe; **combined OCPs are known to deplete B6 and folate** — supplementation often clinically recommended for BC users |
| **Probiotics** | Generally safe |
| **NAC** | Generally safe |
| **Curcumin (food form)** | Food-form turmeric in cooking is fine; high-dose concentrated extracts at practitioner discretion |

### Bonus context — B6, folate, and combined OCPs

Combined oral contraceptives have been shown to **deplete several nutrients**, including:
- Vitamin B6
- Folate (especially methylated forms)
- Vitamin B12 (variable findings)
- Magnesium
- Zinc
- Coenzyme Q10
- Vitamin E

This is documented in the broader literature on hormonal contraception and micronutrient status. **The methylation-cycle support pillar of this protocol (B12, B6, folate, magnesium) is actually MORE clinically indicated for people on combined OCPs**, not less — because the BC depletes these very nutrients.

If you're on combined OCPs, expect:
- The methylation-cycle pillar of the protocol to help significantly
- DIM and calcium-D-glucarate to be the most contraindicated pieces — discuss with prescriber
- The food protocol, fiber, sauna, sleep, and movement pillars to remain fully applicable

---

## Decision framework if you're on BC

### Stay on BC + do most of the protocol (recommended for most people)

The protocol elements you can almost certainly do without prescriber consultation:

✅ Elimination diet (no gluten/dairy/soy/corn/eggs/sugar/alcohol/caffeine for 30 days)
✅ Environmental swaps (glass containers, clean personal care, filtered water)
✅ Cruciferous vegetables daily
✅ Fiber to 30+ g/day
✅ Sleep optimization (8h)
✅ Sauna (gradual ramp)
✅ Vitamin D, omega-3, magnesium glycinate, methylated B-complex
✅ Movement, stress management, breath work

The pieces requiring prescriber discussion:
⚠️ NAC, milk thistle, curcumin (extracts), sulforaphane (extracts)
⛔ DIM, calcium-D-glucarate (discuss explicitly)
⛔ St. John's Wort (never)

### Stop BC + do the full protocol (only if your clinical situation supports it)

This is a meaningful clinical decision. Only consider this if:
- You have a clinical reason to be off BC (planning pregnancy, side effects, exploring root-cause)
- You have a prescriber's support and a non-hormonal contraception backup plan if needed
- You have time to observe your natural cycle to gather data

**Do not stop BC purely because of this protocol.** The protocol works on either baseline; the data interpretation just differs.

### Use the protocol post-discontinuation

Some people use hormonal contraception for years, then discontinue, and find that their endo symptoms return. The protocol is particularly relevant in the post-discontinuation window — to support the body as natural cycles resume and to reduce the inflammatory + hormonal drive that may have been masked by BC.

---

## What does this mean for the case study data interpretation?

When reading [Case Study 001](../case-studies/001-core-restore-no-bc/):

- The cycle-phase analysis (luteal phase HRV suppression) reflects natural endogenous cycling
- The biomarker shifts (homocysteine ⬇, B12 ⬆, vitamin D ⬆) are likely applicable to anyone whose methylation cycle is suboptimal, regardless of BC status
- The HRV improvements may be more muted on hormonal contraception (because synthetic hormones already flatten the natural cycle variation)
- The supplement protocol may need modification (DIM, calcium-D-glucarate, sulforaphane extracts) for BC users

In short: **the mechanism stories generalize; the specific magnitudes may not.**

---

## References

- Sitruk-Ware R, Nath A. "Characteristics and metabolic effects of estrogen and progestins contained in oral contraceptive pills." *Best Pract Res Clin Endocrinol Metab.* 2013;27(1):13-24. PMID: 23384743
- Palmery M, Saraceno A, Vaiarelli A, Carlomagno G. "Oral contraceptives and changes in nutritional requirements." *Eur Rev Med Pharmacol Sci.* 2013;17(13):1804-13. PMID: 23852908
- Wegienka G, Baird DD. "A comparison of recalled date of last menstrual period with prospectively recorded dates." *J Womens Health.* 2005;14(3):248-52. PMID: 15857271 (For the broader context of cycle-tracking accuracy)
- The full bibliography on hormonal contraception × liver pharmacology + nutrient depletion is extensive; the citations above are anchor points. **For your specific clinical questions, consult your prescriber.**

---

## Bottom line

| Question | Answer |
|---|---|
| Does this protocol work if I'm on BC? | **Most of it, yes.** Discuss specific supplements with your prescriber. |
| Will I see the same wearable patterns the case study shows? | **No.** Cycle-phase signals will be flatter on hormonal contraception. |
| Should I stop my BC to do this protocol? | **No.** Not without medical supervision and a specific clinical reason. |
| If I am stopping BC for clinical reasons anyway, does this protocol help? | **Yes, particularly during the transition window.** Talk to your practitioner. |
| Does the protocol's mechanism (estrogen clearance) still apply on BC? | **Yes** — the liver is processing synthetic hormones via the same pathways. Supporting Phase 2 is beneficial. |
| Does this position the author as anti-BC? | **No.** It positions her as choosing root-cause investigation for her own case studies. BC is a valid clinical tool. |
