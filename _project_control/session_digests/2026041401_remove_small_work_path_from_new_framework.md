---
lorespec: "0.1"
id: "2026041401"
date: "2026-04-14"
source: "codex"
topic: "Removed small-work handling from the new Work Delivery Framework specification"
tags: [work-delivery-framework, specification, scaling, scope, small-work-removal, lore]
classification:
  type: "drafting"
  secondary_type: "operational"
  domains: [framework-design, delivery-readiness, governance]
  value: "high"
trails: [work-delivery-framework]
---

## Session Arc

### Started
The session began with the user asking for a vague request to be restructured into a brief and then executed. The substantive request was to "Cleanly remove the handling of small-work" because the specification should "only handle planned software initiatives." Source: "Transform my request into a structured brief, then execute it." and "Cleanly remove the handling of small-work. The specification will only handle planned software initiatives." (Transcript L1-L1)

### Pivots
- The first pivot converted the request into a scoped framework-editing task and isolated the question of repository scope: update only the new framework or also the legacy `work_delivery/` docs. Source: "should I limit this to the new framework file in `work_delivery_framework/`, or also update the older `work_delivery/` documents" (Transcript L2-L2)
- The second pivot settled scope when the user chose `1`, meaning only the new framework file would change. Source: "1" (Transcript L3-L3)
- The third pivot settled the editing approach: remove small-work and Work Brief handling, keep one initiative definition path, and rewrite scaling as proportionate rigor inside planned software initiatives. Source: "approve" after the design summary that proposed removing `small-work` / `large-work` classification and the `Work Brief` path. (Transcript L5-L5)
- The fourth pivot extended the session from implementation into repository hygiene when the user requested a session digest and a commit. Source: "create a session digest then commit the changes." (Transcript L6-L6)

### Ended
The session ended with the new framework specification edited to remove small-work handling, a fresh session digest added under `session_digests/`, and the work prepared for a single commit that captures both artifacts. Source: "Updated `work_delivery_framework/work_delivery_framework_specification.md` to remove small-work handling from the new framework." and the subsequent request to create a digest and commit. (Transcript L7-L8)

## ARTIFACT

### A1
- Artifact: Updated `work_delivery_framework/work_delivery_framework_specification.md`.
- Final state: The specification now defines the framework for planned software initiatives only, removes the `Work Brief` artifact and all `small-work` / `large-work` classification logic, replaces the dual-path packaging model with one `Initiative Definition / Project Brief`, and rewrites scaling as proportionate rigor within a single initiative path.
- Evolution: The change started as a request to remove small-work handling generally, then was narrowed by user choice to the new framework file only rather than the legacy `work_delivery/` documents.
- Source: "Remove small-work handling from the new framework spec so it governs only planned software initiatives" and the later verification summary that no `small-work`, `large-work`, `Work Brief`, or `ARTIFACT-WORK-BRIEF` references remained in the file. (Transcript L4-L5, L7-L7)

### A2
- Artifact: Added `session_digests/2026041401_remove_small_work_path_from_new_framework.md`.
- Final state: The digest records the scope choice, the settled framework-model change, the specific implementation direction, and the requirement to commit the work.
- Evolution: The digest was requested only after the specification edit and verification pass were complete.
- Source: "create a session digest then commit the changes." (Transcript L6-L6)

## DECISION

### D1
- Decision: Limit the change scope to `work_delivery_framework/work_delivery_framework_specification.md` and do not update legacy `work_delivery/` docs in this session.
- Issue: Whether removing small-work handling should affect only the in-progress new framework or also clean up older framework materials in the repository.
- Positions:
  1. Update the new framework only.
  2. Update both the new framework and legacy docs.
- Arguments: The user selected the narrower scope directly, which preserves a minimal diff and avoids changing historical or legacy guidance without explicit instruction.
- Warrant: When a repository contains both active and legacy documentation, scope should follow the user's explicit target rather than assuming a full-repo normalization.
- Qualifier: for this session
- Status: settled
- Source: "1" in response to the scope choice between `work_delivery_framework/` only and `work_delivery/` cleanup too. (Transcript L3-L3)

### D2
- Decision: Remove the small-work path entirely from the new framework and replace it with one initiative path for planned software initiatives.
- Issue: Whether the specification should continue to model `small-work` versus `large-work`, or be simplified to a single path for planned software initiatives.
- Positions:
  1. Keep the dual model and merely reduce references.
  2. Remove the dual model and keep one initiative path.
  3. Remove the dual model and also rewrite the sections built around it.
- Arguments: The dual model was no longer aligned with the user's intent. The packaging and scaling sections were structurally built around the old split, so they needed more than term deletion.
- Warrant: If the specification is intended to govern only planned software initiatives, alternate classes and substitute primary artifacts should be removed so the control model stays internally consistent.
- Qualifier: in the new framework specification
- Status: settled
- Source: The approved design summary: "Remove `small-work` and `large-work` classification language", "Remove `Work Brief` packet mode", and "Keep one required initiative definition path for Gate 2." (Transcript L4-L5)

## INSIGHT

### I1
- Insight: In this framework, small-work handling was not a local term but a structural modeling choice that touched packaging, scaling, gate criticality, artifact YAML, and anti-bureaucracy rules.
- Domain: framework-design
- Confidence: high
- Source: The implementation summary explicitly described the edit as a "true model collapse" that removed the `Work Brief` artifact, the classification section, and packet-mode gate rules, then reworded scaling as proportional rigor inside one initiative path. (Transcript L7-L7)

### I2
- Insight: The most useful output for this request was not a plan document or abstract analysis, but a compact execution brief followed by direct specification edits.
- Domain: operational
- Confidence: high
- Source: The user asked to "Transform my request into a structured brief, then execute it," and then approved the brief/design directly rather than asking for a separate spec or plan artifact first. (Transcript L1-L1, L5-L5)

## PATTERN

### P1
- Pattern: Reframe a vague framework-change request into a scoped execution brief before editing.
- Scope: local
- Components:
  1. infer the role, objective, approach, and useful output shape
  2. ask one scope-setting question if repository boundaries are ambiguous
  3. propose a small set of editing approaches with a recommendation
  4. get explicit approval on the chosen design
  5. make the minimal structural edit and verify for leftover vocabulary
- Why it matters: The session avoided both over-scoping and under-editing by turning an ambiguous wording change into an explicit model change with a user-approved boundary.
- Source: The user instruction to restructure the request as `ROLE`, `OBJECTIVE`, `APPROACH`, and `OUTPUT`, followed by the scope question and approval sequence. (Transcript L1-L5)

## SOLUTION

### S1
- Problem: The new framework specification still modeled `small-work` as a first-class path, including a `Work Brief` packet, dual-tier scaling rules, quick-pass gate language, and packet-mode critical-artifact mappings, which conflicted with the user's requirement that the specification only handle planned software initiatives.
- Fix: Removed the `Work Brief` artifact and all `small-work` / `large-work` references from `work_delivery_framework/work_delivery_framework_specification.md`, rewrote Section `2.7` as single-path scaling for planned software initiatives, and normalized downstream references in gate YAML, acceptance criteria guidance, supportability guidance, anti-bureaucracy rules, and gate-mapping rules.
- Why the fix works: The specification now expresses one coherent operating model instead of leaving a deleted branch half-implied through artifact names, gate rules, and machine-consumable structures.
- Caveats: The legacy `work_delivery/` documents still contain small-work concepts because the user explicitly scoped this session to the new framework only.
- Source: The edit summary and verification note that the remaining references were removed from the new framework file, while legacy docs were intentionally untouched. (Transcript L7-L7)

## NEXT_STEP

### NS1
- What: Commit the specification change and this session digest together.
- Why: The user explicitly requested both the digest and the commit in the same follow-up instruction.
- Urgency: now
- Source: "create a session digest then commit the changes." (Transcript L6-L6)

## Connections

D1 --[led_to]--> A1
D2 --[led_to]--> A1
I1 --[informed_by]--> D2
I2 --[informed_by]--> P1
P1 --[led_to]--> D1
P1 --[led_to]--> D2
S1 --[depends_on]--> D1
S1 --[depends_on]--> D2
NS1 --[depends_on]--> A2
NS1 --[related_to]--> A1

## Trail Updates

- Extends the `work-delivery-framework` trail.
- Revises the current framework direction after the earlier scaling-focused work recorded in [2026041204_work_delivery_framework_a09_scaling_rules_resolved.md](</home/rmicua/projects/ssd-its-operating-model/session_digests/2026041204_work_delivery_framework_a09_scaling_rules_resolved.md>) by removing the small-work / large-work split from the new specification.
- Records that the legacy `work_delivery/` documents were intentionally left unchanged in this session because the user selected the narrower scope.
