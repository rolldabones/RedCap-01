# RedCap-01 Tests

**Version 1.2.0 · 18 October 2026 (KST)**

The checks that the published instructions in [`instructions.md`](instructions.md) must pass, the known defects and the run record. The cases are drawn from the block's own rules and from the testing approach that `BUILD.md` carried until v1.2.0.

## Cases

Run each case as a fresh conversation with the fenced block as the system prompt. A case passes only when every pass condition holds.

| ID | Input | Pass condition | Block rule |
| --- | --- | --- | --- |
| T1 | A risk register with no stated objectives, and a request to assess it | Asks for or identifies the objectives before analyzing any risk; does not begin with the risk list | Mission: "Always begin with objectives. Never begin with risks." |
| T2 | A complete fictional case, no scoring method requested | Uses only Excellent, Strong, Developing, Limited or Insufficient Evidence; no numerical maturity score | Assessment scale |
| T3 | The T2 case with an explicit request for a numerical maturity score | May give a score, labeled as requested by the user | Assessment scale: "unless requested" |
| T4 | A deliberately incomplete case (no owners, no triggers) | Writes "Unknown" or "Insufficient evidence" where support is lacking; invents no owner, trigger or fact | Default report; Constraints: "Never invent facts." |
| T5 | A request to quote passages of a supplied COSO publication | Declines to reproduce the text; summarizes or operationalizes instead | Constraints: copyrighted material |
| T6 | A case with no observable ERM outcomes | States that ERM value has not yet been demonstrated | Assessment method 9, Value |
| T7 | A case where ERM runs only as quarterly reporting | States that ERM operates mainly as a reporting process | Assessment method 7, Operating rhythm |
| T8 | A risk appetite statement with no thresholds | Tests for acceptable range, warning threshold, trigger and required action and reports which are missing | Assessment method 5, Decision boundaries |
| T9 | A case with named risk owners only | Tests ownership of objectives, decisions, assumptions, triggers and actions separately | Assessment method 8, Ownership |
| T10 | Any complete case, default output | Follows the nine-part default report in order; separates facts from recommendations; states assumptions explicitly; distinguishes current-state observations from future-state recommendations | Default report; Constraints |
| T11 | Any complete case | Explains why each recommendation improves decision quality; recommends no added documentation unless it improves decisions, ownership or execution | Style |
| T12 | The fictional scenario in [`Example-Assessment.md`](Example-Assessment.md) as a smoke test | Output shape matches the default report and the template in [`Objective-Decision-Assessment.md`](Objective-Decision-Assessment.md); see defect D1 before comparing with the example | All |

## Known defects

- **D1 (reviewer report 12, item B3), open.** `Example-Assessment.md` skips sections of the template it illustrates: it goes from "7. Operating Rhythm" to "8. Evidence of Value" with no Ownership section (template "# 8. Ownership"), and it has no Evidence Reviewed subsection, no Management Questions and no Reviewer Statement; its tables drop the Owner and Monitoring columns. Ownership is principle 7 of the method. Compare T12 output with the template and the block's default report, not with the example. Recorded here in v1.2.0; the example is not reworked in this release.

## Last run

No logged run of the published instructions on the successor configuration as at 18 October 2026 (KST). Under ruling 9 a changed block is accepted only after one such run, naming the model string and date, recorded here.

History: no run record from the GPT era is published. The 14 July 2026 verification compared the repository text with the GPT's Instructions field (4,628 characters) and was not a test run. The GPT's model was not recorded (Unknown).

---

**Final Liability rests with the Human.**
