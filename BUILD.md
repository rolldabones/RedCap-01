# BUILD.md

# Building RedCap-01

**Version:** 0.1.0  
**Status:** Initial Build  
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

RedCap-01 complements existing repositories.

| Repository | Primary question |
|---|---|
| **GRC Workbook** | How do we build and operate an effective GRC capability? |
| **Risk-Informed Decision Making** | How should we analyze and govern this decision? |
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
6. Building a supporting Custom GPT.

---

## Knowledge sources

### Primary inspiration

Ryan Luttenton  
Stefany Samp  
Alexa Stone

*From Guidance to Action: Exploring Practical Enterprise Risk Management*

Committee of Sponsoring Organizations of the Treadway Commission (COSO), 2026.

This publication is copyrighted. RedCap-01 summarizes and operationalizes concepts without reproducing protected content.

### Additional references

- COSO Enterprise Risk Management (2017)
- ISO 31000
- ISO/IEC 42001
- NIST AI Risk Management Framework
- OCEG Principled Performance

---

## Building the Custom GPT

### Recommended configuration

**Name**

RedCap-01

**Description**

Objective-to-Risk Alignment Check

**Knowledge**

Upload:

- *From Guidance to Action: Exploring Practical Enterprise Risk Management*
- Relevant internal documentation (appropriately authorized and, where appropriate, redacted)

**Instructions**

Use:

`prompts/RedCap-01-Custom-GPT.md`

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

## Future evolution

Potential future enhancements include:

- integration with RedCap-00
- decision traceability
- portfolio analytics
- AI-assisted evidence review
- structured board reporting
- objective mapping

Version 1 intentionally excludes those capabilities to preserve a tightly scoped diagnostic.

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

---

## Closing thought

RedCap-01 is intentionally modest.

It does not attempt to solve Enterprise Risk Management.

It asks one question exceptionally well.

> **Does Enterprise Risk Management improve the decisions that determine whether organizational objectives are achieved?**
