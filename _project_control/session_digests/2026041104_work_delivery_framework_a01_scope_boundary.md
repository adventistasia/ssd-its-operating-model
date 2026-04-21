---
lorespec: "0.1"
id: "2026041104"
date: "2026-04-11"
source: "codex"
topic: "Resolved A01 by defining the default scope boundary for the Work Delivery Framework"
tags: [work-delivery-framework, ambiguity-resolution, scope, software-delivery, governance]
classification:
  type: "drafting"
  secondary_type: "framework-design"
  domains: [work_delivery_framework, governance, delivery_operations]
  value: "high"
trails: [work-delivery-framework, ambiguity-resolution]
---

## Session Arc

### Started
The session focused on the first active ambiguity in the Work Delivery Framework resolution plan: A01, the unresolved scope boundary for which work types are governed by the framework.

### Pivots
- The ambiguity was confirmed as the active item because it was the first unresolved entry in both the ambiguity register and the prioritized resolution plan.
- The scope question was then narrowed into three explicit buckets: in scope, out of scope, and conditional use.
- The user clarified that the framework should be optimized for software initiatives rather than treated as a universal enterprise change framework.

### Ended
The session ended with A01 resolved. The framework now has an explicit default scope boundary that can anchor future decisions about framework form, governance, lifecycle stages, artifacts, completeness, and scaling.

## ARTIFACT

### A1
- Artifact: `work_delivery_framework/work_delivery_framework_specification.md`
- Final state: Updated to define a new `Scope of applicability` section that states the framework is optimized for software initiatives and records in-scope, out-of-scope, and conditional categories.
- Why it matters: This turns a directional statement into an operational boundary for future framework design.

### A2
- Artifact: `work_delivery_framework/resolution_plan_work_delivery_framework_specification.md`
- Final state: Updated to mark A01 as resolved in both the ambiguity register and the prioritized resolution plan.
- Why it matters: This keeps the tracking document aligned with the settled decision and makes A02 the next active ambiguity.

### A3
- Artifact: `session_digests/20260411_work_delivery_framework_a01_scope_boundary.md`
- Final state: Created as the LoreSpec session digest for the resolved ambiguity.
- Why it matters: It preserves the session arc, settled decision, and next step without relying on chat history.

## DECISION

### D1
- Decision: Optimize the Work Delivery Framework for software initiatives and define its default scope accordingly.
- Issue: Whether the framework should be broadly applicable to many work types or centered on software delivery with only limited reuse outside that default boundary.
- Positions:
  - Define the framework broadly for software and non-software work.
  - Optimize the framework for software initiatives and allow only limited conditional reuse outside that default boundary. (Chosen)
- Arguments:
  - The user explicitly scoped the framework to greenfield and brownfield software projects.
  - The user explicitly excluded minor low-risk changes, research spikes, support work, and small internal process changes.
  - The user allowed only conditional use for complex operational changes affecting multiple organizations, complex internal process changes affecting the whole organization, and non-software initiatives that can use the framework with minimum changes.
- Warrant: Future framework mechanics should be designed around a clear primary work type rather than broad abstraction.
- Qualifier: Conditional reuse is allowed where the same control logic fits with minimal change.
- Status: settled

## INSIGHT

### I1
- Insight: The user wants reuse beyond software only where the framework can be applied with minimum change, not through broad default generalization.
- Domain: framework-design
- Confidence: high

### I2
- Insight: The main boundary is not only software versus non-software; it is also whether the work is complex and organization-wide enough to justify governed delivery treatment.
- Domain: governance
- Confidence: high

## PATTERN

### P1
- Pattern: Default-scope plus conditional-extension boundary.
- Scope: local
- Components:
  - Set a default design target for the framework.
  - State explicit exclusions for low-governance or low-signal work.
  - Allow conditional extension only for cases that share the same control needs.
  - Prevent conditional reuse from silently redefining the framework's primary purpose.
- Why it matters: This preserves a clear core framework while still allowing disciplined reuse in adjacent cases.

## NEXT_STEP

### NS1
- What: Resolve A02 — Framework form and publication model.
- Why: A01 is now settled, and A02 is the next unresolved item in the prioritized plan.
- Urgency: next session

## Connections

D1 --[led_to]--> A1
D1 --[led_to]--> A2
D1 --[led_to]--> A3
I1 --[informed_by]--> D1
I2 --[informed_by]--> D1
P1 --[instance_of]--> D1
A2 --[led_to]--> NS1

## Trail Updates

- Extends `ambiguity-resolution` by settling A01 and recording the first resolved foundational ambiguity for `work_delivery_framework/`.
- Extends `work-delivery-framework` by fixing the default applicability boundary before framework form, governance, intake, stages, and artifacts are designed.
- Sets up the next session to move directly to A02 without reopening scope unless a later dependency forces reconsideration.
