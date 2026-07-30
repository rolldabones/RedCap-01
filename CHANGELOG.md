# CHANGELOG

All notable changes to this repository. Versions follow semantic versioning. Prior versions are superseded upon release of the next.

---

## [1.1.1] - 2026-07-30

### Changed
- Trademark rendering corrected to the canonical closed-up form GRCnext™. The retired spaced form "GRC next" is withdrawn from repository prose. Thirteen occurrences across README.md, BUILD.md, DOCTRINE.md, CONTRIBUTING.md and Objective-Decision-Assessment.md, plus one unmarked bold occurrence in the README grc neighbor line.
- This reverses the v1.1.0 decision to standardize repository prose on the spaced form. That decision moved the repository out of alignment with its own production mirror, whose deployed instruction block and deployed Description both read GRCnext™. The prose and the mirror now agree.
- The explanatory note in RedCap-01-Custom-GPT.md rewritten to record the reversal and to state that no production change is required.
- README.md, BUILD.md, DOCTRINE.md, VERSION.md and RedCap-01-Custom-GPT.md moved to 1.1.1 in lockstep per the versioning rule in VERSION.md.

### Unchanged
- The deployed instruction block, byte for byte. It already carried the canonical form.
- The v1.1.0 entry below, which records the superseded standardization in its original wording. Historical entries are not rewritten.

## [1.1.0] - 2026-07-14

### Added

- LICENSE.md: CC BY-NC-SA 4.0, the ecosystem default (the README previously linked a LICENSE file that did not exist)
- Part of the ecosystem section linking the canonical ECOSYSTEM.md in the profile repository plus five nearest neighbors
- Dated regulatory and standards currency note: COSO's *From Guidance to Action* verified released 4 May 2026; framework references confirmed as references only, with no conformance claims
- Production mirror header in RedCap-01-Custom-GPT.md recording the deployed configuration: name, description, Knowledge, no conversation starters, capabilities (Web Search, Canvas, Image Generation, Code Interpreter & Data Analysis); instruction block verified verbatim against production, 4,628 characters
- BUILD.md configuration steps, testing approach and limitations sections (promised by the v1.0.0 README but absent)

### Changed

- README repository structure corrected to the actual flat layout: the v1.0.0 README described prompts/, templates/ and examples/ directories and a LICENSE file that never existed and omitted DOCTRINE.md
- Version lockstep restored at 1.1.0: README and BUILD carried 0.1.0 while CHANGELOG, DOCTRINE and VERSION carried 1.0.0
- Custom GPT description aligned to production ("An evidence-oriented Enterprise Risk Management (ERM) assessment assistant within the GRCnext™ ecosystem"); the v1.0.0 README and BUILD each carried a different, non-production description
- Conversation starters removed from the configuration (none are deployed) and retained in the README as example prompts
- Branding standardized to GRC next™ in repository prose, matching RedCap-00 and the canonical ecosystem map; the deployed instruction block retains GRCnext™ and is mirrored as deployed
- BUILD.md reference to the nonexistent path prompts/RedCap-01-Custom-GPT.md corrected
- Duplicate filename headings (a "# Filename.md" line above each document title) removed from all files
- Ecosystem relationship prose consolidated into the standard Part of the ecosystem section; the governing-questions table retained

### Fixed

- Broken LICENSE link in the README

### Superseded

- v1.0.0 README.md, BUILD.md, CHANGELOG.md, VERSION.md, DOCTRINE.md, RedCap-01-Custom-GPT.md and templates (release tag v1 retained as the historical record)

## [1.0.0] - 2026-07-13

### Added

- Initial RedCap-01 method
- README
- BUILD guide
- Custom GPT instructions
- Objective-to-Decision Assessment template
- Trigger Register template
- Decision Boundary Register template
- Example assessment
- DOCTRINE, VERSION, CONTRIBUTING

### Purpose

Initial release of the Objective-to-Risk Alignment Check. The repository provides a practical method for assessing whether Enterprise Risk Management is genuinely connected to objectives, decisions and operational execution.

### References

Primary inspiration: *From Guidance to Action: Exploring Practical Enterprise Risk Management*, Committee of Sponsoring Organizations of the Treadway Commission (COSO), 2026.

---

**Final Liability rests with the Human.**
