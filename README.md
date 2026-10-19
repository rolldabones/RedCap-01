# RedCap-01

**Objective-to-Risk Alignment Check**

**Version 1.2.2 · 19 October 2026 · Instrument, formerly the RedCap-01 custom GPT (retired 1 October 2026) · Instructions last verified against the GPT on 14 July 2026, before the conversion · Part of GRCnext™ · License: [CC BY-NC-SA 4.0](LICENSE.md)**

> **Retired 1 October 2026 (KST).** The RedCap-01 custom GPT was retired on 1 October 2026 and converted to a private plug-in on the OpenAI platform. The instructions published in this repository are the text of record and suffice for anyone who wants to build their own. History and sources: [RETIREMENT.md](https://github.com/rolldabones/rolldabones/blob/main/RETIREMENT.md).

## What it does

A focused, evidence-oriented diagnostic for testing whether Enterprise Risk Management (ERM) is genuinely anchored to organizational objectives, strategic decisions and operational execution. It assesses nine capabilities, from objective integrity to value and learning, on a five-rating qualitative scale, and it answers "Unknown" or "Insufficient evidence" where support is lacking.

> **Governing question:** Does our Enterprise Risk Management improve the decisions that determine whether we achieve our objectives?

## Run it in three steps

1. Paste the fenced block in [`instructions.md`](instructions.md) into the system prompt, custom instructions or project instructions of any current assistant. There is no `reference.md`: the GPT's knowledge file was a copy of COSO's *From Guidance to Action*, which this repository does not reproduce, so supply your own lawfully obtained copy if you have one.
2. Give it the inputs it asks for (see How to use it below) or start from the fictional case in [`Example-Assessment.md`](Example-Assessment.md).
3. Review the output yourself and check it against [`tests.md`](tests.md). You own sign-off.

## What this is

RedCap-01 is a practical self-assessment and advisory tool within the **GRCnext™** ecosystem.

**What this instrument is, stated plainly.** This is a **structured self-assessment**. It is not a measurement, a benchmark, an audit, a certification or a rating. Its outputs are the organization's own answers, organized against a defined structure and disciplined by an evidence rule. That structure is what makes the answers comparable over time and arguable in front of a board. It does not make them independent. A score produced here evidences the organization's position; it does not attest to it, and it should never be presented externally as though a third party had.

It tests whether an organization's ERM:

- begins with explicit objectives rather than disconnected risk lists
- informs consequential strategic and operational decisions
- makes assumptions and uncertainty visible
- translates risk appetite into usable decision boundaries
- uses observable triggers tied to defined actions
- assigns ownership to the people responsible for outcomes
- operates inside existing planning, investment and performance rhythms
- demonstrates value through decisions influenced, pivots enabled, opportunities supported and surprises reduced

RedCap-01 is deliberately narrow. It does not attempt to replace an ERM framework, redesign an entire governance, risk management and compliance program or decide a specific business issue for management.

## Why it exists

Many ERM programs produce risk registers, heat maps, risk and control self-assessments, dashboards and board reports. Those artifacts may be necessary, but they do not by themselves demonstrate that ERM improves decisions.

The practical test is whether risk information reaches decision-makers while meaningful options remain and whether it changes what the organization chooses, monitors, funds, pauses, escalates or revisits.

RedCap-01 was inspired by the Committee of Sponsoring Organizations of the Treadway Commission (COSO) paper *From Guidance to Action: Exploring Practical Enterprise Risk Management* (2026). The paper emphasizes that strategy and risk are inseparable, ERM should create and protect value, risk information should be decision-useful and ERM should be embedded into the operating rhythms where choices are made.

RedCap-01 converts that practical orientation into a bounded diagnostic.

## Regulatory and standards currency

Verified 14 July 2026. *From Guidance to Action* was released by COSO on 4 May 2026 and is COSO's current supplemental ERM guidance; the COSO Enterprise Risk Management framework (2017) remains the framework of record. This repository cites COSO, ISO 31000, ISO/IEC 42001, the NIST AI Risk Management Framework and OCEG as references only. It makes no conformance, alignment or certification claim against any of them. Verify current status before relying on any framework reference.

## The assessment

RedCap-01 examines nine connected capabilities.

### 1. Objective integrity

- Are the relevant objectives explicit?
- Are success measures or outcome criteria identifiable?
- Is each objective owned?
- Is the objective sufficiently clear to support risk analysis?

### 2. Decision linkage

- Which decisions materially determine whether the objective is achieved?
- Does ERM influence those decisions before options close?
- Can the organization identify a decision that changed because of ERM?

### 3. Assumptions

- What assumptions must remain true?

### 4. Uncertainty

- What uncertainties could materially alter the expected outcome?
- Are ranges and scenarios used where point estimates would create false precision?
- Are material interdependencies visible?

### 5. Risk posture and decision boundaries

- What uncertainty is the organization willing to accept in pursuit of the objective?
- Which outcomes or conditions are unacceptable?
- Has risk appetite been translated into usable boundaries?
- Can a leader apply those boundaries to a real decision?

### 6. Triggers and action

- What observable signals require reassessment?
- Who monitors each trigger?
- What happens when a trigger is reached?
- Is the response a defined action, escalation, pause or pivot rather than a request for more reporting?

### 7. Ownership and follow-through

- Who owns the objective?
- Who owns the decision?
- Who monitors assumptions and triggers?
- Who has authority to act?
- Is follow-through visible and reviewable?

### 8. Operating rhythm

- Is ERM present in strategy setting, planning, budgeting, capital allocation, transformation, delivery and performance reviews?
- Or does ERM operate as a parallel reporting process?
- Do risk discussions occur early enough to preserve options?

### 9. Value and learning

- What did ERM change?
- Which decisions were improved?
- Which pivots occurred earlier?
- Which opportunities were enabled?
- Which surprises, losses or delays were reduced?
- What was learned and incorporated into the next decision cycle?

## Assessment scale

RedCap-01 uses a qualitative scale unless the user expressly requests another method:

| Rating | Meaning |
| --- | --- |
| **Excellent** | The capability is embedded, decision-useful, owned and supported by current evidence. |
| **Strong** | The capability is generally effective, with limited gaps that do not materially impair decision use. |
| **Developing** | Important elements exist, but use is inconsistent, incomplete or weakly evidenced. |
| **Limited** | The capability is largely informal, episodic, artifact-led or disconnected from decisions. |
| **Insufficient Evidence** | Available information does not support a reliable conclusion. |

RedCap-01 does not convert these ratings into a numerical maturity score by default. It avoids false precision and states uncertainty directly.

## Evidence discipline

The assessment is evidence-oriented and conservative.

Claims should be supported by high-level references to artifacts or observable practices, such as:

- approved objectives or strategy materials
- decision records
- investment or transformation papers
- risk appetite statements
- thresholds and trigger definitions
- named owner roles
- action or escalation logs
- operating committee agendas
- board or executive materials
- post-decision reviews
- evidence of a pivot, avoided loss or enabled opportunity

Do not paste confidential information, personal data, credentials, bank details, sensitive contract text, regulator correspondence, security vulnerabilities or export-controlled information. Use redacted summaries and artifact descriptions.

When support is absent or unclear, RedCap-01 uses **Unknown/Insufficient data** rather than filling gaps by inference.

## What you get

Depending on the requested scope, RedCap-01 can produce:

- an Objective-to-Risk Alignment Review
- an Executive ERM Assessment
- an objective and decision map
- an assumptions and uncertainty register
- a decision boundary register
- a trigger and action register
- a prioritized gap assessment
- quick wins and longer-term improvements
- a board-ready summary
- questions requiring management judgment

The default report distinguishes:

1. facts and evidence provided
2. observations
3. assumptions
4. gaps
5. recommendations
6. management decisions required

## How to use it

### Fast diagnostic

Use one material objective or initiative.

Provide:

- the objective
- the decision or decisions that matter
- the accountable owner
- the most important assumptions
- the relevant risk appetite or boundaries
- current triggers and actions
- the forum and cadence where the issue is reviewed
- examples of decisions ERM has influenced

RedCap-01 will identify the strongest linkages, material gaps and the smallest practical improvements.

### Program-level review

Use a defined portfolio of strategic objectives.

Provide high-level descriptions of:

- strategy and objective-setting
- ERM processes
- risk appetite
- executive and board reporting
- planning and investment forums
- trigger monitoring
- ownership and escalation
- recent decisions or pivots influenced by ERM

RedCap-01 will assess whether the program operates as a decision-support system or mainly as an artifact and reporting process.

### Design mode

Use the tool prospectively to design an objective-centric ERM layer for a new strategy, transformation or major initiative.

The tool will help translate the objective into:

- critical decisions
- assumptions
- uncertainty ranges
- risk posture
- boundaries
- triggers
- owners
- actions
- review cadence
- evidence of value

### Example prompts

- Test whether our ERM is linked to our strategic objectives.
- Review this objective and identify the decisions, assumptions, boundaries and triggers that matter.
- Assess whether our risk appetite is usable in real decisions.
- Convert this ERM report into a decision-useful executive brief.
- Identify where our ERM process is producing activity rather than decision value.

See [`BUILD.md`](BUILD.md) for the design rationale, build history and limitations, and [`tests.md`](tests.md) for the checks.

## Change control

The RedCap-01 GPT configuration is Locked as of 1 October 2026; the configuration as last deployed is archived in [CHANGELOG.md](CHANGELOG.md), in the entry that retired the GPT. Changes are made in [`instructions.md`](instructions.md) under this repository's version rule (Status, below). A changed block is accepted only after one logged run of the published instructions as a system prompt on a current frontier model, recorded in [`tests.md`](tests.md). The block's first logged run, T5 on 18 October 2026 (KST) on `claude-opus-5-5`, passed 10 of 12 cases; it is not accepted, pending review (`tests.md`, Last run; transcripts in [`evidence/transcripts-2026-10-18-T5/`](evidence/transcripts-2026-10-18-T5/README.md)).

## Part of the ecosystem

This repository is one tool in a connected set. The canonical map is [ECOSYSTEM.md](https://github.com/rolldabones/rolldabones/blob/main/ECOSYSTEM.md) in the profile repository. Nearest neighbors:

- [grc](https://github.com/rolldabones/grc): the **GRCnext™** framework whose primitives (Services, Tolerances, Pipes, Switches, Exits) sit beneath this tool's boundaries, triggers and ownership tests
- [grc-workbook](https://github.com/rolldabones/grc-workbook): the workbook instrument for building and operating an integrated governance, risk management and compliance capability, within which RedCap-01 serves as a focused ERM diagnostic
- [risk-informed-decision-making-prompt](https://github.com/rolldabones/risk-informed-decision-making-prompt): structures a single decision under uncertainty; RedCap-01 operates one level above, testing whether the ERM system consistently reaches the decisions that matter
- [RedCap-00](https://github.com/rolldabones/RedCap-00): tests whether an organization can execute five critical operational moves within 72 hours under disruption; RedCap-01 tests the upstream link between objectives, risk and decisions
- [AI-Impact-Assessment-Tool](https://github.com/rolldabones/AI-Impact-Assessment-Tool): the companion assessment gate for AI system deployment, also published as an instrument since its custom GPT was retired on 1 October 2026

Governing questions across the set:

| Repository | Governing question |
| --- | --- |
| **grc-workbook** | How do we build and operate an effective GRC capability? |
| **risk-informed-decision-making-prompt** | How should we analyze and govern this decision? |
| **RedCap-00** | Can we execute meaningful operational options under stress? |
| **RedCap-01** | Does ERM improve the decisions that determine whether objectives are achieved? |

## Repository structure

The repository is intentionally flat; its one folder, `evidence/`, holds run records.

```
RedCap-01/
├── README.md                          Overview, method, run steps and change control
├── BUILD.md                           Design rationale, build history, limitations
├── instructions.md                    Instruction block, text of record
├── tests.md                           Test cases, known defects, run record
├── evidence/                          Run transcripts, copied byte for byte (run T5, 18 October 2026)
├── PRINCIPLES.md                      The ten principles behind the method
├── Objective-Decision-Assessment.md   Full assessment template
├── Decision-Boundary-Register.md      Decision boundary register template
├── Trigger-Register.md                Trigger register template
├── Example-Assessment.md              Fictional worked example
├── CHANGELOG.md                       Version history
├── CONTRIBUTING.md                    Contribution guidance
└── LICENSE.md                         CC BY-NC-SA 4.0
```

## Important limitations

RedCap-01 is:

- not legal advice
- not a compliance determination
- not an audit opinion
- not a certification of ERM effectiveness
- not a substitute for management, board, legal, risk, finance, internal audit or subject-matter judgment
- dependent on the accuracy and completeness of information provided
- designed to identify gaps and decision points, not to eliminate uncertainty

Jurisdiction, regulatory obligations and authoritative requirements remain unknown unless supplied and verified.

## Design commitments

RedCap-01 is designed to remain:

- objective-first
- decision-led
- evidence-oriented
- conservative about uncertainty
- lightweight
- usable under real constraints
- clear about ownership
- focused on observable value
- complementary to existing **GRCnext™** methods

It should not become a general ERM encyclopedia, a documentation generator or a substitute for the broader repositories to which it connects.

## Reference and attribution

RedCap-01 is an independent GRCnext™ tool inspired by:

Ryan Luttenton, Stefany Samp and Alexa Stone, *From Guidance to Action: Exploring Practical Enterprise Risk Management*, Committee of Sponsoring Organizations of the Treadway Commission, 2026.

Official COSO materials:

- [New ERM Guidance](https://www.coso.org/new-erm-guidance)
- [Enterprise Risk Management Guidance](https://www.coso.org/guidance-erm)

The cited COSO publication is copyrighted. This repository does not reproduce it. Users should obtain and use the publication subject to the publisher's terms.

RedCap-01 is not affiliated with, sponsored by or endorsed by COSO or Crowe LLP.

## Status

**Version:** 1.2.2
**Date:** 18 October 2026
**Status:** Instrument; the custom GPT was retired on 1 October 2026 and its configuration is Locked as of that date
**Method:** Objective-to-Risk Alignment Check
**Ecosystem:** GRCnext™
**Compatibility:** grc-workbook, risk-informed-decision-making-prompt, RedCap-00
**Versioning:** the account rule, at release 1.2.2. The README masthead, this Status block, How to Cite, `CITATION.cff`, the CHANGELOG head and the release tag move together. `BUILD.md`, `instructions.md` and `tests.md` keep the version line of the release that last changed them, stated in each file's own header; `PRINCIPLES.md` was added at 1.1.7. Every change is logged in [CHANGELOG.md](CHANGELOG.md). This block replaces `VERSION.md`, deleted at 1.1.7.

## How to Cite

> Paik, Son-U Michael. *RedCap-01*, v1.2.2. GRC Solutions Korea, 2026. https://github.com/rolldabones/RedCap-01

A machine-readable citation is in [CITATION.cff](CITATION.cff).

## License

Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0). See [`LICENSE.md`](LICENSE.md).

Third-party publications, trademarks and referenced materials remain subject to their respective rights and terms.

---

**Final Liability rests with the Human.**
