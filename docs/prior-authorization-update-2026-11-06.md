# Prior authorization deck: update log (2026-11-06)

Handoff notes for anyone (including Codex) continuing work on `prior-authorization.html`.

**Status:** This is still Wendyl's **concept presentation to teammates for consideration**. It is **not** the approved hackathon concept. Keep wording evaluative ("could", "hypothesis", "team question"), not committed ("we will", "our solution").

Changes were made by Claude Code after reviewing an external Gemini audit of the deck. They are **not committed or pushed**. The live GitHub Pages site still shows the 16-slide version.

## What changed (16 → 18 slides)

| Slide | Change | Why |
|---|---|---|
| 4 | 61% card reworded: "were concerned that AI increases or will increase PA denial rates. The AMA describes this as concern about health plans' use of AI." Operational-meaning note adds a pre-check hypothesis. Footer cites the AMA press release. | The old wording was ambiguous about whose AI. The survey PDF says only "augmented intelligence (AI)"; the [AMA press release](https://www.ama-assn.org/press-center/ama-press-releases/physicians-concerned-ai-increases-prior-authorization-denials) says "health plans' use of AI." Both are now reflected. |
| 9 | Added a one-line definition of **payer** under the heading. | A teammate-level reader may not know that "payer" means the insurer or health plan, not the patient. |
| 14 (new) | **Existing tools and policy context**: provider-side vendors (Silna, Flexbone, plus Waystar, Optum, Notable, AKASA from directories), CMS-0057-F scope, a possible angle (traceable reasoning), and a team question. | The deck had no competitor or regulatory slide. The same function is already sold, so the team needs to weigh redundancy. |
| 15 (new) | **Working theory on cost, adoption, and compatibility**: Wendyl's theory for each, a challenge, and a test. | Wendyl's hypothesis for why the problem persists despite existing tools. Framed as hypotheses to test in interviews. |
| All | Footers renumbered to `/ 18`. README updated to "eighteen-slide". | Slide count changed. |

## Sources verified (2026-11-06)

- **Silna:** [Predictive Document Intelligence](https://www.silnahealth.com/resources/predictive-document-intelligence/). Vendor's own page: checks documents for completeness before submission. The 98% first-pass rate is a company claim.
- **Flexbone:** [vendor's own page](https://flexbone.ai/blog/what-is-cohere-health/). Agents assemble documentation and staff review before submission.
- **Waystar, Optum Digital Auth Complete, Notable, AKASA:** seen only in third-party directories (Elion, Honey Health, Innovaccer). **Not verified on the vendors' own sites.** Verify before quoting specifics.
- **Cohere Health** is mainly **payer-side**, not a provider-side competitor.
- **CMS-0057-F:** [CMS fact sheet](https://www.cms.gov/newsroom/fact-sheets/cms-interoperability-prior-authorization-final-rule-cms-0057-f). Covers Medicare Advantage, Medicaid, CHIP, and QHP issuers on federal exchanges. The Prior Authorization API must identify documentation requirements. APIs are due mainly Jan 1, 2027. Drugs are excluded.

## Open item: a newer AMA survey exists

The deck cites the **2024** AMA survey (fielded Dec 2024). The AMA has published a **[2025 AMA Prior Authorization Physician Survey](https://www.ama-assn.org/system/files/prior-authorization-survey.pdf)**, fielded **December 2025**, n=1,000. Figures that were readable in the PDF text extraction (re-check against the PDF before using):

- 40 PAs per physician per week (was 39); 40% have PA-only staff
- 94% say PA increases burnout (was 89%)
- 26% serious adverse event, 22% life-threatening event, 8% disability, permanent damage, or death
- 32% say PAs are often or always denied; 21% always appeal
- Reasons for not appealing: 59% expect no success, 52% lack staff or time
- 60% concerned AI increases or will increase denials (was 61%)
- 24% say their EHR offers electronic PA for prescriptions (was 23%)
- Phone is the most common method for medical-service PAs
- New in 2025: the insurer pledge of June 2025; only 33% of physicians expect it to make a meaningful difference

The weekly-hours figure and several other percentages did not extract cleanly. Read them from the PDF.

**Why it matters:** The 2025 survey was fielded **after** several AI PA tools launched (Silna, for example, launched in April 2025), and the burden still appears. This weakens the "tools are too new to show up in the data" explanation and strengthens the adoption and payer-side explanations. **Decision for Wendyl:** update slides 2–7 and 15 to the 2025 figures, or keep 2024 and add a note. Not done yet.

## Suggestions not yet applied (need Wendyl's decision)

1. **Pick one service on the last slide.** Lumbar spine MRI or a step-therapy biologic. Note that imaging PA is often handled by radiology benefit managers (eviCore, Carelon), so their guideline may be the policy source.
2. **Consolidate evidence slides 2–7.** Several figures repeat (89%, 13 hours, 40%).
3. **Add interview questions** to the last slide or a backup slide:
   - Do you use PA software today? If not, why not?
   - Where does your time go per request: checking whether PA is required, gathering evidence, submitting, or follow-up and appeals?
   - How often are requests pended or denied for missing documents versus the payer's criteria?
   - Would you upload chart PDFs to a separate tool? Would compliance allow it?
4. **Pre-existing styling quirk:** `.coral{color:var(--coral)}` also colors the text in `.card.coral` and `.note.coral` red (for example, slide 9's problem card). Not changed.

## Claims to keep out of the deck (from the Gemini audit)

- "31% don't appeal due to staff time" / "1 in 3 denials never appealed." Wrong: 31% is the often-or-always-denied rate.
- "13 hours per doctor wasted." Wrong: the 13 hours is physician **and staff** time.
- "Missing documentation is the **leading** cause of overturns." Wrong: CMS says a **common** reason, in targeted Medicare fee-for-service programs.
- "45 minutes → 90 seconds." Made up; there is no baseline.
- "CMS-0057-F excludes commercial plans." Partly wrong: it covers QHPs on the federal exchanges.
- "Clear product whitespace." Unsupported; see slide 14.

## Verification done

Desktop screenshots (1440×900) of slides 4, 9, 14, and 15 checked visually. Phone-width headless screenshots clip on the right, but original slide 2 clips the same way. This is a headless-Chrome minimum-width artifact, not caused by these edits. Check on a real phone if needed.

## Follow-up edit (2026-11-06)

- Last slide (18): "suitable for a four-week demonstration?" changed to "suitable for an eight-week hackathon build?". Wendyl confirmed the hackathon build is 8 weeks.
