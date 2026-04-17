---
lorespec: "0.1"
id: "2026041203"
date: "2026-04-12"
source: "codex"
topic: "A08 resolved: completeness is a hybrid mandatory-plus-qualitative model applied at artifact and gate level, with Gate 4 requiring strong quality"
tags: [work_delivery_framework, a08, completeness, delivery_readiness, gates, artifacts, ai_validation]
classification:
  type: "operational"
  secondary_type: "drafting"
  domains: [work-delivery, governance, documentation]
  value: "high"
trails: [work-delivery-framework]
---

## Session Arc

### Started
The session began with a focused ambiguity-resolution interview on A08, with the user asking for iterative questioning until the intended completeness model was understood well enough to update the specification and resolution plan. ("interview me until you are 95% confident" (Transcript L1-L1))

### Pivots
- The user chose a hybrid model rather than pure pass/fail or pure scoring, then immediately required mandatory failure when any blocker criterion is unmet. ("hybrid" (Transcript L3-L3); "yes fail immediately" (Transcript L5-L5))
- The model became explicitly two-layered: completeness is judged both per artifact and per gate, with artifact-specific rules plus a small shared core. ("both" (Transcript L7-L7); "each artifact having it's own completeness rules with only a small shared core" (Transcript L9-L9))
- The assistant recommended that only Gate 4 require `strong` quality while other gates require `adequate`, and the user adopted that recommendation. ("only Gate 4 (`Specification Complete`) require `strong` quality" (Transcript L19-L19); "let's adopt this" (Transcript L20-L20))
- The user chose to defer the exact mapping of critical stage-defining artifacts, but required that this unresolved dependency be recorded explicitly in both the spec and the resolution plan. ("leave the mapping later. document this open ambiguity" (Transcript L31-L31))

### Ended
The session ended with A08 resolved into a formal review standard and framework design rule: mandatory completeness checks plus execution-oriented quality ratings, explicit blocker vs open-issue treatment, no conditional progression on completeness failure, and a new deferred ambiguity (A17) for gate-to-critical-artifact mapping. ("review standard + required design property so that AI can also assist in validating completeness." (Transcript L57-L57))

## ARTIFACT

### A1
- Artifact: Updated framework specification and ambiguity resolution plan reflecting A08 as resolved, with a new deferred ambiguity for critical stage-defining artifact mapping.
- Where:
  - `work_delivery_framework/work_delivery_framework_specification.md`
  - `work_delivery_framework/resolution_plan_work_delivery_framework_specification.md`
- What the artifact now encodes:
  - A hybrid completeness model that combines mandatory pass/fail rules with qualitative ratings. ("hybrid" (Transcript L3-L3))
  - Dual-level evaluation at artifact and gate level, with artifact-specific rules plus a small shared core. ("both" (Transcript L7-L7); "each artifact having it's own completeness rules with only a small shared core" (Transcript L9-L9))
  - Explicit reviewer discipline rules, including no undocumented-context upgrades and no conditional progression for completeness failure. ("spec should explicitly forbid this" (Transcript L45-L45); "no conditional progression" (Transcript L51-L51))

## DECISION

### D1
- Decision: Resolve A08 by defining completeness as a hybrid model with immediate-fail mandatory criteria plus qualitative ratings (`weak`, `adequate`, `strong`), applied at both artifact and gate level.
- Issue: The framework previously defined “good” and “complete” directionally, but not as an operational review standard, so gates and reviewers could invent local readiness rules.
- Positions:
  - P1: Use a hybrid model with mandatory blockers plus qualitative ratings. ("hybrid" (Transcript L3-L3))
  - P2: Use strict pass/fail only.
  - P3: Use a scored or purely qualitative rubric without immediate fail conditions.
- Arguments:
  - Mandatory criteria must fail immediately when unmet so teams cannot proceed on incomplete foundations. ("yes fail immediately" (Transcript L5-L5))
  - Completeness must be judged both artifact-by-artifact and gate-by-gate because local document quality and whole-package coherence are distinct concerns. ("both" (Transcript L7-L7))
  - Artifact rules should be tailored to each artifact while still sharing a common review core. ("each artifact having it's own completeness rules with only a small shared core" (Transcript L9-L9))
  - Gate 4 is the point where ambiguity becomes most expensive, so it alone should require `strong` quality. ("only Gate 4 (`Specification Complete`) require `strong` quality" (Transcript L19-L19); "let's adopt this" (Transcript L20-L20))
- Warrant: If completeness is not defined as enforceable mandatory criteria plus a constrained quality model, reviewers and delivery teams will substitute local judgment, hidden assumptions, or formatting polish for genuine readiness.
- Qualifier: The exact mapping of critical stage-defining artifacts is intentionally deferred and recorded as a later ambiguity rather than silently assumed. ("leave the mapping later. document this open ambiguity" (Transcript L31-L31))
- Status: settled (captured as A08 resolution in the specification and resolution plan)

## INSIGHT

### I1
- Insight: A useful completeness model for delivery readiness must separate **minimum safe-to-proceed conditions** from **quality-of-definition judgments**; otherwise one model becomes either too rigid or too subjective.
- Evidence: The user selected a hybrid model, required immediate failure on unmet mandatory criteria, and still wanted qualitative ratings and gate-specific thresholds. ("hybrid" (Transcript L3-L3); "yes fail immediately" (Transcript L5-L5); "depends on gate" (Transcript L17-L17))
- Domain: work-delivery governance
- Confidence: high

### I2
- Insight: Gate-level quality should not be treated as a free-floating reviewer opinion; it works better when constrained by artifact ratings and cross-artifact coherence.
- Evidence: The assistant recommended a separate but constrained gate judgment, and the user accepted it. ("The gate rating cannot exceed the weakest materially relevant cross-artifact condition." (Transcript L26-L26); "yes adopt it" (Transcript L27-L27))
- Domain: readiness evaluation
- Confidence: high

## OPEN_QUESTION

### OQ1
- Question: Which artifacts are the critical stage-defining artifacts for each gate, including when the initiative uses packet mode versus separate artifacts and when conditional artifacts apply?
- Why it matters: The resolved completeness model now depends on critical-artifact identification to determine when a gate can legitimately be rated `strong`, especially at Gate 4.
- Partial progress: The user explicitly chose to defer this mapping and required it to be recorded as a later ambiguity instead of being inferred ad hoc. ("leave the mapping later. document this open ambiguity" (Transcript L31-L31))

## NEXT_STEP

### NS1
- What: Continue the ambiguity sequence with A09 (scaling rules for simple versus complex work), while preserving A17 as a deferred follow-on ambiguity for critical stage-defining artifact mapping.
- Prompted by: A08 being resolved and the resolution plan advancing to the next active unresolved item.
- Urgency: soon

## Connections

D1 --[led_to]--> A1
I1 --[informed_by]--> D1
I2 --[informed_by]--> D1
D1 --[led_to]--> OQ1
D1 --[led_to]--> NS1
OQ1 --[related_to]--> NS1

## Trail Updates

- Extends the `work-delivery-framework` trail and continues the ambiguity-resolution sequence after:
  - `session_digests/2026041202_work_delivery_framework_a07_boundary_to_technical_spec_work_resolved.md`
- Creates a new deferred branch in the trail for `A17`, which was introduced because the A08 completeness model now requires an explicit gate-to-critical-artifact mapping.
