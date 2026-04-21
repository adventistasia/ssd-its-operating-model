---
lorespec: "0.1"
id: "2026041103"
date: "2026-04-11"
source: "codex"
topic: "Chose work_delivery_framework as the authoritative framework and agreed to resolve ambiguities while updating the spec iteratively"
tags: [work-delivery, framework, work-delivery-framework, ambiguity-resolution, deprecation, delivery-owner, acceptance, evidence]
classification:
  type: "strategy"
  secondary_type: "framework-design"
  domains: [work_delivery_framework, governance, documentation, delivery_operations]
  value: "high"
trails: [work-delivery-framework, ambiguity-resolution, framework-usability]
---

## Session Arc

### Started
The user expressed intent to rewrite the existing Work Delivery Framework because it feels heavy and hard to use. (Transcript L1-L1)

### Pivots
- The direction shifted from "rewrite the existing framework" to "replace it" when the user stated they plan to replace `work_delivery/` with `work_delivery_framework/` and deprecate the legacy folder. (Transcript L12-L12)
- The lifecycle approach pivoted when the user stated they want an entirely new lifecycle model (not preserving the existing 7-stage model) and that the work is still in progress. (Transcript L16-L16)
- The primary operator persona was clarified as the Delivery Owner, which focused the framework design on repeat-use guidance and operational clarity rather than policy prose. (Transcript L23-L23)
- The main pain points were narrowed to "what's next" ambiguity and acceptance/evidence pain at the end, which implies the new framework must emphasize next-step routing and continuous evidence readiness. (Transcript L25-L25)
- The operating approach pivoted to "ambiguity-first" iteration: resolve ambiguities according to the resolution plan and update the specification as decisions are made. (Transcript L33-L33)

### Ended
The session ended with the user directing that ambiguity resolution should follow the recommended order in `work_delivery_framework/resolution_plan_work_delivery_framework_specification.md`, starting from foundational ambiguities (scope/form/governance) and updating the spec along the way. (Transcript L34-L34)

## ARTIFACT

### A1
- Artifact: `work_delivery_framework/work_delivery_framework_specification.md` (draft specification).
- Final state (in this session): Treated as the active draft to be iteratively updated as ambiguities are resolved. (Transcript L30-L30)
- Evolution: The user positioned this spec as the basis for building a new authoritative framework, not merely a meta-description. (Transcript L12-L12)
- Source: "I plan to replace the whole thing with [work_delivery_framework]" (Transcript L12-L12)

### A2
- Artifact: `work_delivery_framework/resolution_plan_work_delivery_framework_specification.md` (resolution plan).
- Final state (in this session): Confirmed as the sequencing source-of-truth for ambiguity resolution (foundational cluster first). (Transcript L34-L34)
- Source: "whatever is recommended in the resolution_plan_work_delivery_framework_specification.md" (Transcript L34-L34)

## DECISION

### D1
- Decision: Make `work_delivery_framework/` the authoritative home of the Work Delivery Framework and deprecate `work_delivery/`.
- Issue: Whether to incrementally improve the legacy `work_delivery/` framework or replace it with the in-progress `work_delivery_framework/` draft set.
- Positions:
  - Keep `work_delivery/` authoritative and refactor for usability.
  - Make `work_delivery_framework/` authoritative and deprecate `work_delivery/`. (Chosen)
- Arguments:
  - The existing `work_delivery/` framework is perceived as heavy/hard to use, motivating replacement rather than further patching. (Transcript L1-L1)
  - The user has already started new work in `work_delivery_framework/` (spec + resolution plan), suggesting momentum is on the replacement path. (Transcript L30-L30)
- Warrant: If the current framework's usability problems are structural and the target lifecycle model is expected to change substantially, replacement reduces drag versus reworking a legacy information architecture.
- Qualifier: This commits only to the repository's authoritative location and deprecation intent; it does not yet define the new lifecycle model or artifact set.
- Status: settled (direction set), with implementation still in progress.
- Source: "authoritative will be work_delivery_framework and deprecate work_delivery" (Transcript L12-L12)

### D2
- Decision: Define an entirely new lifecycle model based on the evolving specification and ambiguity resolution, rather than retaining the current 7-stage governance spine.
- Issue: Whether the new authoritative framework should preserve the existing stage model (with edits) or design a new lifecycle model.
- Positions:
  - Preserve the 7-stage model (optionally with overlays).
  - Define a new lifecycle model. (Chosen)
- Arguments:
  - The user explicitly wants "an entirely new one" and states the framework is still a work in progress, implying openness to re-grounding lifecycle from first principles. (Transcript L16-L16)
- Warrant: If the stage model is a primary contributor to "what's next" confusion and acceptance/evidence pain, a redesigned lifecycle may better encode operator routing and acceptance-readiness as first-class controls.
- Qualifier: The new lifecycle is not yet specified; this is a design direction, not a completed stage definition.
- Status: settled (direction set).
- Source: "we will define an entirely new one" (Transcript L16-L16)

### D3
- Decision: Primary operator persona for the new framework is the Delivery Owner.
- Issue: Who the framework is optimized for (operator-first vs governance-first vs engineering-first vs AI-first).
- Positions: Delivery Owner; PMO/delivery manager; engineering lead; AI agent operator.
- Arguments:
  - User explicitly identified the Delivery Owner as primary persona. (Transcript L23-L23)
- Warrant: If the primary failure modes are "what's next" confusion and end-of-delivery acceptance pain, optimize for the role that runs day-to-day controls and evidence readiness.
- Qualifier: Does not preclude secondary personas; it sets the optimization priority.
- Status: settled.
- Source: "The primary operator persona will be the delivery owner." (Transcript L23-L23)

### D4
- Decision: Resolve ambiguities and update the framework specification iteratively (ambiguity-first development).
- Issue: Whether to pause implementation until all ambiguities are resolved or progress by resolving and incorporating decisions incrementally.
- Positions:
  - Resolve all ambiguities first, then update the spec once.
  - Resolve ambiguities in sequence and update the spec as decisions are made. (Chosen)
- Arguments:
  - User explicitly directed ambiguity resolution + spec update as a combined workflow. (Transcript L33-L33)
- Warrant: If foundational decisions unblock downstream structure (stages, artifacts, readiness rules), an iterative loop reduces churn while keeping the spec aligned with actual decisions.
- Qualifier: Requires a stable ordering (the resolution plan) to avoid thrash.
- Status: settled (working method).
- Source: "we will resolve ambiguity and update the spec as we go along as well." (Transcript L33-L33)

## INSIGHT

### I1
- Insight: The new framework's usability success criteria are dominated by (a) clear next-step routing for Delivery Owners and (b) avoiding late-stage acceptance/evidence scramble.
- Domain: delivery_operations
- Confidence: high
- Source: "unclear 'what's next' and acceptance/evidence pain at the end" (Transcript L25-L25)

### I2
- Insight: Scope definition is intentionally deferred until the new lifecycle and foundational ambiguity cluster are resolved, which is consistent with an ambiguity-first development approach but will keep A01 open longer.
- Domain: framework-design
- Confidence: medium
- Source: "we will see based on the new specs and the resolution plan" (Transcript L19-L19)

## PATTERN

### P1
- Pattern: "Ambiguity-first iteration" for framework design.
- Scope: local
- Components:
  - Use a resolution plan to sequence foundational decisions.
  - Resolve one ambiguity at a time.
  - Update the spec immediately after resolving an ambiguity so the spec remains the canonical current truth.
  - Avoid locking dependent mechanics (stages, artifacts, completeness criteria) before scope/form/governance are decided.
- Why it matters: Prevents teams from inventing incompatible stages/artifacts while also preventing a long "spec-only" period where decisions are not reflected in the canonical document set.
- Source: "resolve ambiguity and update the spec as we go along" (Transcript L33-L33) and "whatever is recommended in the resolution plan..." (Transcript L34-L34)

## OPEN_QUESTION

### OQ1
- Question: What categories of work are in-scope vs out-of-scope for the new framework (A01), given the stated intent to decide scope based on the spec/resolution work rather than upfront.
- Why it matters: Scope determines which lifecycle paths must exist, which artifacts are required, and how to scale rigor versus bureaucracy.
- Partial progress: The user stated scope will be determined based on the new spec and resolution plan, but no default scope option was selected in this session. (Transcript L19-L19)
- Source: "we will see based on the new specs and the resolution plan" (Transcript L19-L19)

### OQ2
- Question: What is the primary "control surface" for Delivery Owners in the new framework (e.g., a runbook-style process spine vs a checklist/tracker template), and how will it drive next-step clarity and evidence readiness.
- Why it matters: This decision directly targets the two primary failure modes (what-next ambiguity and end-of-delivery acceptance pain).
- Partial progress: The user leaned toward a process runbook but did not commit. (Transcript L29-L29)
- Source: "I'm not sure yet but I'm leaning towards process runbook." (Transcript L29-L29)

## REFERENCE

### R1
- Reference: `work_delivery_framework/resolution_plan_work_delivery_framework_specification.md`
- Relevance: Defines the recommended sequencing (scope, form, governance, then intake/stages/artifacts, then completeness/scaling/boundaries, etc.). (Transcript L34-L34)
- Source: The user directive to follow "whatever is recommended" in this plan. (Transcript L34-L34)

### R2
- Reference: 2026-04-10 session digests on framework usability and overlay decisions:
  - `session_digests/20260410_work_delivery_framework_simplification_and_overlay.md`
  - `session_digests/20260410_framework_readability_fatigue_and_plain_language_template.md`
  - `session_digests/20260410_delivery_owner_runbook_and_glossary_for_navigation_fatigue.md`
- Relevance: Provide prior evidence for the human usability failure mode (re-orientation and getting lost) and candidate mitigations (runbook/dashboard, progressive disclosure), while the new work chooses to redesign the lifecycle model entirely. (Transcript L2-L2)
- Source: "also see the session digest from 20260410." (Transcript L2-L2)

## NEXT_STEP

### NS1
- What: Start ambiguity resolution per the plan with the foundational cluster: A01 (scope) -> A02 (framework form/publication) -> A03 (governance/decision rights), and update `work_delivery_framework/work_delivery_framework_specification.md` after each resolution.
- Why: These decisions block intake rules, lifecycle stages, artifact taxonomy, and completeness criteria.
- Urgency: now
- Source: "we will resolve ambiguity and update the spec as we go" (Transcript L33-L33) and the plan's recommended order referenced by the user. (Transcript L34-L34)

## Connections

D1 --[led_to]--> NS1
D2 --[depends_on]--> NS1
D3 --[informed_by]--> I1
D4 --[instance_of]--> P1
A2 --[led_to]--> NS1
I1 --[informed_by]--> D3
OQ1 --[depends_on]--> NS1

## Trail Updates

- Extends `work-delivery-framework` by committing to `work_delivery_framework/` as the authoritative home and by explicitly deprecating `work_delivery/` as the legacy location. (Transcript L12-L12)
- Extends `ambiguity-resolution` by adopting the "resolve ambiguities and update the spec as we go" development method anchored to the existing resolution plan. (Transcript L33-L34)
- Related to `framework-usability`: the new framework remains delivery-owner-optimized and explicitly targets "what's next" clarity and acceptance/evidence readiness as primary usability objectives. (Transcript L23-L25)
