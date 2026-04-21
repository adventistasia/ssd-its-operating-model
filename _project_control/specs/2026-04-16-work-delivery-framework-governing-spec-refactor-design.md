# Work Delivery Framework Governing Specification Refactor Design

## Purpose

Refactor `work_delivery_framework/work_delivery_framework_specification.md` so it functions unambiguously as the canonical governing specification for the Work Delivery Framework rather than reading as though it is the framework release itself.

The refactor must preserve valid framework content that already defines initiative lifecycle, gates, artifacts, completeness controls, and review rigor, while correcting authority, publication, maintenance, and conformance gaps identified in `work_delivery_framework/work_delivery_framework_governing_spec_review_report.md`.

## Design Goals

1. Establish a clean authority hierarchy between the canonical specification, authoritative framework release, derived operating pack, and supporting artifacts.
2. Make the authoritative framework derivable without interpretive governance decisions.
3. Define publication, validation, versioning, supersession, and change-control rules for the framework as a governed asset.
4. Preserve strong existing lifecycle and artifact-definition content wherever it is already substantively correct.
5. Replace editorial amendment instructions with final-state normative requirements.

## Non-Goals

1. Re-design the initiative lifecycle.
2. Re-invent the existing artifact taxonomy unless needed to clarify governance-layer boundaries.
3. Introduce a separate permanent source document unless the existing file cannot support the governing-spec role.
4. Create a new broader documentation architecture beyond what is needed to satisfy the governing-spec review.

## Recommended Refactor Approach

Use a full governing-spec refactor that preserves core framework substance.

This approach restructures the document around governance first, then retains and relabels the existing normative framework-definition material. It avoids a risky clean-sheet rewrite while still making the authority and publication model explicit.

## Target Document Shape

### 1. Governance-first front matter

Reframe the opening so the document states that it specifies the Work Delivery Framework rather than presenting itself as the framework object.

Section 1 should explicitly define:

1. the file as the canonical governing specification
2. the authoritative Work Delivery Framework release as an approved derivative publication
3. the document's scope and applicability
4. the fact that the specification governs both framework content and framework publication

### 2. Framework publication, authority, and maintenance model

Add a dedicated early section that defines:

1. artifact classes
2. authority ranking and precedence
3. required derivative classes
4. the minimum authoritative release publication set
5. required machine-readable outputs
6. publication metadata requirements
7. validation checks before publication
8. conflict resolution rules
9. versioning, supersession, archival, and change-control rules
10. identifier stability and compatibility rules

This section is the main correction for the review report's critical governance findings.

### 3. Normative framework-definition content

Retain the current lifecycle, gates, artifact taxonomy, completeness model, acceptance-quality model, supportability model, review model, and anti-bureaucracy controls as normative framework-definition content, but ensure the wording makes clear that these are requirements defined by the canonical specification.

This keeps the strong current material while removing source/framework conflation.

### 4. Explicit layer boundary in artifact sections

The artifact taxonomy section must distinguish:

1. initiative artifacts produced under the framework
2. framework-publication artifacts used to publish the framework itself
3. supporting derivatives such as templates, examples, checklists, and machine-readable exports

The initiative artifact taxonomy remains intact, but the section must state that it does not define the authoritative framework release publication set.

### 5. Final-state normative YAML

Sections `2.7.4` and `2.8.3` must be rewritten as final-state canonical definitions.

The spec should directly state the required artifact and gate content rather than telling the reader to add or update YAML in place. The final-state content should read as complete normative source material suitable for direct derivation into published artifacts and exports.

### 6. Explicit classification of Sections 4-6

Sections `4` to `6` must not remain ambiguously framed.

Recommended treatment:

1. keep Section `4` as normative conformance and operating-boundary material if it is still needed for external constraints on framework application
2. keep Section `5` as normative conformance scenarios if those scenarios are intended to test whether the framework behaves correctly in practice
3. move Section `6` into an explicit conformance or implementation-constraint classification, or into a non-normative appendix if it merely restates design intent

The final edit should choose one treatment and label it plainly.

## Proposed Rewrite Waves

### Wave 1: Authority and publication model

1. Rewrite the title/overview framing.
2. Replace current Section `1.2` with governance-source framing.
3. Insert the framework publication, authority, and maintenance model.

### Wave 2: Layer boundaries and artifact-model cleanup

1. Update Section `2.5` to distinguish initiative artifacts from framework-publication artifacts.
2. Preserve current initiative artifact content unless a governance clarification requires wording changes.

### Wave 3: Final-state normative rewrites

1. Rewrite Section `2.7.4` as final-state artifact and gate YAML.
2. Rewrite Section `2.8.3` as final-state artifact and gate YAML.

### Wave 4: Section-role cleanup

1. Reclassify Sections `4` to `6` explicitly.
2. Adjust headings and short preambles so their normative status is obvious.

### Wave 5: Consistency pass

1. Verify terminology is consistent across the document.
2. Verify all references to authority, release, derivative, template, export, and precedence follow the new hierarchy.
3. Verify no editorial patch language remains in normative source sections.

## Acceptance Criteria

The refactored specification is acceptable when:

1. a reader can identify the canonical specification without inference
2. a reader can identify the authoritative framework release without inference
3. a worker can derive the authoritative publication set without inventing governance rules
4. a maintainer can determine how changes are approved, versioned, published, regenerated, validated, and superseded
5. a reviewer can distinguish canonical, authoritative, derived, and supportive materials
6. no normative section relies on editorial patch instructions instead of final-state requirements
7. the existing valid lifecycle and artifact logic remain materially intact unless changed for a stated governance reason

## Risks and Controls

### Risk: over-rewrite

Because this is a full refactor, the main risk is replacing too much valid content at once.

Control: preserve existing lifecycle and artifact substance wherever the issue is framing rather than logic.

### Risk: accidental semantic drift

A large structural rewrite can subtly change framework meaning.

Control: anchor edits to the review report findings and run a consistency pass focused on IDs, gates, artifact intent, and authority language.

### Risk: unresolved status of Sections 4-6

If those sections are only renamed but not clearly classified, the core ambiguity remains.

Control: make an explicit normative versus non-normative decision and reflect it in headings and opening sentences.

## Execution Notes

The implementation should proceed as a structured documentation refactor, not as incremental wording tweaks scattered through the file. Large structural edits are appropriate, but they should be traceable to the review report's findings and the rewrite waves above.
