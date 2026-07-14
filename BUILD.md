# Building RedCap-01

**Version:** 1.1.0
**Date:** 14 July 2026
**Status:** Production
**Repository:** RedCap-01
**Part of:** GRC next™

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

## Relationship to GRC next™

RedCap-01 complements existing repositories.

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

1. Reviewing the GRC next™ ecosystem.
2. Identifying capability overlap.
3. Defining one missing capability.
4. Studying the COSO 2026 guidance.
5. Designing a bounded diagnostic.
6. Building and deploying the RedCap-01 Custom GPT.
7. Mirroring the deployed configuration in this repository (v1.1.0).

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

## Building the Custom GPT

### Production configuration

The deployed RedCap-01 Custom GPT is configured as follows. [`RedCap-01-Custom-GPT.md`](RedCap-01-Custom-GPT.md) mirrors the live instruction block verbatim.

| Field | Value |
|---|---|
| Name | RedCap-01 |
| Description | An evidence-oriented Enterprise Risk Management (ERM) assessment assistant within the GRCnext™ ecosystem |
| Instructions | The block in `RedCap-01-Custom-GPT.md`, pasted exactly |
| Knowledge | *From Guidance to Action* (lawfully obtained) plus authorized, appropriately redacted internal materials |
| Conversation starters | None configured |
| Capabilities | Web Search, Canvas, Image Generation, Code Interpreter & Data Analysis |

### Configuration steps

1. Create a new Custom GPT in the GPT builder.
2. Set the name and description exactly as above.
3. Paste the instruction block from `RedCap-01-Custom-GPT.md` into the Instructions field. Paste only the block that follows the header divider; do not include this repository's header material.
4. Upload a lawfully obtained copy of *From Guidance to Action* to Knowledge. Add internal materials only if authorized and appropriately redacted.
5. Enable the capabilities listed above. Reduce the set if your deployment does not need them; fewer capabilities means a smaller surface.
6. Leave conversation starters empty to match production, or add your own; they do not change behavior.
7. Restrict sharing to the intended audience before publishing.
8. Test before first use (below).

### Testing approach

Before relying on the tool, verify at minimum that it:

- begins with objectives and refuses to begin with a risk list
- uses the five-rating qualitative scale and declines numerical maturity scores unless requested
- answers "Unknown" or "Insufficient evidence" when given deliberately incomplete inputs rather than inferring
- refuses to reproduce text from the uploaded COSO publication
- separates facts, observations, assumptions, gaps and recommendations in the default report
- states that ERM value has not been demonstrated when no observable outcomes are provided

Run the fictional scenario in [`Example-Assessment.md`](Example-Assessment.md) as a smoke test and compare the shape of the output.

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

## Future evolution

Potential future enhancements include:

- integration with RedCap-00
- decision traceability
- portfolio analytics
- AI-assisted evidence review
- structured board reporting
- objective mapping

The current release intentionally excludes those capabilities to preserve a tightly scoped diagnostic.

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

The repository and the deployed Custom GPT version together. A change to the live instruction block requires a repository release in the same cycle, and the reverse.

---

## Closing thought

RedCap-01 is intentionally modest.

It does not attempt to solve Enterprise Risk Management.

It asks one question exceptionally well.

> **Does Enterprise Risk Management improve the decisions that determine whether organizational objectives are achieved?**

**Final Liability rests with the Human.**
