# Work Delivery Framework Governing Spec Refactor Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Refactor `work_delivery_framework/work_delivery_framework_specification.md` into a true canonical governing specification that satisfies the findings in `work_delivery_framework/work_delivery_framework_governing_spec_review_report.md` while preserving the framework's valid lifecycle and artifact content.

**Architecture:** Treat the work as a controlled documentation refactor with one primary source file, one review report, and one design doc. Reframe governance and publication semantics first, then update artifact-boundary language, replace editorial patch language with final-state normative text, and finish with a conformance-focused consistency review.

**Tech Stack:** Markdown, fenced YAML, `rg`, `git`, repository documentation conventions

---

## File Structure

- Modify: `work_delivery_framework/work_delivery_framework_specification.md`
- Reference: `work_delivery_framework/work_delivery_framework_governing_spec_review_report.md`
- Reference: `docs/superpowers/specs/2026-04-16-work-delivery-framework-governing-spec-refactor-design.md`
- Create: `session_digests/` update only if the user later asks for a session digest

The refactor should stay inside the existing specification file. Do not create a second source specification or a parallel framework-definition file. Preserve all stable IDs unless the plan explicitly says otherwise.

### Task 1: Baseline the Governing-Spec Gaps

**Files:**
- Modify: `work_delivery_framework/work_delivery_framework_specification.md`
- Reference: `work_delivery_framework/work_delivery_framework_governing_spec_review_report.md`
- Reference: `docs/superpowers/specs/2026-04-16-work-delivery-framework-governing-spec-refactor-design.md`

- [ ] **Step 1: Re-read the current opening, artifact-boundary, editorial-YAML, and closing-conformance sections**

Run:

```bash
rg -n "## 1\.|### 1\.2|### 2\.5|#### 2\.7\.4|#### 2\.8\.3|## 4\.|## 5\.|## 6\." work_delivery_framework/work_delivery_framework_specification.md
```

Expected: line hits for the exact sections the review report identified as requiring governance-focused rewrite.

- [ ] **Step 2: Reconfirm the mandatory rewrite outcomes from the review report**

Read these outcomes and restate them in working notes before editing:

```text
1. Separate canonical specification from authoritative framework release.
2. Define derivation, publication, validation, precedence, versioning, supersession, and change control.
3. Distinguish framework-publication artifacts from initiative artifacts.
4. Rewrite editorial patch language as final-state normative content.
5. Explicitly classify Sections 4-6.
```

Expected: a short working checklist exists in the agent's notes or scratchpad before the first edit.

- [ ] **Step 3: Verify the current file has no hidden secondary publication model elsewhere**

Run:

```bash
rg -n "authoritative framework|operating pack|publication set|supersed|deprecat|canonical specification|source of truth" work_delivery_framework/work_delivery_framework_specification.md
```

Expected: little or no current coverage of the needed governance model, confirming that a front-loaded rewrite is required rather than scattered wording tweaks.

- [ ] **Step 4: Commit the baseline-readiness checkpoint**

```bash
git add docs/superpowers/plans/2026-04-16-work-delivery-framework-governing-spec-refactor.md
git commit -m "docs: add governing spec refactor plan"
```

Expected: a commit exists containing the implementation plan before source-document editing begins.

### Task 2: Reframe the Top of the Specification Around Governance

**Files:**
- Modify: `work_delivery_framework/work_delivery_framework_specification.md:1-125`
- Reference: `work_delivery_framework/work_delivery_framework_governing_spec_review_report.md:38-124`

- [ ] **Step 1: Replace opening language that presents the file as the framework itself**

Update the top of the file so the opening follows this structure:

```md
# Work Delivery Framework Governing Specification

## 1. Governing Specification Overview

This document is the canonical governing specification for the Work Delivery Framework.

It defines the normative content, stable identifiers, authority model, publication rules, and maintenance rules for the framework.

The authoritative Work Delivery Framework is an approved published release derived from this specification.
```

Expected: the document title and opening paragraphs identify the file as the canonical specification and define the release as a derivative.

- [ ] **Step 2: Rewrite Section `1.2` so it defines form and publication model without collapsing source and release**

Replace the current `1.2` framing with final-state content that covers:

```text
1. Canonical source: this file.
2. Authoritative release: approved derivative publication.
3. Derived operating pack: usability-oriented derivative.
4. Supporting artifacts: templates, examples, checklists, exports.
5. Lower-ranked artifacts must conform and cannot weaken higher-ranked artifacts.
```

Expected: Section `1.2` becomes a governing-source section rather than operating-model marketing language.

- [ ] **Step 3: Preserve the machine-consumable requirement, but tie it to publication derivation**

Keep the existing YAML-first requirement, but rewrite the surrounding prose to say that embedded YAML blocks are the canonical machine-consumable source from which faithful derivatives and release outputs are produced.

Expected: YAML remains required, but its role is clearly connected to publication and validation.

- [ ] **Step 4: Verify the top-of-file terminology after editing**

Run:

```bash
rg -n "This framework is|authoritative operating model definition|canonical source of truth|approved derivative publication|canonical governing specification" work_delivery_framework/work_delivery_framework_specification.md
```

Expected: legacy source/framework conflation language is removed or intentionally replaced by the new governance terms.

- [ ] **Step 5: Commit the governance-front-matter rewrite**

```bash
git add work_delivery_framework/work_delivery_framework_specification.md
git commit -m "docs: reframe work delivery spec as governing source"
```

Expected: the first substantive source-file commit isolates the top-of-document authority rewrite.

### Task 3: Add the Framework Publication, Authority, and Maintenance Model

**Files:**
- Modify: `work_delivery_framework/work_delivery_framework_specification.md` immediately after Section `1.2`
- Reference: `work_delivery_framework/work_delivery_framework_governing_spec_review_report.md:64-124`

- [ ] **Step 1: Insert a new early section for publication, authority, and maintenance**

Create a new section with subsections covering:

```md
### 1.x Artifact classes and definitions
### 1.x Authority hierarchy and precedence
### 1.x Required derivative classes and authoritative release set
### 1.x Publication metadata and validation requirements
### 1.x Versioning, identifier stability, and compatibility
### 1.x Change control, supersession, and archival
```

Expected: the document contains one obvious governance section that answers the report's critical derivation and maintenance concerns.

- [ ] **Step 2: Define the authoritative release as a minimum publication set**

Include explicit final-state rules similar to this content:

```text
An authoritative Work Delivery Framework release MUST include:
1. the release identifier and publication date
2. the source specification version and reference
3. the normative framework publication or assembled pack
4. faithful machine-readable exports derived from canonical YAML
5. a manifest listing included derivative artifacts and their normative status
```

Expected: a worker can derive the authoritative release set without inventing what counts as a valid publication.

- [ ] **Step 3: Define conflict and validation rules**

Add explicit rules that:

```text
1. the canonical specification prevails on conflict
2. derivative artifacts must preserve stable IDs and semantic meaning
3. publication requires validation of completeness, ID fidelity, and semantic equivalence
4. every release must declare the source-spec version it was derived from
```

Expected: publication conformance is auditable rather than implied.

- [ ] **Step 4: Define change-control and maintenance rules**

Add final-state governance rules covering:

```text
1. who proposes changes
2. who approves changes
3. how versions are assigned
4. when ID changes are allowed
5. when derivative releases must be regenerated
6. how superseded releases remain referenceable
```

Expected: the document governs future framework changes, not only the present content.

- [ ] **Step 5: Verify that the new section closes the report's critical governance gaps**

Run:

```bash
rg -n "authority hierarchy|authoritative Work Delivery Framework release|derived operating pack|validation|supersed|identifier stability|change control|publication metadata" work_delivery_framework/work_delivery_framework_specification.md
```

Expected: each governance concept appears explicitly in the new section.

- [ ] **Step 6: Commit the publication-model section**

```bash
git add work_delivery_framework/work_delivery_framework_specification.md
git commit -m "docs: add framework publication and maintenance model"
```

Expected: the governance model is isolated in its own commit.

### Task 4: Clarify Initiative Artifacts Versus Framework-Publication Artifacts

**Files:**
- Modify: `work_delivery_framework/work_delivery_framework_specification.md:471-523`
- Reference: `work_delivery_framework/work_delivery_framework_governing_spec_review_report.md:149-177`

- [ ] **Step 1: Add an explicit boundary statement at the start of Section `2.5`**

Insert a short paragraph directly under `### 2.5 Required artifact taxonomy` using wording equivalent to:

```md
This section defines initiative-level artifacts produced by projects operating under the Work Delivery Framework. It does not define the publication set used to publish or govern the framework itself.
```

Expected: readers can no longer confuse project artifacts with framework-release artifacts.

- [ ] **Step 2: Add a brief note cross-referencing the new governance/publication section**

Add a sentence that points readers to the early publication-and-authority section for the framework's own publication artifacts.

Expected: the layer separation is structural, not just semantic.

- [ ] **Step 3: Keep the existing initiative artifact taxonomy materially intact**

Do not rename artifact IDs or triggers unless required for consistency with the new authority model. Preserve the current taxonomy substance.

Expected: the refactor corrects governance layering without disturbing valid initiative-level logic.

- [ ] **Step 4: Verify the section contains both boundary and continuity language**

Run:

```bash
rg -n "initiative-level artifacts|framework itself|publication set|Section 1\.|authoritative release" work_delivery_framework/work_delivery_framework_specification.md
```

Expected: Section `2.5` explicitly distinguishes the layers and points to the governing section.

- [ ] **Step 5: Commit the artifact-layer clarification**

```bash
git add work_delivery_framework/work_delivery_framework_specification.md
git commit -m "docs: separate initiative artifacts from framework publication artifacts"
```

Expected: the artifact-boundary rewrite is isolated and reviewable.

### Task 5: Rewrite Section `2.7.4` as Final-State Normative Content

**Files:**
- Modify: `work_delivery_framework/work_delivery_framework_specification.md:1040-1068`
- Reference: `work_delivery_framework/work_delivery_framework_governing_spec_review_report.md:126-148`

- [ ] **Step 1: Remove all editorial patch language from Section `2.7.4`**

Delete wording such as `Add/update the following in existing YAML blocks` and `Update GATE-SPECIFICATION-COMPLETE and GATE-DELIVERABLES-ACCEPTED YAML`.

Expected: the section reads like canonical source content, not instructions to an editor.

- [ ] **Step 2: Present the acceptance-criteria artifact as final-state canonical YAML**

Retain the current artifact semantics, but frame the YAML as the canonical artifact definition. The section should begin with wording equivalent to:

```md
The canonical machine-consumable model includes the following artifact definition:
```

Expected: the artifact definition is directly usable as source material.

- [ ] **Step 3: Present the impacted gate requirements as final-state normative gate content**

Write complete gate fragments or complete gate blocks for `GATE-SPECIFICATION-COMPLETE` and `GATE-DELIVERABLES-ACCEPTED` instead of prose instructions. Include the acceptance-quality requirement directly in the gate definition.

Expected: a downstream worker no longer has to infer how to merge updates into the gate model.

- [ ] **Step 4: Verify no editorial verbs remain in the section**

Run:

```bash
rg -n "Add/update|Add to|Update GATE|existing YAML blocks" work_delivery_framework/work_delivery_framework_specification.md
```

Expected: no hits remain in Section `2.7.4` or nearby normative YAML update sections.

- [ ] **Step 5: Commit the acceptance-criteria YAML rewrite**

```bash
git add work_delivery_framework/work_delivery_framework_specification.md
git commit -m "docs: rewrite acceptance criteria YAML as final-state source"
```

Expected: Section `2.7.4` is captured in a dedicated commit.

### Task 6: Rewrite Section `2.8.3` as Final-State Normative Content

**Files:**
- Modify: `work_delivery_framework/work_delivery_framework_specification.md:1122-1154`
- Reference: `work_delivery_framework/work_delivery_framework_governing_spec_review_report.md:126-148`

- [ ] **Step 1: Remove editorial instructions from Section `2.8.3`**

Delete wording such as `Add to ARTIFACT-DEPLOYMENT-GUIDE and ARTIFACT-TDD required_contents` and `Update GATE-TRANSITION-COMPLETE`.

Expected: the section stops reading like a patch note.

- [ ] **Step 2: Replace the prose instructions with final-state artifact content requirements**

Write direct normative statements that the canonical `ARTIFACT-DEPLOYMENT-GUIDE` and `ARTIFACT-TDD` definitions include support ownership, observability, maintainability commitments, and transition-checklist content where applicable.

Expected: the required state is visible without an edit operation being implied.

- [ ] **Step 3: Replace the gate update snippet with a final-state gate definition or final-state mandatory conditions block**

Use wording or YAML that directly states the required `GATE-TRANSITION-COMPLETE` conditions.

Expected: gate semantics are fully defined in-source.

- [ ] **Step 4: Keep the example snippet explicitly non-authoritative if retained**

If the deployment-guide example remains, label it as an example or illustrative derivative, not a normative source artifact.

Expected: examples cannot be mistaken for canonical source definitions.

- [ ] **Step 5: Verify the rewritten section uses final-state language only**

Run:

```bash
rg -n "Add to ARTIFACT|Update GATE|Updated YAML for artifacts/gates|final-state|illustrative" work_delivery_framework/work_delivery_framework_specification.md
```

Expected: editorial instructions are gone and any retained example is clearly labeled.

- [ ] **Step 6: Commit the supportability YAML rewrite**

```bash
git add work_delivery_framework/work_delivery_framework_specification.md
git commit -m "docs: rewrite supportability YAML as final-state source"
```

Expected: Section `2.8.3` is isolated in its own commit.

### Task 7: Reclassify Sections `4` to `6` So Their Status Is Explicit

**Files:**
- Modify: `work_delivery_framework/work_delivery_framework_specification.md:1921-2075`
- Reference: `work_delivery_framework/work_delivery_framework_governing_spec_review_report.md:178-222`

- [ ] **Step 1: Choose one classification model and apply it consistently**

Use this recommended model:

```text
1. Section 4: Normative conformance and operating-boundary constraints.
2. Section 5: Normative conformance scenarios.
3. Section 6: Normative implementation constraints or a clearly labeled non-normative appendix.
```

Expected: no section remains in an ambiguous middle state.

- [ ] **Step 2: Rewrite each section preamble so its normative status is explicit**

Examples of acceptable lead-in language:

```md
This section defines normative conformance boundaries for application of the framework.
This section defines normative conformance scenarios used to evaluate whether the framework produces the required outcomes.
This appendix is non-normative and provides explanatory implementation constraints.
```

Expected: a reader can tell from the heading and first paragraph how to treat each section.

- [ ] **Step 3: Align headings with the chosen classification**

Rename section headings if needed so the status is obvious from the table of contents alone.

Expected: headings and preambles reinforce the same interpretation.

- [ ] **Step 4: Verify that the closing sections now have explicit normative status markers**

Run:

```bash
rg -n "normative conformance|non-normative appendix|operating-boundary|conformance scenarios|implementation constraints" work_delivery_framework/work_delivery_framework_specification.md
```

Expected: Sections `4` to `6` each have explicit status language.

- [ ] **Step 5: Commit the section-role cleanup**

```bash
git add work_delivery_framework/work_delivery_framework_specification.md
git commit -m "docs: classify governing spec conformance sections"
```

Expected: the classification change is reviewable in one commit.

### Task 8: Run a Full Consistency and Acceptance Pass

**Files:**
- Modify: `work_delivery_framework/work_delivery_framework_specification.md`
- Reference: `work_delivery_framework/work_delivery_framework_governing_spec_review_report.md`
- Reference: `docs/superpowers/specs/2026-04-16-work-delivery-framework-governing-spec-refactor-design.md`

- [ ] **Step 1: Search for leftover conflation and patch-language terms**

Run:

```bash
rg -n "This framework is a full operating model|authoritative operating model definition|Add/update|Add to|Update GATE|shadow taxonomies|source of truth" work_delivery_framework/work_delivery_framework_specification.md
```

Expected: no outdated governing-language or editorial-patch phrasing remains except where intentionally replaced by new canonical terms.

- [ ] **Step 2: Search for the required governance vocabulary**

Run:

```bash
rg -n "canonical governing specification|authoritative Work Delivery Framework release|derived operating pack|supporting artifacts|publication metadata|semantic equivalence|identifier stability|superseded releases|change control" work_delivery_framework/work_delivery_framework_specification.md
```

Expected: the required governance model is now visibly present in the file.

- [ ] **Step 3: Manually review the opening, new governance section, `2.5`, `2.7.4`, `2.8.3`, and Sections `4-6` together**

Read those sections in sequence and confirm all of the following:

```text
1. The file is clearly the canonical specification.
2. The authoritative release is clearly a derivative publication.
3. Initiative artifacts are distinct from framework-publication artifacts.
4. Normative YAML sections state end-state content, not edits.
5. Conformance sections are explicitly classified.
```

Expected: no cross-section contradiction is visible after the major refactor waves.

- [ ] **Step 4: Run a git diff and inspect for accidental semantic drift**

Run:

```bash
git diff -- work_delivery_framework/work_delivery_framework_specification.md
```

Expected: changes are concentrated in the targeted governance sections and preserve lifecycle/artifact substance unless changed for a stated governance reason.

- [ ] **Step 5: Make any final consistency edits and commit**

```bash
git add work_delivery_framework/work_delivery_framework_specification.md
git commit -m "docs: finalize governing specification refactor"
```

Expected: the final commit contains only consistency corrections after the main rewrite tasks are complete.

### Task 9: Final Verification and Handoff

**Files:**
- Modify: none unless fixes are needed after verification

- [ ] **Step 1: Run the final acceptance-check command set**

Run:

```bash
rg -n "canonical governing specification|authoritative Work Delivery Framework release|derived operating pack|supporting artifacts" work_delivery_framework/work_delivery_framework_specification.md
rg -n "initiative-level artifacts|publication set used to publish or govern the framework itself" work_delivery_framework/work_delivery_framework_specification.md
rg -n "Add/update|Add to|Update GATE|existing YAML blocks" work_delivery_framework/work_delivery_framework_specification.md
rg -n "normative conformance|non-normative appendix|conformance scenarios" work_delivery_framework/work_delivery_framework_specification.md
```

Expected: required governance language is present, prohibited editorial language is absent, and section classification language is present.

- [ ] **Step 2: Summarize the outcome against the design acceptance criteria**

Produce a short handoff note covering:

```text
1. how the source/release distinction is now expressed
2. where publication and maintenance rules live
3. where artifact-layer boundaries are defined
4. where final-state YAML rewrites were applied
5. how Sections 4-6 were classified
```

Expected: the user receives a traceable map from the review report to the implemented refactor.

- [ ] **Step 3: Leave the repo ready for user review**

Run:

```bash
git status
```

Expected: either a clean working tree or only the intended documentation changes remain.
