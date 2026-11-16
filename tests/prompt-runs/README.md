# Prompt runs

The records of the logged runs of the cases in [prompt-cases.md](../prompt-cases.md), made with [run_prompt_cases.py](../run_prompt_cases.py) on `claude-opus-5-5` and scored with [score_prompt_cases.py](../score_prompt_cases.py) by `claude-sonnet-5-5`. Transcripts are in [transcripts/](transcripts/) as the runner wrote them, with the closing line appended after the runner's end marker and nothing else changed; each score file has a JSON twin of the same name in [scores/](scores/). The status and the session review rest on run 20261116-R4 and are in [tests.md](../../tests.md). LLM scoring is developer testing, not independent assurance; the Human reviewer reads every sample and owns the status.

| Run | Date (KST) | Block | Manifest | Scores | Result |
|---|---|---|---|---|---|
| 20261116-R4 | 16 November 2026 | `d2ca8ba0, as published` | [manifest](transcripts/20261116-R4_claude-opus-5-5_run.json) | [opus, scored by sonnet](scores/20261116-R4_claude-opus-5-5_scored-by_claude-sonnet-5-5.md) | 10 of 13, not accepted (status of record) |
| 20261116-R3 | 16 November 2026 | `f8fcca60, draft` | [manifest](transcripts/20261116-R3_claude-opus-5-5_run.json) | [opus, scored by sonnet](scores/20261116-R3_claude-opus-5-5_scored-by_claude-sonnet-5-5.md) | 12 of 13, not accepted |
| 20261116-R2 | 16 November 2026 | `28f5383d, draft` | [manifest](transcripts/20261116-R2_claude-opus-5-5_run.json) | [opus, scored by sonnet](scores/20261116-R2_claude-opus-5-5_scored-by_claude-sonnet-5-5.md) | 10 of 13, not accepted |
| 20261116-R1 | 16 November 2026 | `b0385357, draft` | [manifest](transcripts/20261116-R1_claude-opus-5-5_run.json) | [opus, scored by sonnet](scores/20261116-R1_claude-opus-5-5_scored-by_claude-sonnet-5-5.md) | 9 of 13, not accepted |

R1 to R3 ran drafts of block v1.3.0, each revised after the run before it; the rule scored in every case gained rulings A and B before R2 and D before R3 (CHANGELOG.md, v1.3.0). Their score files were written under the case file as it then stood.

---

**Final Liability rests with the Human.**
