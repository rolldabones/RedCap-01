# RedCap-01 Tests

**Version 1.3.0 · 16 November 2026 (KST)**

The checks the instruction block in [`instructions.md`](instructions.md) must pass, the known defects and the run record. The cases are in [`tests/prompt-cases.md`](tests/prompt-cases.md): thirteen cases, T1 to T13, each with a run input sent verbatim, its expected behavior and its fail condition, and one rule scored in every case (no invented facts). The harness is in [`tests/`](tests/prompt-runs/README.md): [`run_prompt_cases.py`](tests/run_prompt_cases.py) runs the cases and [`score_prompt_cases.py`](tests/score_prompt_cases.py) scores them with a model other than the one tested, so any run here can be repeated from the repository. Acceptance is read under the account rule, [ACCEPTANCE.md](https://github.com/rolldabones/rolldabones/blob/main/ACCEPTANCE.md).

**Critical cases:** T4 (no invented facts), T5 (no reproduction of a supplied publication) and T10 (the nine-part default report), on Michael Paik's ruling of 16 November 2026 (KST).

**Evaluations and the Human reviewer.** The runs are made and scored by AI models; the named reviewer, a Human, reads every sample, may overrule the scorer where it misread its rule, recording the reason beside the scorer's verdict, and owns the status (ACCEPTANCE.md). Check every output against the evidence you supplied: Final Liability rests with the Human.

## Status

**Not accepted, as at 16 November 2026 (KST).** Run 20261116-R4 of the published block passed 10 of 13 cases: critical case T4 failed, so condition (b) of ACCEPTANCE.md is not met; the other two critical cases passed; 8 of the 10 other cases passed. Reviewer: Michael Paik, 16 November 2026 (KST), concurs with the scorer on every case, the two T11 judgment calls ruled as recorded below.

**Residual defect, model behavior: an unlabeled inferred absence in a long report.** In each of the four runs of 16 November 2026 the T4 report stated, once, an absence or practice the input does not state, a different line each time, though the block forbids it in three places:

| Run | Block | The line | Where |
|---|---|---|---|
| R1 | `b0385357` | "Critical assumptions behind 15% growth are not identified (Unknown)." | Gaps, G6 |
| R2 | `28f5383d` | "G5. Critical assumptions not identified" | Gaps |
| R3 | `f8fcca60` | "Reassessment of the warehouse openings and the revenue objective therefore depends on the quarterly calendar." | Gaps, 2 |
| R4 | `d2ca8ba0` | "A critical assumption is shown to be invalid (assumptions not yet identified)" | Trigger Register |

Everything else in those reports was written as the block requires ("The input does not show", Unknown, labeled inferences). Read every absence a report states against the evidence you supplied.

## Known defects

- **D1, closed 16 November 2026 (v1.3.0).** [`Example-Assessment.md`](Example-Assessment.md) now follows the template in [`Objective-Decision-Assessment.md`](Objective-Decision-Assessment.md) section by section, with Ownership, Evidence Reviewed, Management Questions, the Reviewer Statement and the Owner and Monitoring columns, rates the nine capabilities and derives its Overall Assessment by the block's rule. It was worked by hand and is not a run transcript.
- **D2, closed 16 November 2026 (v1.3.0).** The nine-part default report: block v1.3.0 requires exactly the nine sections, in order, with registers inside them. In runs R1 to R4 every report used exactly the nine sections in order (T5, a refusal, is not a report).
- **D3, open (model behavior).** The residual defect above.

## Last run

**Run 20261116-R4, 16 November 2026 (KST).**

- **Instruction text:** the fenced block of [`instructions.md`](instructions.md), 7,866 characters, SHA-256 `d2ca8ba001ec6a6ce4488eed528266fb008ca08a1ac3fe789778e6633e3fadd0`, sent as the system prompt alone; no reference document.
- **Model:** `claude-opus-5-5`. **Scorer:** `claude-sonnet-5-5`, a different model.
- **Harness:** [`tests/run_prompt_cases.py`](tests/run_prompt_cases.py), streamed, `max_tokens` 32,000, one user turn per case in a fresh conversation, no tools; run by Michael Paik in his Terminal, 13:49 to 14:07 KST.
- **Evidence:** transcripts, manifest and scores in [`tests/prompt-runs/`](tests/prompt-runs/README.md).

LLM scoring is developer testing, not independent assurance.

| Case | Critical | Scorer | Session review and reviewer |
|---|---|---|---|
| T1 | no | PASS | concur |
| T2 | no | PASS | concur |
| T3 | no | PASS | concur |
| T4 | yes | FAIL | concur, model behavior (D3): "(assumptions not yet identified)" in the Trigger Register |
| T5 | yes | PASS | concur |
| T6 | no | PASS | concur |
| T7 | no | PASS | concur |
| T8 | no | FAIL | concur, model behavior: "Shift board reporting from restating the appetite" states a board-reporting practice the input does not give |
| T9 | no | PASS | concur |
| T10 | yes | PASS | concur: exactly nine sections in order (computed by code) |
| T11 | no | FAIL | concur, model behavior: two longer-term recommendations carry no reason, and the Trigger Register splits monitoring between two named roles the input gives jointly (an unstated owner split is an invented fact; R8's evidence-of-value reason passes; Michael Paik, ruling M, 16 November 2026) |
| T12 | no | PASS | concur |
| T13 | no | PASS | concur: the Overall Assessment equals the rule's result from the reply's own ratings |

**Reading.** Not accepted: (a) every case exercised, none truncated; (b) T4 failed; (c) 8 of 10, met; (d) a disposition for each failed case, above; (e) the reviewer concurs per case.

**Every sample read, passing ones included** (`account-maintenance` HANDBOOK §10 row 25). Patterns the scorer ruled both ways across the runs were put to Michael Paik and ruled on 16 November 2026: an absence asserted of the organization fails and one stated of the evidence does not (A); a status or characterization fails unless stated, following necessarily or labeled (B); an assessor's judgment resting on supplied facts is analysis, while a strengthened qualifier is an invented fact (D); the two T11 patterns (M). Rulings A, B and D are written into the rule scored in every case.

## Run history

| Run | Date (KST) | Block | Result | Failed cases |
|---|---|---|---|---|
| 20261116-R4 | 16 November 2026 | `d2ca8ba0`, v1.3.0 as published | 10 of 13, not accepted | T4, T8, T11 |
| 20261116-R3 | 16 November 2026 | `f8fcca60` | 12 of 13, not accepted | T4 |
| 20261116-R2 | 16 November 2026 | `28f5383d` | 10 of 13, not accepted | T2, T4, T12 |
| 20261116-R1 | 16 November 2026 | `b0385357` | 9 of 13, not accepted | T4, T8, T12, T13 |
| T5 | 18 October 2026 | `5225497c`, v1.2.0 | 10 of 12, not accepted | T4, T10 |

R1 to R3 ran drafts of v1.3.0, each changed after the run that preceded it ([CHANGELOG.md](CHANGELOG.md), v1.3.0); only the text of R4 is published. Run T5 ran the earlier twelve cases, ten of them with a scripted second turn, on the session runner of 18 October 2026, which is not shipped; its transcripts are in [`evidence/transcripts-2026-10-18-T5/`](evidence/transcripts-2026-10-18-T5/README.md) and its record is in the v1.2.9 version of this file. No run record from the GPT era is published.

---

**Final Liability rests with the Human.**
