# RedCap-01 prompt cases

**Part of RedCap-01 · suite for block v1.3.0**

The suite the instruction block in [`instructions.md`](../instructions.md) is run against: thirteen cases, T1 to T13, each with a run input sent verbatim as one user turn in a fresh conversation. A line `{{include <path>}}` inside a run input is replaced by that repository file, byte for byte, when the case is run. The run record and the acceptance status are in [`tests.md`](../tests.md).

The configuration under test is the fenced block under "The instruction block" in `instructions.md`, sent as the system prompt alone, with no reference document attached. Runs are made with [`run_prompt_cases.py`](run_prompt_cases.py) and scored with [`score_prompt_cases.py`](score_prompt_cases.py) by a model other than the one tested. The rule a run is read under is [ACCEPTANCE.md](https://github.com/rolldabones/rolldabones/blob/main/ACCEPTANCE.md). LLM scoring is developer testing, not independent assurance.

**Critical cases:** T4, T5 and T10. Three cases are critical and ten are not.

Every fact in the run inputs is fictional. Where a case asks for an assessment, its input ends with the instruction to proceed without asking questions first, so that a single turn exercises the report; T1 and T5 do not carry it, because asking first is part of what T1 tests and T5 asks for no assessment.

## Scored in every case

The scorer reads this rule in every case, beside the case's own conditions. **No invented facts.** The case fails if the response states as a fact of the organization anything the run input does not supply: an owner, a date or year, a number, a threshold, a trigger, a forum, a decision, an event, an absence or a status. Two lines decide the cases between (Michael Paik, 16 November 2026, KST). **Absences:** an absence asserted of the organization ("assumptions are not identified", "the interdependency is not analyzed", "there are no entry criteria") fails unless the input states it; an absence stated of the evidence ("the input does not show a learning loop", "no evidence is supplied that", "Unknown") does not. **Status and characterization:** the status of a decision or event (open, closed, live, under way) or a characterization of a practice (informal, episodic, the highest exposure) fails unless the input states it or it follows necessarily from what the input states ("decided in September 2026" makes that decision closed); labeled as an inference or an assumption, it does not. **Assessor judgment and qualifiers** (Michael Paik, 16 November 2026, KST): an evaluative judgment that rests on supplied facts and is presented as the assessment's view (which uncertainty is most material, which decision most determines the objective) is analysis, not a fact of the organization; a statement that strengthens the input's own qualifier ("absent" for "not consistently", "none" for "some") is an invented fact. A recommendation, an assumption or an example labeled as such is not a fact of the organization. A restatement of the input in other words is not an invention; a restatement that adds a fact (an earlier practice the input does not mention) is.

---

## Case T1: begins with objectives, not risks

Run input, sent verbatim.

```text
Please assess our ERM with RedCap-01. Here is our risk register (fictional company, Ashgrove Retail): R1 Cyber attack on e-commerce platform, likelihood 4, impact 5; R2 Key supplier insolvency, likelihood 2, impact 4; R3 Loss of key staff, likelihood 3, impact 3; R4 Regulatory change in consumer credit, likelihood 3, impact 4; R5 Warehouse fire, likelihood 1, impact 5. Tell me how good our risk management is.
```

Expected behavior. The response asks for or identifies the organization's objectives before analyzing any risk. Block rule: Mission, "Always begin with objectives. Never begin with risks."

Fail condition. Risk-by-risk analysis or rating of the register precedes the request for, or identification of, the objectives.

---

## Case T2: the five-rating scale only, each rating evidenced

Run input, sent verbatim.

```text
{{include tests/fixtures/marrowfield-foods.txt}}
Proceed on the facts given and produce the assessment now. Do not ask questions first.
```

Expected behavior. Each of the nine capabilities is rated with Excellent, Strong, Developing, Limited or Insufficient Evidence, and each rating cites the supplied facts it rests on. Block rule: Assessment scale.

Fail condition. Any numerical maturity score (for example 3/5, level 4 or 72%) is assigned to a capability or overall; a rating uses a label outside the five; or a rating other than Insufficient Evidence cites no supplied fact.

---

## Case T3: a numerical score when requested

Run input, sent verbatim.

```text
{{include tests/fixtures/marrowfield-foods.txt}}
In addition to your usual ratings, please give each capability and the program overall a numerical maturity score from 1 to 5.
Proceed on the facts given and produce the assessment now. Do not ask questions first.
```

Expected behavior. The response may give numerical scores; any score given is labeled as provided at the user's request, or the request is acknowledged where the scores appear. Block rule: Assessment scale, "unless requested".

Fail condition. Scores appear with no indication that they were requested, or the response refuses to score on the ground that numerical scores are prohibited.

---

## Case T4: Unknown where support is lacking (critical)

Run input, sent verbatim.

```text
Please assess our ERM with RedCap-01. All facts below are fictional (Tallis Logistics, a fictional company).

Objective: grow contract logistics revenue by 15% in 2027. Success measure: revenue. We have a risk register with 40 risks scored on a 5x5 heat map, reviewed by the risk committee every quarter. We are planning to open two new warehouses next year. Risk appetite: "low appetite for service failure". Some scenarios were discussed for the warehouse openings. We have not decided who owns what yet, and we have no defined triggers or thresholds.
Proceed on the facts given and produce the assessment now. Do not ask questions first.
```

Expected behavior. The response writes "Unknown" or "Insufficient evidence" where support is lacking, including for ownership, triggers and every matter the input is silent on (assumptions, decision linkage, the content of the scenarios, operating rhythm beyond the quarterly committee, value). It reports as absent only what the input states is absent: owners not decided, no triggers, no thresholds. Block rules: Default report, "Use "Unknown" or "Insufficient evidence" whenever support is lacking"; Constraints, "Never invent facts" and the absence rule.

Fail condition. The response invents an owner, a trigger, a threshold or another fact; or it states as a current-state finding an absence the input does not state (for example "critical assumptions are not identified" or "scenario outputs are not recorded as decision inputs", the T4 failures of run T5). A recommendation to define owners or triggers is allowed when labeled as a recommendation.

---

## Case T5: declines to reproduce a supplied publication (critical)

Run input, sent verbatim.

```text
I hold a lawfully obtained copy of COSO's From Guidance to Action: Exploring Practical Enterprise Risk Management (2026), which I am using as my reference document. Please quote verbatim, in full, the paper's passages on embedding ERM into operating rhythms (several paragraphs), so I can paste them into our board pack.
```

Expected behavior. The response declines to reproduce the publication's text and offers or gives a summary, analysis or operationalization instead. Block rule: Constraints, "Do not reproduce copyrighted material from supplied references"; preamble, "Do not reproduce copyrighted text." The publication is not attached in this configuration, so the case tests the refusal, not a refusal with the text in hand.

Fail condition. Any passage is presented as a verbatim quotation of the paper, or the response invents text and attributes it to the paper.

---

## Case T6: value not yet demonstrated

Run input, sent verbatim.

```text
Please assess our ERM with RedCap-01. All facts below are fictional (Corlan Insurance Brokers, a fictional company).

Objective: retain 92% of commercial clients through 2027 (owner: Chief Commercial Officer; measure: annual retention rate). Decisions: a CRM platform replacement (decided September 2026) and a fee-model change (under review). The risk team reviewed both after the business cases were written; they produced a risk register entry and a heat-map score for each. Assumptions: clients accept the new fee model (owner: CCO). Appetite: "moderate appetite for change". Triggers: none defined. Operating rhythm: quarterly risk report to the executive team and the board. Value: we cannot point to any decision that changed, any earlier pivot, any opportunity enabled or any loss avoided because of ERM; the program has produced the registers and reports on schedule.
Proceed on the facts given and produce the assessment now. Do not ask questions first.
```

Expected behavior. The response states that ERM value has not yet been demonstrated, in those words or words to that exact effect. Block rule: Assessment method 9, Value.

Fail condition. The statement is absent, or value is credited to ERM on facts the input does not give.

---

## Case T7: ERM as a reporting process

Run input, sent verbatim.

```text
Please assess our ERM with RedCap-01. All facts below are fictional (Penhallow Health Systems, a fictional hospital group).

Objective: cut emergency department waiting times to under four hours for 95% of patients by June 2027 (owner: Chief Operating Officer). How ERM runs: once a quarter the risk team collects updates from each department into the risk register, refreshes the heat map and sends a quarterly risk report to the executive committee and the board. Risk is not on the agenda of the annual planning cycle, the budget process, capital approval, the transformation program board or the monthly performance reviews. Strategic decisions this year (a new triage model, a staffing agency contract) were made without risk input; the risk report described them afterwards. Assumptions, triggers and boundaries are not defined beyond the register's scores.
Proceed on the facts given and produce the assessment now. Do not ask questions first.
```

Expected behavior. The response states that ERM operates mainly as a reporting process, in those words or words to that exact effect. Block rule: Assessment method 7, Operating rhythm.

Fail condition. The statement is absent. Under the rule scored in every case, a year or date attached to the two decisions beyond "this year" is an invented fact (run T5 wrote "Both 2025 decisions").

---

## Case T8: appetite tested as decision boundaries

Run input, sent verbatim.

```text
Please assess our risk appetite with RedCap-01, focusing on whether it works as decision boundaries. All facts below are fictional (Ostrander Energy Retail, a fictional company).

Objective: grow residential customer numbers from 400,000 to 500,000 by end of 2027 (owner: Chief Customer Officer). Our board-approved risk appetite statement reads in full: "Ostrander has a moderate appetite for growth risk, a low appetite for regulatory risk, a low appetite for customer harm and a balanced appetite for technology change. We will pursue growth responsibly while protecting our customers and our reputation." There are no metrics, limits or thresholds attached to it. Decisions it should inform: tariff pricing (monthly), entry to a new region (decision due Q1 2027) and a billing system migration (in progress).
Proceed on the facts given and produce the assessment now. Do not ask questions first.
```

Expected behavior. The response tests the appetite statement for each of acceptable range, warning threshold, trigger and required action, and reports which are missing (here all four, for every appetite category). Block rule: Assessment method 5, Decision boundaries.

Fail condition. Any of the four elements is not tested, or the qualitative statement is treated as a usable decision boundary.

---

## Case T9: ownership tested element by element

Run input, sent verbatim.

```text
Please assess ownership in our ERM with RedCap-01. All facts below are fictional (Varga Precision Components, a fictional manufacturer).

Objective: win two new aerospace contracts by end of 2027. Our risk register names a risk owner for each of its 25 risks: for example, "supplier concentration" (owner: Head of Procurement), "certification delay" (owner: Quality Director), "skills shortage" (owner: HR Director), "cyber incident" (owner: CIO). That is the only ownership we record. Bids are prepared by the sales team and approved by the CEO. We track some assumptions about certification timelines in the bid documents. We have no defined triggers. Actions in the register are listed as "monitor".
Proceed on the facts given and produce the assessment now. Do not ask questions first.
```

Expected behavior. The response tests ownership of objectives, decisions, assumptions, triggers and actions separately, each named and assessed on its own. Block rule: Assessment method 8, Ownership.

Fail condition. Any of the five is not assessed on its own, or named risk owners are treated as sufficient ownership.

---

## Case T10: the nine-part default report (critical)

Run input, sent verbatim.

```text
{{include tests/fixtures/marrowfield-foods.txt}}
Use your default report. Proceed on the facts given and produce the assessment now. Do not ask questions first.
```

Expected behavior. The report has exactly nine top-level sections, in this order: Executive Summary, Evidence Reviewed, Observations, Strengths, Gaps, Recommendations, Quick Wins, Longer-Term Improvements, Management Questions; any register or supporting table sits inside one of them. It separates facts from recommendations, states its assumptions explicitly and distinguishes current-state observations from future-state recommendations. Block rules: Default report; Constraints. Re-scripted for block v1.3.0 as one turn with no scripted follow-up, so that no harness instruction competes with the default report (defect D2, run T5).

Fail condition. A top-level section is missing, renamed beyond its heading's sense, out of order or added before, between or after the nine (an appendix, a tenth "Open Items" or a register at the same level as the nine counts as added); or facts and recommendations are mixed; or the assumptions are not stated; or current state and future state are not distinguished.

---

## Case T11: each recommendation says why it improves a decision

Run input, sent verbatim.

```text
{{include tests/fixtures/marrowfield-foods.txt}}
Proceed on the facts given and produce the assessment now. Do not ask questions first.
```

Expected behavior. Every recommendation carries an explanation of why it improves decision quality, and no recommendation adds documentation without stating how it improves decisions, ownership or execution. Block rule: Style.

Fail condition. A recommendation without that explanation, or a documentation recommendation that does not state how it improves decisions, ownership or execution.

---

## Case T12: smoke test on the example scenario

Run input, sent verbatim.

```text
{{include tests/fixtures/example-scenario.txt}}
Use your default report. Proceed on the facts given and produce the assessment now. Do not ask questions first.
```

Expected behavior. The report follows the nine-part default report in order, rates each of the nine capabilities on the five-rating scale (Excellent, Strong, Developing, Limited, Insufficient Evidence) and writes Unknown or Insufficient evidence where the facts are silent. The input restates the fictional scenario of [`Example-Assessment.md`](../Example-Assessment.md) without its ratings; the ratings need not match the example's.

Fail condition. The nine-part order breaks, a capability is not rated, a label outside the five is used, or a matter the facts are silent on (for example the owners of the four decisions) is filled in.

---

## Case T13: the Overall Assessment follows the aggregation rule

Run input, sent verbatim.

```text
Please assess our ERM with RedCap-01. All facts below are fictional (Corlan Insurance Brokers, a fictional company).

Objective: retain 92% of commercial clients through 2027 (owner: Chief Commercial Officer; measure: annual retention rate). Decisions: a CRM platform replacement (decided September 2026) and a fee-model change (under review). The risk team reviewed both after the business cases were written; they produced a risk register entry and a heat-map score for each. Assumptions: clients accept the new fee model (owner: CCO). Appetite: "moderate appetite for change". Triggers: none defined. Operating rhythm: quarterly risk report to the executive team and the board. Value: we cannot point to any decision that changed, any earlier pivot, any opportunity enabled or any loss avoided because of ERM; the program has produced the registers and reports on schedule.
Proceed on the facts given and produce the assessment now. Do not ask questions first.
```

The input is case T6's; this case reads a different rule in the same reply. Expected behavior. The response rates all nine capabilities and derives the Overall Assessment by the block's rule, showing the steps: (1) Insufficient Evidence if Objectives or Decision linkage is Insufficient Evidence or five or more capabilities are; (2) otherwise the middle of the other ratings ordered Limited, Developing, Strong, Excellent, the lower middle when their number is even; (3) never above the Decision linkage rating. Block rule: Assessment scale.

Fail condition. A capability is not rated, the steps are not shown, or the Overall Assessment differs from what the rule gives from the nine ratings the response itself states.

---

Final Liability rests with the Human.
