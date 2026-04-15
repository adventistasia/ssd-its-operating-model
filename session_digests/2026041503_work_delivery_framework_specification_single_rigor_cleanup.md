---
lorespec: "0.1"
id: "2026041503"
date: "2026-04-15"
source: "codex"
topic: "Removed work-size distinctions, collapsed review rigor, deleted Section 2.7, and renumbered the Work Delivery Framework specification"
tags: [work-delivery-framework, specification, review-model, renumbering, cleanup]
classification:
  type: "drafting"
  secondary_type: "technical"
  domains: [governance, documentation, review-process]
  value: "high"
trails: [work-delivery-framework-specification]
---

## Session Arc

### Started
The session began with detection of a stale `small-work` reference in the new framework specification and a request to remove it. The immediate focus was consistency with the already-decided removal of small-work handling from the document.

### Pivots
- The work moved from a single stale reference to a broader consistency review when the user asked whether the scaling model still made sense after removing small-work handling. That widened the scope from local cleanup to conceptual alignment. Source: "Is the scaling model still relevant since we've removed small work handling?" (Transcript L3-L3)
- The session then shifted from terminology cleanup to structural simplification when the user stated that the document should assume only one type of work and should not even mention that fact. Source: "there will only be no distinction made between large work and small work" (Transcript L9-L9)
- A second structural pivot happened when the user removed the distinction between substantive and quick-pass review, which forced a rewrite of Section 2.10 from dual modes to one review standard. Source: "there is only one standard review rigor" (Transcript L13-L13)
- The final pivot was to remove Section 2.7 entirely and then repair the numbering gap across the rest of Section 2. Source: "we can now remove section 2.7 and any references to it" (Transcript L15-L15) and "Fix the gap by renumbering as needed." (Transcript L17-L17)

### Ended
The session ended with the specification updated to remove work-size distinctions, remove dual review modes, delete Section 2.7, and renumber later sections so Section 2 is contiguous again. A remaining wording inconsistency about lower/higher-complexity phrasing was noted but not resolved in this session. Source: "One leftover inconsistency still exists in prose" (Transcript L18-L18)

## ARTIFACT

### A1
- Artifact: Updated `work_delivery_framework/work_delivery_framework_specification.md`.
- Summary: The artifact was revised in multiple passes to remove `small-work` / `large-work` handling, remove edge-case scenarios 5.6 and 5.7, collapse Section 2.10 into a single gate review standard, delete Section 2.7 entirely, and renumber downstream sections from former `2.8`-`2.14` to current `2.7`-`2.13`.
- Evolution:
  - Initial cleanup removed stale `small-work` review wording.
  - Follow-up cleanup removed size-bucket framing from scenario and implementation language.
  - Review-model refactor removed substantive/quick-pass distinctions.
  - Final structural cleanup deleted Section 2.7 and repaired section numbering.
- Source: "Updated ... to remove the obsolete `Small-work` / `Large-work` handling." (Transcript L2-L2)
- Source: "Removed Sections 5.6 and 5.7" (Transcript L8-L8)
- Source: "Updated Section 2.10 ... to use a single review standard." (Transcript L14-L14)
- Source: "Removed the entire `2.7` section" (Transcript L16-L16)
- Source: "Renumbered the gap so Section 2 is contiguous again" (Transcript L18-L18)

## DECISION

### D1
- Decision: Remove all distinctions between small work and large work from the specification, and avoid explicitly stating that the framework has only one work type.
- Issue: Whether the document should preserve any explicit framing around work-size categories after small-work handling was removed.
- Positions:
  - Keep some explicit "one type of work" or one-path language.
  - Remove work-size distinctions and avoid even stating the singularity explicitly.
- Arguments:
  - The user rejected any lingering framing around large vs small work.
  - Explicit "one type" statements were considered unnecessary and undesirable because they still foreground a distinction the document is meant to discard.
- Warrant: If a distinction is no longer part of the operating model, the specification should stop naming it, not merely invert it into a "single type" doctrine.
- Qualifier: for this specification revision
- Status: settled
- Source: "there will only be no distinction made between large work and small work" (Transcript L9-L9)
- Source: "This does not even need to be mentioned in the document." (Transcript L9-L9)

### D2
- Decision: Replace the dual review-mode model in Section 2.10 with a single gate review rigor and a generic review meeting model.
- Issue: Whether Section 2.10 should retain substantive vs quick-pass review distinctions after the framework was simplified.
- Positions:
  - Keep substantive and quick-pass as separate review modes.
  - Use one standard review rigor for all gate reviews.
- Arguments:
  - The user explicitly stated there is only one standard review rigor.
  - Keeping dual review modes would preserve a distinction the user no longer wanted in the framework.
  - A single review meeting model aligns better with the simplified control model.
- Warrant: When the governance model no longer recognizes multiple review rigor classes, the review section should encode one review standard and express variation only through triggered participants/signoffs, not alternate modes.
- Qualifier: within Section 2.10
- Status: settled
- Source: "there is only one standard review rigor" (Transcript L13-L13)
- Source: "there is no longer to make a distinction between substantive and quick-pass review mode" (Transcript L13-L13)
- Source: "There should also no longer a substantive review meeting model but rather just a review meeting model" (Transcript L13-L13)

### D3
- Decision: Delete Section 2.7 and remove its references rather than preserving it as a separate scaling section.
- Issue: Whether the specification still needed a dedicated scaling section after work-type distinctions and separate review rigor modes were removed.
- Positions:
  - Retain a renamed or reduced Section 2.7.
  - Remove Section 2.7 entirely and fold any necessary proportionality language into local sections.
- Arguments:
  - The user explicitly directed removal of Section 2.7 and its references.
  - Once work-type and review-mode distinctions were removed, the dedicated section became unnecessary overhead.
  - Remaining local sections could carry any still-needed proportionality wording directly.
- Warrant: If a control concept no longer needs to exist as a standalone framework mechanism, keeping a separate section for it adds structural weight without governance value.
- Qualifier: in this revision cycle
- Status: settled
- Source: "we can now remove section 2.7 and any references to it." (Transcript L15-L15)

### D4
- Decision: Renumber all later Section 2 headings and references to close the numbering gap left by deleting Section 2.7.
- Issue: Whether to leave a numbering gap after deleting Section 2.7 or repair the numbering.
- Positions:
  - Leave the gap as a narrow deletion artifact.
  - Renumber subsequent sections and internal references.
- Arguments:
  - The user explicitly asked to fix the gap.
  - A contiguous numbering sequence is easier to navigate and less likely to confuse future editing or review.
- Warrant: Structural deletions in a normative specification should be followed by numbering repair when continuity and navigability matter more than preserving transient editorial history.
- Qualifier: for the current document version
- Status: settled
- Source: "Fix the gap by renumbering as needed." (Transcript L17-L17)

## INSIGHT

### I1
- Insight: In this specification, simplification was not just wording cleanup; it required cascading removal of dependent control concepts, headings, and cross-references.
- Domain: documentation governance
- Confidence: high
- Source: The session progressed from one stale `small-work` reference to review-model simplification, full section deletion, and renumbering. Source excerpts: "yes do the cleanup pass." (Transcript L5-L5) and "we can now remove section 2.7 and any references to it." (Transcript L15-L15)

### I2
- Insight: The document still contains at least one unresolved phrasing inconsistency around complexity-based language after the structural cleanup.
- Domain: specification hygiene
- Confidence: high
- Source: "One leftover inconsistency still exists in prose" (Transcript L18-L18)

## PATTERN

### P1
- Pattern: Simplify a normative specification by removing obsolete distinctions in dependency order.
- Scope: local
- Steps/components:
  1. Remove the first stale reference that reveals the obsolete distinction.
  2. Audit the broader document for conceptual dependencies on that distinction.
  3. Remove scenario/examples that keep the old framing alive.
  4. Collapse any operational models that still encode the distinction.
  5. Delete now-redundant top-level sections.
  6. Renumber headings and patch internal references last.
- Why it mattered here: This prevented the document from ending up in a half-simplified state where obsolete concepts were deleted locally but still encoded structurally elsewhere.
- Source: The session followed this sequence from stale reference cleanup through Section 2.10 rewrite, Section 2.7 deletion, and renumbering. Source excerpt: "remove the whole 2.7 block and normalize the remaining headings/text" (Transcript L16-L16)

## OPEN_QUESTION

### OQ1
- Question: Should the remaining "lower-complexity" / "higher-complexity" phrasing in the acceptance-criteria section be removed to fully align with the no-work-type-distinction rule?
- Why unresolved: The inconsistency was identified after renumbering, but the user asked for a session digest rather than another cleanup pass.
- Partial progress: The assistant explicitly flagged the remaining inconsistency and localized it to prose in the acceptance-criteria section.
- Source: "One leftover inconsistency still exists in prose" (Transcript L18-L18)

## NEXT_STEP

### NS1
- What: Perform a final terminology cleanup pass to remove any remaining lower/higher-complexity phrasing that could be read as a reintroduced work classification.
- Prompted by: The unresolved inconsistency noted after renumbering.
- Urgency: soon
- Source: "it may still conflict with your 'no work-type distinction' direction" (Transcript L18-L18)

## Connections

D1 --[led_to]--> A1
D1 --[led_to]--> D2
D2 --[led_to]--> A1
D2 --[led_to]--> D3
D3 --[led_to]--> D4
D4 --[led_to]--> A1
A1 --[informed_by]--> I1
I2 --[led_to]--> OQ1
OQ1 --[led_to]--> NS1
P1 --[instance_of]--> A1

## Trail Updates

- Extends `work-delivery-framework-specification`.
- Related prior digests:
  - `2026041401_remove_small_work_path_from_new_framework.md`
  - `2026041502_governing_spec_review_of_work_delivery_framework_specification.md`
- This session advances the trail from identifying and removing the small-work path to removing the remaining structural dependencies that still encoded work-size or review-rigor distinctions.
