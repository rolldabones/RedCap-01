# Run T5 transcripts, RedCap-01

**Evidence · run T5 · 18 October 2026 (KST)**

What: the transcripts of run T5 of the `redcap-01` suite, one file per case, each with the case's rule, pass condition, the full conversation and the scorer's verdict and reasoning, and [summary.json](summary.json), the runner's summary (repository HEAD `4d32760`, system-file digests, models, max_tokens, finish time).

When: finished 2026-10-18T10:49+09:00 (Seoul).

Models: tested `claude-opus-5-5`; scored by `claude-sonnet-5-5`, a different model. LLM scoring is developer testing, not independent assurance. Harness: API system prompt, no tools, max_tokens 16000, one fresh session per case. System text (the fenced block of instructions.md extracted byte for byte, then any knowledge file named): `RedCap-01-instructions.txt` SHA-256 `5225497cfcbfdf411a3b632876fec236e68584025fd0fde1c5be352d77e84ecd`.

How produced: the session T5 runner (`t5_run.py`, a session tool, not shipped in this repository) run by Michael Paik in his Terminal; the suite manifest was written in session T5 from this repository's test cases. Each transcript here is the runner's output copied byte for byte; the only change is the closing line appended at the end of each file. `summary.json` is copied unchanged. Model output is verbatim and is not edited for house style. The session review of each verdict and the acceptance result are in [tests.md](../../tests.md).

| Case | Scorer verdict |
|---|---|
| [T1](T1.md) | PASS |
| [T2](T2.md) | PASS |
| [T3](T3.md) | PASS |
| [T4](T4.md) | FAIL |
| [T5](T5.md) | PASS |
| [T6](T6.md) | PASS |
| [T7](T7.md) | PASS |
| [T8](T8.md) | PASS |
| [T9](T9.md) | PASS |
| [T10](T10.md) | FAIL |
| [T11](T11.md) | PASS |
| [T12](T12.md) | PASS |

---

Final Liability rests with the Human.
