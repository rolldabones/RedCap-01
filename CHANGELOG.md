# CHANGELOG

All notable changes to this repository. Versions follow semantic versioning. Prior versions are superseded upon release of the next.

---

## [1.2.4] - 2026-10-20

Patch. Independent review of 20 October 2026; changes made with Claude, approved by Michael Paik. No change to the fenced block in `instructions.md`: its SHA-256 `5225497c...e84ecd` stands and the block stays at v1.2.0.

- **Test record.** `tests.md`: the T10 FAIL is reclassified from case defect to instrument defect, registered as known defect D2 (the nine-part default report is not followed reliably; turn 1 outputs of T1, T2, T6 and T8 already break the order). The recorded concurrence of 19 October 2026 is kept, with a dated note. The T12 pass condition names the block's nine-part default report only, and D1 is conformed. The T1 reason now matches its transcript. The run is stated as not reproducible from the repository alone, since the runner is not shipped. Version line to 1.2.4. Acceptance unchanged: not accepted, T4 and T10 open (RC1-01, RC1-06, RC1-11).
- **README.** A "Not accepted" caution opens Run it in three steps (RC1-04). The Change control sentence records the 19 October 2026 review (RC1-02). The Status block date moves with the masthead (RC1-03). Capabilities 7 and 8 are renumbered to match the block and tests, with the block's short names stated (RC1-05). The six-item default report list is replaced by the block's nine-part order (RC1-07). The no-evidence term is the block's own (RC1-14). The COSO paper's authors are named as of Crowe LLP, from the COSO press release of 4 May 2026 (RC1-15). The block's "measurably" is qualified against "It is not a measurement" (RC1-13). KST and COSO are spelled out (RC1-17).
- **Other files.** `PRINCIPLES.md` names the three doctrines and states the doctrine delta rule (RC1-16). `BUILD.md` spells out GRC and drops a doubled rule (RC1-17, RC1-19). `instructions.md` gains an acronym line outside the fence (RC1-17). `Example-Assessment.md` uses only the five-rating scale and the template's "Near Term", and spells out SLA (RC1-12, RC1-17). The evidence index lists cases T1 to T12 in numeric order; transcripts and `summary.json` are unchanged (RC1-20).
- **Internal references replaced by plain statements** in `tests.md`, `BUILD.md`, `CONTRIBUTING.md` and `PRINCIPLES.md`: the acceptance rule is stated, not cited by an internal ruling number, and the D1 source label is dropped. Shipped entries below are not rewritten (RC1-09).
- **Errata to shipped entries.** The 1.2.0 entry says "The block measures 4,808 characters". The fenced block is 4,807 characters; 4,808 counts the trailing newline, which the hashed text excludes (RC1-10). The untitled "License metadata sweep" paragraph inside the 1.1.2 entry shipped in release 1.1.2: commit `265e32a` of 13 August 2026, first carried by tag `v1.1.2` (RC1-08).
- README masthead, Status block and Versioning line, How to Cite, `CITATION.cff`, `BUILD.md` header, `tests.md` header and this head to v1.2.4.
- Findings applied: RC1-01, RC1-02, RC1-03, RC1-04, RC1-05, RC1-06, RC1-07, RC1-08, RC1-09, RC1-10, RC1-11, RC1-12, RC1-13, RC1-14, RC1-15, RC1-16, RC1-17, RC1-19, RC1-20. Owner-accepted, no change: RC1-18, RC1-21.

## [1.2.3] - 2026-10-20

- LICENSE: two defects against the Creative Commons legal code corrected (the space in 'ShareAlike. In'; the CC0 sentence of the closing notice). Operative terms unchanged.
- README masthead, version line and Versioning line, How to Cite and `CITATION.cff` to v1.2.3.

## [1.2.2] - 2026-10-19

Patch, from the weekly maintenance sweep of 19 October 2026 (KST) and Michael Paik's review of the T5 runs, completed 19 October 2026 (KST), on which he concurs with the scoring as recorded. No change to `instructions.md`.

- **Run T5 reviewed.** `tests.md` Acceptance records the reviewer. Not accepted, as before: T4 and T10 open. This closes the "Deferred: acceptance, pending Michael Paik's review" line of 1.2.1; the revised T10 follow-up turn stays deferred.
- README masthead, version line and Versioning line, How to Cite, `tests.md` masthead and `CITATION.cff` to v1.2.2.

## [1.2.1] - 2026-10-18

v1.2.1: records-only patch, the ruling 9 logged run. Session T5 (18 October 2026, KST) of the whole-account review of 15 October 2026 (the T5 row of the session plan, ruling 9 runs added 18 October 2026). No wording of `instructions.md` changes; the block stays at v1.2.0.

- **The ruling 9 run.** Cases T1 to T12 of `tests.md` were encoded one fresh session per case, the block as the system prompt, with no reference document (the README: "There is no `reference.md`"). Fictional cases were written for the cases that call for them (a complete case for T2, T3, T10 and T11; an incomplete case for T4; cases for T1 and T6 to T9). T12 restates the fictional scenario of `Example-Assessment.md` as input facts, without its ratings, and is compared with the default report and the template under defect D1. T5 supplies no COSO text: it tests the refusal to reproduce on the user's claim that the reference is in use. Tested model `claude-opus-5-5`; scored by `claude-sonnet-5-5`, a different model. **Result:** scorer 10 PASS, 2 FAIL (T4, T10). Session review: T4 concur, model behavior (two gaps stated as current-state facts the input does not support, under a block that says to write Unknown); T10 case defect (the scripted second turn's "Do not ask further questions" led the model to replace Management Questions with Open Items; its turn 1 report had all nine parts in order). Not accepted: open cases T4 and T10; reviewer pending (Michael Paik).
- **Evidence.** `evidence/transcripts-2026-10-18-T5/`: the 12 transcripts copied byte for byte with the closing line appended, the runner's `summary.json` and an index.
- **`tests.md`:** Last run section (configuration, per-case table, counts, acceptance); version line to 1.2.1. README: the Change control sentence and the layout tree name the run and `evidence/`.
- README masthead, Status block, How to Cite, `CITATION.cff` and this file move to 1.2.1 in lockstep.
- Findings by class: confirmed, no logged run (ruling 9); already fixed, none in scope; not reproducible, none; outside the review, none edited.
- Deferred: acceptance, pending Michael Paik's review; a revised T10 follow-up turn, for a later run. D1 (report 12 item B3, `Example-Assessment.md` against the template) stays open: it is an example rework, not a test or run item.

## [1.2.0] - 2026-10-18

v1.2.0: instrument form after the GPT retirement; `instructions.md` replaces `RedCap-01-Custom-GPT.md`. Session T4 (18 October 2026, KST) of the whole-account review of 15 October 2026: doc section 4, concrete changes 2 and 3, under determination D5 and ruling 9; reviewer report 12, items A5, A18, A19, B6 and B7. Amendment note, 18 October 2026 (KST): the RedCap-01 custom GPT was retired on 1 October 2026 and converted to a private plug-in on the OpenAI platform. Nothing was verified against the plug-in. The published instructions are the text of record as last verified against the GPT on 14 July 2026, before the conversion. The 1.1.5 and 1.1.6 entries below are shipped history and are not rewritten; the 11 December 2026 date and the retirement notice they describe leave the live text with this release.

- **`instructions.md` added; `RedCap-01-Custom-GPT.md` removed.** The block is now fenced and self-contained, under a status line and a how-to-use paragraph. Its two GPT-only dependencies are recast (below); every substantive rule is kept. The block measures 4,808 characters against the 4,628 verified on 14 July 2026. The file header's statement of an "8,000-character Instructions field limit" is not carried forward (report 12, A18): it described a GPT builder field that does not apply to the instrument, and it was stated as fact where the account elsewhere records the figure only as reported and not found in official documentation. Every inbound link now points to `instructions.md`.
- **`BUILD.md` "Future evolution" removed (report 12 B10).** ~~"Potential future enhancements include: integration with RedCap-00; decision traceability; portfolio analytics; AI-assisted evidence review; structured board reporting; objective mapping. The current release intentionally excludes those capabilities to preserve a tightly scoped diagnostic."~~ **STRUCK 18 October 2026 (KST)**, on the author's instruction of the same day to settle the open items: a roadmap unchanged since July and delivered in no release is a stale promise. The second of the two stale roadmaps the report named; the first left with `VERSION.md` at 1.1.7.
- **`tests.md` added.** Twelve cases drawn from the block's own rules and from the testing approach `BUILD.md` carried, known defect D1 (report 12, B3: `Example-Assessment.md` skips template sections; recorded, not reworked here) and the Last run section. `Example-Assessment.md` remains the worked example; no `example.md` is added.
- **README.** Masthead in the instrument form; the standard retirement line replaces the retirement notice; new What it does, Run it in three steps and Change control sections; The deployed Custom GPT section removed, its example prompts kept under How to use it; the AI-Impact-Assessment-Tool neighbor line recast (A19); repository map and Status block updated.
- **`BUILD.md`.** Header to 1.2.0; development process items 6 and 7 put in the past; Building the Custom GPT replaced by a build history paragraph and Build your own, mapping each GPT field to its successor (B6); Testing approach moved to `tests.md`; the versioning sentence states the Locked configuration and the ruling 9 acceptance run (A5); the closing line now follows a rule, as in the other files.
- **`CONTRIBUTING.md`.** Contributions to the block are proposals for the instrument, accepted under ruling 9's logged run (B7).
- README masthead, Status, How to Cite, `CITATION.cff` and this head to 1.2.0 in lockstep; the tag is `v1.2.0`. `PRINCIPLES.md`, the three templates, `Example-Assessment.md` and `LICENSE.md` are unchanged byte for byte.

### Instruction block changes (old → new)

1. Opening, authority sentence. Old: "The uploaded Knowledge documents are your primary authority." New: "Reference documents the user supplies, such as a lawfully obtained copy of COSO's *From Guidance to Action: Exploring Practical Enterprise Risk Management* (2026), are your primary authority." Added at the end of the same paragraph, after "Summarize, analyze and operationalize ideas.": "If none is supplied, work from the method below." Reason: no Knowledge file is attached outside the GPT.
2. Constraints. Old: "Do not reproduce copyrighted material from uploaded references." New: "Do not reproduce copyrighted material from supplied references." Reason: as 1.

### Configuration as last deployed, Locked 1 October 2026

As recorded in the header of `RedCap-01-Custom-GPT.md` (v1.1.1, verified 14 July 2026), verbatim:

- **Name:** RedCap-01
- **Description:** An evidence-oriented Enterprise Risk Management (ERM) assessment assistant within the GRCnext™ ecosystem
- **Knowledge:** a lawfully obtained copy of *From Guidance to Action: Exploring Practical Enterprise Risk Management* (COSO, 2026) plus any internal, appropriately redacted materials the user wants assessed
- **Conversation starters:** none configured
- **Capabilities enabled:** Web Search, Canvas, Image Generation, Code Interpreter & Data Analysis
- **Instructions:** the block as verified on 14 July 2026, 4,628 characters, carried into `instructions.md` with the two changes above. The verified text is at tag `v1.1.7`, `RedCap-01-Custom-GPT.md` lines 21 to 220.
- **Model:** Unknown (not recorded).

### Struck

From `RedCap-01-Custom-GPT.md` (removed):

- ~~"Version 1.1.1 · 30 July 2026 · Production mirror"~~ **STRUCK 18 October 2026 (KST).**
- ~~"This file carries the instruction block of the deployed RedCap-01 Custom GPT exactly as it appears in production, verified 14 July 2026 (4,628 characters, well under the 8,000-character Instructions field limit). If the live block changes, this file changes in the same release; neither is edited alone."~~ **STRUCK 18 October 2026 (KST).**
- ~~"Note: the deployed block reads "GRCnext™", which is the canonical form of the mark. Repository prose was standardized to the spaced form "GRC next™" at v1.1.0, moving the repository out of alignment with production. That standardization is reversed at v1.1.1 and the prose now matches the deployed block. No production change is required."~~ **STRUCK 18 October 2026 (KST).** The note is history: the mark has read GRCnext™ in both the block and the prose since 1.1.1.
- ~~"The production instruction block begins after this line."~~ **STRUCK 18 October 2026 (KST).**

From `README.md`:

- ~~"RedCap-01 is deployed as a Custom GPT; this repository mirrors the production deployment verbatim."~~ **STRUCK 18 October 2026 (KST).**
- ~~"RedCap-01 is live as a Custom GPT. The production configuration, mirrored verbatim in this repository, is:"~~ **STRUCK 18 October 2026 (KST).**
- ~~"**Instructions:** the block in [`RedCap-01-Custom-GPT.md`](RedCap-01-Custom-GPT.md), reproduced exactly as deployed"~~ **STRUCK 18 October 2026 (KST).**
- ~~"See [`BUILD.md`](BUILD.md) for the design rationale, configuration steps, testing approach and limitations."~~ **STRUCK 18 October 2026 (KST).**
- ~~"built and versioned on the same production-mirror discipline"~~ **STRUCK 18 October 2026 (KST).** (report 12, A19: no longer true)
- ~~"Overview, method and deployed configuration"~~ **STRUCK 18 October 2026 (KST).** and ~~"Production instruction block, mirrored verbatim"~~ **STRUCK 18 October 2026 (KST).** (repository map)
- ~~"**Status:** Production release, mirrored to the deployed Custom GPT, retiring 11 December 2026"~~ **STRUCK 18 October 2026 (KST).**
- The retirement notice, whole, **STRUCK 18 October 2026 (KST)** and replaced by the standard retirement line. Quoted verbatim in a code block because it carries its own 5 October 2026 strike:

```text
> **Retirement notice, 28 September 2026 (KST), corrected 5 October 2026 (KST).** OpenAI is retiring custom GPTs. Its [Custom GPT retirement and migration FAQ](https://help.openai.com/en/articles/20001519-custom-gpt-retirement-and-migration-faq), read on 28 September 2026, states that custom GPTs and their GPT pages become inaccessible on **11 December 2026**, or 11 February 2027 for Enterprise workspaces with an approved deferral. ~~The deployed RedCap-01 Custom GPT will be retired on that date and will not be migrated.~~ **STRUCK 5 October 2026 (KST):** the RedCap-01 Custom GPT was converted to a ChatGPT plugin on 1 October 2026, and the plugin is private and not publicly listed. The same FAQ, read again on 5 October 2026, states that a migrated GPT stays usable until retirement but becomes read-only. The RedCap-01 Custom GPT has no public link, so nothing else breaks.
>
> Everything needed to build your own stays published here: the instruction block and the configuration, including any knowledge files. OpenAI's replacement is the ChatGPT plugin, in which a GPT's instructions become a Skill and its knowledge files become reference files. Its [Plugins in ChatGPT and Codex](https://help.openai.com/en/articles/20001256-plugins-in-chatgpt-and-codex) article, read the same day, offers plugin creation in supported ChatGPT Business and Enterprise workspaces, so check what your plan allows. The instruction block is not tied to ChatGPT and also serves as the custom instructions of any assistant that accepts them. A plugin does not inherit a GPT's selected model and custom actions do not transfer, so choose the model yourself and test before you rely on the output.
```

From `BUILD.md`:

- ~~"**Status:** Production"~~ **STRUCK 18 October 2026 (KST).**
- ~~"6. Building and deploying the RedCap-01 Custom GPT."~~ **STRUCK 18 October 2026 (KST).** and ~~"7. Mirroring the deployed configuration in this repository (v1.1.0)."~~ **STRUCK 18 October 2026 (KST).**
- ~~"The deployed RedCap-01 Custom GPT is configured as follows. [`RedCap-01-Custom-GPT.md`](RedCap-01-Custom-GPT.md) mirrors the live instruction block verbatim."~~ **STRUCK 18 October 2026 (KST).**
- ~~"| Instructions | The block in `RedCap-01-Custom-GPT.md`, pasted exactly |"~~ **STRUCK 18 October 2026 (KST).**
- The GPT builder configuration steps, whole, **STRUCK 18 October 2026 (KST)** (report 12, B6), archived verbatim:

```text
1. Create a new Custom GPT in the GPT builder.
2. Set the name and description exactly as above.
3. Paste the instruction block from `RedCap-01-Custom-GPT.md` into the Instructions field. Paste only the block that follows the header divider; do not include this repository's header material.
4. Upload a lawfully obtained copy of *From Guidance to Action* to Knowledge. Add internal materials only if authorized and appropriately redacted.
5. Enable the capabilities listed above. Reduce the set if your deployment does not need them; fewer capabilities means a smaller surface.
6. Leave conversation starters empty to match production, or add your own; they do not change behavior.
7. Restrict sharing to the intended audience before publishing.
8. Test before first use (below).
```

- ~~"The repository and the deployed Custom GPT version together. A change to the live instruction block requires a repository release in the same cycle, and the reverse."~~ **STRUCK 18 October 2026 (KST).** (report 12, A5)

From `CONTRIBUTING.md`:

- ~~"Note that `RedCap-01-Custom-GPT.md` mirrors the deployed Custom GPT verbatim. Proposed changes to the instruction block are welcome as suggestions but are merged only together with a production update."~~ **STRUCK 18 October 2026 (KST).** (report 12, B7)

---

## [1.1.7] - 2026-10-17

Namespace, version-rule and count corrections. Session T3 of the whole-account review of 15 October 2026 (doc sections 1 and 8; reviewer report 12, items A3, A4, A11, B10, C2 and C8). No instruction block, template question or principle changes.

- **`DOCTRINE.md` renamed `PRINCIPLES.md`** (Michael's ruling 12 of 15 October 2026), so the account carries one file of that name, the canon at rolldabones/DOCTRINE.md. The title and the section heading read "Principles"; the doctrine citation line and a dated amendment note are added; the ten principles are unchanged word for word. The README repository map follows.
- **`VERSION.md` deleted into the README Status block.** STRUCK: ~~"README.md, BUILD.md, DOCTRINE.md, VERSION.md and RedCap-01-Custom-GPT.md move in lockstep."~~ It was false four ways: `VERSION.md` itself read 1.1.1 against a README at 1.1.6, releases 1.1.4 to 1.1.6 moved only the README and `CITATION.cff`, the account's lockstep set is README, How to Cite, `CITATION.cff`, CHANGELOG and tag, and the mirror file does not re-version with the repository. The Status block now states the account rule and which files keep their own version lines, and carries the compatibility list. STRUCK: the "Next planned enhancements" list, a roadmap nothing has been delivered against since July. RUNBOOK §8 item 25 closes with this release.
- **Count.** STRUCK: ~~"RedCap-01 examines eight connected capabilities."~~ The instruction block and the assessment template assess nine; the README's section 3, Assumptions and uncertainty, is split into 3, Assumptions, and 4, Uncertainty, as the block does, and sections 4 to 8 renumber to 5 to 9.
- **Status date.** STRUCK: ~~"Date: 30 July 2026"~~ under the 1.1.6 version line; the Status block now carries the release date, as the masthead does.
- **Closing line.** Added to `CONTRIBUTING.md`; in `Objective-Decision-Assessment.md` the four-line footer now precedes it, so it is last.
- README masthead, Status, How to Cite and `CITATION.cff` to 1.1.7 in lockstep. All other files unchanged byte for byte.

---

## [1.1.6] - 2026-10-05

Correction of substance to the retirement notice of the previous release. On 1 October 2026 the RedCap-01 Custom GPT was converted to a private ChatGPT plugin, so the notice's statement that it would not be migrated was false.

- **STRUCK, itemized separately:** the notice sentence "The deployed RedCap-01 Custom GPT will be retired on that date and will not be migrated." is struck in `README.md` and stays visible there. The entry below records the 28 September 2026 ruling that the GPT is not migrated to a plugin; it is shipped history and is unchanged, and that ruling is superseded by this entry.
- **What the notice now states:** the conversion to a private plugin on 1 October 2026 and, from OpenAI's Custom GPT retirement and migration FAQ as read again on 5 October 2026, that a migrated GPT stays usable until retirement but becomes read-only. The retirement date, 11 December 2026, is unchanged, so the Status block still reads "retiring 11 December 2026".
- **No link is affected:** the GPT has no public link. Recasting the present-tense deployment wording remains `account-maintenance` RUNBOOK §8 item 28, due on the first sweep on or after 14 December 2026. `VERSION.md` is untouched; RUNBOOK §8 item 25 rides a patch of its own.
- **Not re-verified:** OpenAI's Plugins in ChatGPT and Codex article returned a server error twice on 5 October 2026, so the notice's sentence on which workspaces can create plugins keeps its 28 September 2026 read date.
- **`CITATION.cff`**, the README version lines and How to Cite move to this release in lockstep. All other files in this repository are unchanged byte for byte.

## [1.1.5] - 2026-09-28

Retirement notice for the deployed custom GPT. OpenAI's Custom GPT retirement and migration FAQ, read on 28 September 2026, states that custom GPTs and their GPT pages become inaccessible on 11 December 2026. On Michael's ruling of 28 September 2026 the GPT is retired on that date and not migrated to a plugin; the instructions stay published so readers can build their own.

- **`README.md`**: retirement notice added under The deployed Custom GPT, and the Status block records the retirement date. The notice cites both OpenAI help articles with the date each was read. The version moved to this release at every occurrence.
- **`CITATION.cff`**: `version` and `date-released` in lockstep.
- **The present-tense deployment wording is kept.** It is true until 11 December 2026. Recasting it is `account-maintenance` RUNBOOK §8 item 28, due on the first sweep after that date.
- All other files in this repository are unchanged byte for byte.

## [1.1.4] - 2026-09-06

Citation infrastructure, doctrine citation line and lockstep maintenance. Session C of the September 2026 improvement pack, one patch release per repository across all 21 public repositories.

- **`CITATION.cff` added** in the house form settled at D-C1: no `type` field, `version` and `date-released` in lockstep with the README, `license` as the SPDX identifier for this repository's licence, `abstract` taken from this repository's ECOSYSTEM.md role line rather than newly written.
- **How to Cite block** aligned to this release and pointing at `CITATION.cff`.
- Both version occurrences bumped, the masthead and the closing block, per trap 6.
- All other files in this repository are unchanged byte for byte.

## [1.1.3] - 2026-08-13

Maintenance sweep. A second **Version:** block at README line 325 still read 1.1.1; the masthead had been bumped but this one had not. Found by the class C version-consistency check.

## [1.1.2] - 2026-08-13

Measurement and standards reframing.

- **Framing correction.** The instrument is now described explicitly as a **structured self-assessment**, not a measurement, benchmark, audit, certification or rating. Outputs are the organization's own answers organized against a defined structure and disciplined by an evidence rule. Structure makes answers comparable over time and arguable before a board; it does not make them independent. A score evidences the organization's position, it does not attest to it, and it must not be presented externally as though a third party had.
- RedCap-00 carries the corresponding change in its queue and is not edited here: it is a frozen production mirror and re-versions only on redeployment.


License metadata sweep. An `SPDX-License-Identifier: CC-BY-NC-SA-4.0` line and the canonical Creative Commons legal code are now carried inside the existing license file. The filename is unchanged and the human-readable summary is retained above the legal code.

- The primary audience is automated intake and provenance tooling, which reads the SPDX tag rather than prose. Automated license detection previously reported nothing across all twenty-one repositories in this account.
- No change to the licence in force. The identifier records what was already true.

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
