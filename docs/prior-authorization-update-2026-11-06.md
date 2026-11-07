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

## Changes from second Gemini review (applied 2026-11-06)

**Status:** Applied and published on 2026-11-06 with Wendyl's go-ahead. Slide 13 keeps slides 11–12 unchanged (they still show the agent doing both tasks); the slide 13 note frames policy-to-checklist as possibly simpler software "we would test", not as a decided architecture change. Note links (`.note a`) now use the teal link style.

**How the review was run:** a new Gemini chat with no earlier context, using a strict prompt (list all slide titles first, cite sources, no scores, no rewrites). Gemini could not read slides 9–18 from the live page, so it was given the full slide text. Claude checked its claims against first-party sources. Results are below.

### Applied (verified)

| Slide | Change | Source |
|---|---|---|
| 5 | Label the 31% as **physician-reported** ("reported that PAs are often or always denied" is a perception, not an actual denial rate). Add context: Medicare Advantage insurers denied **7.7%** of PA requests in 2024, and more than 80% of appealed denials were overturned. Do not merge the two numbers. | [KFF, MA PA determinations 2024](https://www.kff.org/medicare/medicare-advantage-insurers-made-nearly-53-million-prior-authorization-determinations-in-2024/) |
| 13 | State plainly which step needs an agent. **Policy → checklist (Task 1)** can be simpler software (structured extraction or rules). **Chart search and reconciliation (Task 2)** is where an agent may add value: choosing what to search, checking dates and durations across scattered notes, resolving conflicts, escalating uncertainty. Keep the existing "What we still need to prove" note. | Gemini review; consistent with Claude's earlier concern that Problem 1 can look like a document pipeline rather than an agent |
| 14 | Add one line on the HL7 Da Vinci standards (CRD, DTR, PAS): DTR uses FHIR questionnaires with CQL rules to pull **structured** EHR data for payer documentation requirements. **Unstructured** clinical notes remain a gap, which is the concept's possible opening. | [HL7 Da Vinci DTR IG](https://build.fhir.org/ig/HL7/davinci-dtr/) |
| 14 | Add **Humata Health**. In June 2026 it launched a drag-and-drop upload portal for independent practices, regional health centers, and specialty clinics, very close to this concept's standalone idea and target clinics. | [Humata, independent practices](https://www.humatahealth.com/resources/prior-authorization-independent-practices) |
| 15 | Add CAQH evidence: only **35%** of medical prior authorizations are fully electronic (X12 278), per the 2024 CAQH Index. This fits better than the AMA's 23% (prescriptions only). Keep both, labeled. | [CAQH CORE priority topics, citing the 2024 CAQH Index](https://www.caqh.org/core/priority-topics) |
| 15 | Under Compatibility, note that Humata's upload portal is a **signal both ways**: a vendor is betting small clinics will accept uploading records (supports the theory), and the small-clinic gap now has a direct competitor (weakens it). | Same Humata source |

### Do not apply (Gemini was wrong or unverified)

- **"The deck links denials to preparation gaps."** It doesn't. Slide 9 says the concept does not guarantee fewer denials. No change.
- **HHS-OIG misread:** Gemini said 13% of denials were *because of* extra payer criteria. The OIG found 13% of denials **met Medicare coverage rules**; extra criteria was one reason among several. Slide 8 is already correct.
- **Cohere Health as a provider-side competitor:** it is mainly payer-side. Do not add it as a competitor.
- **Epic native PA automation, Basys.ai, Rhyme/Infinx:** not verified. Check the vendors' own sites before adding anything.

### Already handled (no change)

- Manual upload friction and HIPAA/BAA burden: already listed as challenges on slide 15.
- Hallucination and fail-closed behavior: covered on slides 13 and 16.
- Synthetic data only: covered on slides 11, 17, and 18.

## Workflow diagram and slide 11 update (2026-11-06)

**Why:** The slide 12 diagram was a straight line (order → read policy → match evidence → validate → review → submit). Slides 13 and 17 promise re-searching, retries, and escalation, and both Gemini reviews asked whether this is "just a document pipeline". Missing evidence also had no path back to people.

**What changed:**

| File | Change |
|---|---|
| `diagrams/prior-authorization-human-ai.workflow.json` | Added edge `validation-retry` from `validateDraft` to `matchEvidence` (label "gaps: search again", role `return`, `toSide: right`). Updated card text: "Match chart evidence; re-check notes when gaps or conflicts appear" and "Clinicians add missing records; staff review and submit". |
| `diagrams/prior-authorization-human-ai.html`, `.visual-check.1440x900.light.png`, `.visual-check.json` | Regenerated with Archify (`deliver workflow … --quality showcase`, then `visual-check`). Slide 12 uses the 1440×900 light PNG. |
| `specifications/prior-authorization-human-ai.workflow.json` | **Was stale** (old single agent node, from before commit 0cc8418). Now a copy of the diagrams version. Treat `diagrams/…workflow.json` as the source of truth. |
| `prior-authorization.html` slide 11 | Caption adds: "If evidence is missing or conflicting, the agent searches the chart again; real gaps go to the clinician to add records before staff review." |

**Tried and rejected:** a separate human node "Add documentation" with its own return edges. It widened the diagram so node text fell below 6px at 1440×900 (Archify `composition/desktop-readability` error). Pinning the retry edge `fromSide: left` was rejected (`workflow/explicit-pin-conflict`). The clinician step is therefore shown in the slide 11 caption and the diagram's card, not as a node.

**Verification:**
- Archify showcase validation: all 9 checks pass, 0 errors, 0 warnings. `deliver` ok.
- `visual-check`: pass at 1440×900, 1600×1000, 1920×1080, 2048×1320.
- Visual review of the PNG: the retry loop and the "validated draft or flagged gaps" path no longer share a line.
- Full deck review: all 18 slides screenshotted at 1440×900 with no overflow. Footers run 1–18. The one cross-reference ("slide 7" on slide 15) is correct. All 11 external links return HTTP 200.

**Known, pre-existing, not changed:**
- The `.coral` text-color quirk (red body text in `.card.coral` / `.note.coral`, e.g. slides 8, 9).
- Slide 7's "The 30% figure" card refers to a number not shown in that slide's stat row.
- The deck still uses the 2024 AMA survey; switching to the 2025 survey is an open decision for Wendyl (see above).
- Untracked Archify sidecars (dark and 2048 PNGs, `visual-check.html`) are left uncommitted.
