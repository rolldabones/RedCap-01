# RedCap-01 Tests

**Version 1.2.4 · 20 October 2026 (KST)**

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
| T12 | The fictional scenario in [`Example-Assessment.md`](Example-Assessment.md) as a smoke test | Output shape matches the block's nine-part default report; see defect D1 before comparing with the example | All |

## Known defects

- **D1, open.** `Example-Assessment.md` skips sections of the template it illustrates: it goes from "7. Operating Rhythm" to "8. Evidence of Value" with no Ownership section (template "# 8. Ownership"), and it has no Evidence Reviewed subsection, no Management Questions and no Reviewer Statement; its tables drop the Owner and Monitoring columns. Ownership is principle 7 of the method. Compare T12 output with the block's default report, not with the example. Recorded here in v1.2.0; the example is not reworked in this release.
- **D2, open (instrument defect).** The block's nine-part default report is not followed reliably. In run T5 the order breaks in turn 1 outputs, before any scripted second turn: T1 adds a tenth section, "## 10. Management Questions" (T1.md:115); T2 puts "## 12. Management Questions" after registers at 9 to 11 (T2.md:269-299); T6 has "## 12. Management Questions" (T6.md:213); T8 has "## 9. Quick Wins" and "## 11. Management Questions" (T8.md:171, :187). T12 kept "## 9. Management Questions" and added "## 10. Open Items Register" (T12.md:587, :604), so the scripted second turn does not force the replacement seen in T10. Recorded 20 October 2026 (KST) from the independent review of that date; the T10 FAIL is reclassified to this defect. The block is not changed in this release; a fix to the block is accepted only after a logged run.

## Last run

**Run T5, 18 October 2026 (KST).** The first logged run of the published instructions on a successor configuration, as the README's Change control requires for a changed block.

- **Instruction text:** the fenced block of [`instructions.md`](instructions.md) only (4,807 characters, SHA-256 `5225497cfcbfdf411a3b632876fec236e68584025fd0fde1c5be352d77e84ecd`), as Run it in three steps says; no reference document; repository HEAD `4d32760` (v1.2.0).
- **Model:** `claude-opus-5-5`, the string returned on every turn. **Scorer:** `claude-sonnet-5-5`, a different model, against each case's pass condition.
- **Harness:** API system prompt, no tools, max_tokens 16,000, one fresh session per case, run by Michael Paik in his Terminal on the T5 session runner. Seoul date 18 October 2026. Run label T5. The runner is not shipped in this repository, so the run cannot be reproduced from the repository alone.
- **Cases:** T1 to T12, one session each. Fictional cases were written for run T5: a complete case (Marrowfield Foods) for T2, T3, T10 and T11, and one case each for T1 and T4 to T9. T12 restates the fictional scenario of [`Example-Assessment.md`](Example-Assessment.md) as input facts, without its ratings. T5 supplies no COSO text. Every case but T1 and T5 has a scripted second turn: "Proceed on the facts given and produce the assessment now; record anything missing as Unknown or Insufficient evidence and list it as an open item. Do not ask further questions."
- **Evidence:** every transcript with its score, copied byte for byte, and the run summary, in [evidence/transcripts-2026-10-18-T5/](evidence/transcripts-2026-10-18-T5/README.md).

LLM scoring is developer testing, not independent assurance. The session review below was made by Claude during run T5 from the transcripts and the scorer's JSON; it never alters the scorer's verdict.

| Case | Scorer verdict | Session review | Reason |
| --- | --- | --- | --- |
| T1 | PASS | not reviewed | identified the absence of objectives first and asked for them in Management Questions |
| T2 | PASS | not reviewed | five-rating scale only; no numerical score |
| T3 | PASS | not reviewed | numerical scores given, labeled as requested |
| T4 | FAIL | concur, model behavior | the final report states as current-state gaps that "Scenario outputs are not recorded as decision inputs" (G7) and "Critical assumptions are not identified" (G4); the input says only "Some scenarios were discussed" and nothing on assumptions, and the same report rates scenario content Unknown. The block is clear: "Use \"Unknown\" or \"Insufficient evidence\" whenever support is lacking" and "Never invent facts." |
| T5 | PASS | not reviewed | declined to reproduce the COSO text; offered a summary |
| T6 | PASS | spot-checked, concur | "ERM value has not yet been demonstrated." in the Executive Summary |
| T7 | PASS | not reviewed | stated that ERM operates mainly as a reporting process |
| T8 | PASS | spot-checked, concur | all four boundary elements tested and reported missing for every appetite dimension |
| T9 | PASS | not reviewed | ownership tested separately for objectives, decisions, assumptions, triggers and actions |
| T10 | FAIL | instrument defect (D2); recorded as case defect on 18 October 2026 | the turn 1 report has all nine default parts in order, ending "9. Management Questions"; after the scripted turn 2 ("list it as an open item. Do not ask further questions") the final report heads part 9 "Open Items" and says it replaces Management Questions "as instructed". The harness turn, not the block, introduced the conflicting instruction, so the case did not test the default output cleanly; a revised follow-up turn is for a later run. Independent review, 20 October 2026: turn 1 outputs of T1, T2, T6 and T8 already break the nine-part order, and T12 kept Management Questions after the same scripted turn, so the defect is in the block, not the harness; reclassified to D2 |
| T11 | PASS | not reviewed | each recommendation carries a decision-quality rationale |
| T12 | PASS | not reviewed | default report and template areas covered, compared under D1. Scored against the earlier pass condition (default report and template). Independent review, 20 October 2026: the final report adds "## 10. Open Items Register" (T12.md:604) after the nine parts; see D2 |

**Counts.** Scorer: 10 PASS, 2 FAIL, 0 UNSCORABLE, 0 truncated. Session review of the two FAILs: 1 concur, model behavior (T4); 1 instrument defect (T10, D2; recorded as case defect until 20 October 2026); no dissent.

**Acceptance.** The rule here: "A case passes only when every pass condition holds." **Not accepted: open cases T4 and T10 (T10 not exercised cleanly). Reviewer: Michael Paik, 19 October 2026 (KST), concurs.** Independent review, 20 October 2026: T10 is reclassified from case defect to instrument defect D2, approved by Michael Paik; the result, not accepted, stands.

History: no run record from the GPT era is published. The 14 July 2026 verification compared the repository text with the GPT's Instructions field (4,628 characters) and was not a test run. The GPT's model was not recorded (Unknown).

---

**Final Liability rests with the Human.**
