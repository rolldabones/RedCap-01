# Building RedCap-01

**Version:** 1.2.0
**Date:** 18 October 2026
**Status:** Instrument; the custom GPT was retired on 1 October 2026
**Repository:** RedCap-01
**Part of:** GRCnext™

---

## Purpose

RedCap-01 was created to answer one practical question:

> **Does our Enterprise Risk Management (ERM) improve the decisions that determine whether we achieve our objectives?**

Many ERM programs produce extensive documentation. Far fewer demonstrably improve organizational decisions.

RedCap-01 is intentionally narrow. It is an evidence-oriented diagnostic for determining whether ERM is genuinely objective-centric, decision-useful and operationally embedded.

It is **not**:

- an ERM framework
- a maturity model
- a replacement for COSO Enterprise Risk Management, ISO 31000 or other governance frameworks

Instead, it complements them.

---

## Why this repository exists

The 2026 COSO paper *From Guidance to Action: Exploring Practical Enterprise Risk Management* argues that:

- strategy and risk are inseparable
- risk exists only in relation to objectives
- ERM creates value by improving decisions
- ERM should be embedded where decisions are made
- documentation should support decisions rather than become the objective

RedCap-01 operationalizes those ideas as a practical diagnostic method rather than reproducing the publication.

---

## Design philosophy

Every RedCap repository answers exactly one governing question.

**RedCap-00**

> Can we execute meaningful operational options under stress?

**RedCap-01**

> Does Enterprise Risk Management improve the decisions that determine whether organizational objectives are achieved?

Everything in this repository supports answering that question.

---

## Relationship to GRCnext™

RedCap-01 complements existing repositories in governance, risk management and compliance (GRC).

| Repository | Primary question |
|---|---|
| **grc-workbook** | How do we build and operate an effective GRC capability? |
| **risk-informed-decision-making-prompt** | How should we analyze and govern this decision? |
| **RedCap-00** | Can we execute meaningful operational options under stress? |
| **RedCap-01** | Does ERM improve the decisions that determine whether objectives are achieved? |

RedCap-01 deliberately avoids duplicating capabilities already provided by these repositories.

---

## Design principles

RedCap-01 is designed to be:

- Objective-first
- Decision-led
- Evidence-oriented
- Conservative about uncertainty
- Explainable
- Auditable
- Actionable
- Lightweight
- Practical
- Framework-neutral

---

## Why not another maturity model?

Most maturity models ask:

> *How mature is your ERM?*

RedCap-01 instead asks:

> *What evidence demonstrates that ERM improved an important decision?*

Observable outcomes take precedence over process maturity.

---

## Why qualitative assessments?

False precision is a recurring governance problem.

RedCap-01 therefore defaults to qualitative ratings rather than numerical maturity scores.

It asks users to demonstrate:

- which decision changed
- what assumptions changed
- which trigger caused action
- who owned the response
- what value resulted

---

## Development process

The repository was developed by:

1. Reviewing the GRCnext™ ecosystem.
2. Identifying capability overlap.
3. Defining one missing capability.
4. Studying the COSO 2026 guidance.
5. Designing a bounded diagnostic.
6. Building and deploying the RedCap-01 custom GPT (retired 1 October 2026).
7. Mirroring the GPT's configuration in this repository (v1.1.0); since v1.2.0 the published block in `instructions.md` is the text of record.

---

## Knowledge sources

### Primary inspiration

Ryan Luttenton, Stefany Samp and Alexa Stone

*From Guidance to Action: Exploring Practical Enterprise Risk Management*

Committee of Sponsoring Organizations of the Treadway Commission (COSO), 2026.

This publication is copyrighted. RedCap-01 summarizes and operationalizes concepts without reproducing protected content.

### Additional references

- COSO Enterprise Risk Management (2017)
- ISO 31000
- ISO/IEC 42001
- NIST AI Risk Management Framework
- OCEG Principled Performance

References only. No conformance or alignment claim is made. See the dated regulatory and standards currency note in the README.

---

## Build history: the custom GPT

From v1.1.0 to v1.1.7 this repository mirrored a RedCap-01 custom GPT built in OpenAI's GPT builder. The GPT was retired on 1 October 2026 and converted to a private plug-in on the OpenAI platform, and its configuration is Locked as of that date. The configuration as last deployed and the builder procedure this section carried are archived in [CHANGELOG.md](CHANGELOG.md) v1.2.0.

## Build your own

1. Paste the fenced block in [`instructions.md`](instructions.md) into the system prompt, custom instructions or project instructions of any current assistant. That takes the place of the GPT's Name, Description and Instructions fields.
2. If you hold a lawfully obtained copy of *From Guidance to Action*, supply it as a reference document; that takes the place of the GPT's Knowledge upload. Add internal materials only if authorized and appropriately redacted.
3. The block needs no tools. The GPT had Web Search, Canvas, Image Generation and Code Interpreter & Data Analysis enabled; enable tools only where your deployment needs them, since fewer tools means a smaller surface.
4. Choose the model yourself. The GPT's model was not recorded.
5. Restrict sharing to the intended audience.
6. Run the cases in [`tests.md`](tests.md) before first use.

### Testing approach

The cases a build must pass, the known defects and the run record are in [`tests.md`](tests.md).

### Limitations

The tool inherits every limitation stated in the README: it is not legal advice, not a compliance determination, not an audit opinion and not a certification of ERM effectiveness. Its output quality is bounded by the accuracy, completeness and candor of the inputs. Jurisdiction and regulatory obligations remain unknown unless supplied and verified. Platform behavior can change without notice; retest after significant platform updates.

---

## Acceptance criteria

RedCap-01 succeeds when users can:

- identify objective-risk misalignment
- improve decision quality
- clarify ownership
- define usable decision boundaries
- establish meaningful triggers
- strengthen executive discussions
- improve board reporting
- avoid unnecessary documentation

---

## Versioning philosophy

Minor releases:

- documentation
- prompt refinements
- templates
- examples

Major releases:

- assessment logic
- method changes
- governance model
- acceptance criteria

The RedCap-01 GPT configuration is Locked as of 1 October 2026. A change to the instruction block in `instructions.md` requires a repository release in the same cycle and, under ruling 9, is accepted only after one logged run of the published instructions as a system prompt on a current frontier model, recorded in `tests.md`.

---

## Closing thought

RedCap-01 is intentionally modest.

It does not attempt to solve Enterprise Risk Management.

It asks one question exceptionally well.

> **Does Enterprise Risk Management improve the decisions that determine whether organizational objectives are achieved?**

---

**Final Liability rests with the Human.**
