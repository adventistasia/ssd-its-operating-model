---
lorespec: "0.1"
id: "2026041107"
date: "2026-04-11"
source: "codex"
topic: "A05 resolved: formal lifecycle stages and gates including Acceptance Owner acceptance, transition completion, and closure completion"
tags: [work_delivery_framework, lifecycle, stage, gate, acceptance, transition, closure]
classification:
  type: "operational"
  secondary_type: "drafting"
  domains: [work-delivery, governance, documentation]
  value: "high"
trails: [work-delivery-framework]
---

## Session Arc

### Started
The session started with a structured ambiguity-resolution process: identify the next unresolved ambiguity in the resolution plan, interview to clarify intent, then update the specification and check off the ambiguity. ("Open ... resolution plan ... determine which ambiguity item is currently active" (Transcript L1-L1))

### Pivots
- The end-state definition pivoted from “documentation readiness” to **post-delivery acceptance**: the user clarified that acceptance means acceptance of the delivered solution against specified acceptance criteria. ("Acceptance of delivered solution according to specified acceptance criteria." (Transcript L5-L5))
- The gate model pivoted when the user identified that “All deliverables delivered” was not the same as acceptance; Gate 6 was redefined to “All deliverables accepted” with Acceptance Owner accountability. ("change Gate 6 to All deliverables accepted" (Transcript L9-L9))

### Ended
The session ended with a complete stage-and-gate sequence, including a new explicit **Transition Complete** gate and a **Closure Complete** gate with decision ownership by ITS Director or PMO depending on project. ("Closure ... Decision owner will be ITS Director or PMO depending on project." (Transcript L9-L9))

## ARTIFACT

### A1
- Artifact: Updated Work Delivery Framework Specification and Resolution Plan reflecting A05 as resolved with explicit stages and gates.
- Where:
  - `work_delivery_framework/work_delivery_framework_specification.md`
  - `work_delivery_framework/resolution_plan_work_delivery_framework_specification.md`
- What the artifact now encodes:
  - A formal ordered stage model. ("The formal stages are: Intake ... Closure" (Transcript L5-L5))
  - A formal gate set with acceptance clarified and closure governance stated. ("change Gate 6 to All deliverables accepted" (Transcript L9-L9))

## DECISION

### D1
- Decision: Define the framework lifecycle as a fixed ordered set of stages with explicit progression gates, including (1) Acceptance Owner acceptance of the delivered solution, (2) transition to supported operating state, and (3) formal closure completion.
- Issue: A05 was ambiguous because the specification implied a staged flow but did not define formal stages, gate names, or exit criteria, which would cause teams to invent their own process. ("Lifecycle stages ... are not explicit" (Transcript L2-L2))
- Positions:
  - P1: Use a multi-stage lifecycle from Intake through Closure, with explicit gates including qualification, authorization (conditional), specification completeness, MVP approval, acceptance, transition completion, and closure completion. ("The formal stages are: ..."; "Gates: ..." (Transcript L5-L5))
  - P2: Treat “delivery-ready documentation” as the end-state and omit post-delivery acceptance/transition mechanics (risk: mismatch to how completion is actually judged). ("Acceptance of delivered solution ..." (Transcript L5-L5))
- Arguments:
  - The real completion criterion for the business is acceptance of the delivered solution against defined acceptance criteria, not only document readiness. ("Acceptance of delivered solution according to specified acceptance criteria." (Transcript L5-L5))
  - Gate naming must avoid conflating “delivered” with “accepted”; the acceptance decision needs an accountable Acceptance Owner. ("Gate 6 means (A)." (Transcript L7-L7); "change Gate 6 to All deliverables accepted" (Transcript L9-L9))
  - Closure should be a governed step distinct from acceptance, with an explicit decision owner depending on project context. ("Decision owner will be ITS Director or PMO depending on project." (Transcript L9-L9))
- Warrant: If stages and gates are not explicit (including acceptance and transition), teams will substitute local interpretations of “done,” leading to inconsistent stop/proceed behavior and inconsistent definitions of completion.
- Qualifier: Authorization is explicitly conditional (for large/complex initiatives); mapping details may evolve when scaling thresholds are resolved. ("Authorization - Required for large or complex initiatives ..." (Transcript L5-L5))
- Status: settled (captured as the intended lifecycle and gate model for A05).

## INSIGHT

### I1
- Insight: A gate model that only says “deliverables delivered” is insufficient as a definition of completion when the organization’s true completion criterion is **Acceptance Owner acceptance** against defined acceptance criteria.
- Evidence: "Gate 6 means (A)." and "change Gate 6 to All deliverables accepted." (Transcript L7-L7; Transcript L9-L9)
- Confidence: high

## OPEN_QUESTION

### OQ1
- Question: Given the now-explicit lifecycle and gates, what is the canonical artifact taxonomy that provides the gate evidence (core vs conditional artifacts, required sections, and completeness criteria)?
- Why it matters: Gates require evidence; without an explicit artifact model, teams can still diverge in what they present at each gate.
- Prompted by: The next unresolved ambiguity in the plan sequence after A05. ("The next active ambiguity is A06." (Transcript L2-L2))

## NEXT_STEP

### NS1
- What: Resolve A06 (required artifact taxonomy) by defining the canonical artifact set and mapping artifacts to stages/gates with required contents and completeness criteria.
- Prompted by: The resolution plan order advancing from A05 to A06 once stages/gates exist. ("The next active ambiguity is A06." (Transcript L2-L2))
- Urgency: soon

## Connections

D1 --[led_to]--> A1
I1 --[informed_by]--> D1
I1 --[led_to]--> OQ1
D1 --[led_to]--> NS1

## Trail Updates

- Extends trail: `work-delivery-framework`.
- Related prior digests in this trail include: A01 scope boundary, A02 Markdown-first operating model, and A03 governance and gate decision owner model; this session extends that sequence by resolving A05 lifecycle stages and gates. ("Recommended high-level order ... Define scope ... governance ... stages ..." (Transcript L1-L1))

