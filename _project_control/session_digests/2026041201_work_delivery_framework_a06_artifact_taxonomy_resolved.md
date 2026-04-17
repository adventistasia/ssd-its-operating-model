---
lorespec: "0.1"
id: "2026041201"
date: "2026-04-12"
source: "codex"
topic: "A06 resolved: defined canonical artifact taxonomy with Work Brief packet mode, always-required Decision Log, and conditional artifacts mapped to gate timing"
tags: [work_delivery_framework, a06, artifact_taxonomy, work_brief, decision_log, gate_timing]
classification:
  type: "operational"
  secondary_type: "drafting"
  domains: [work-delivery, governance, documentation]
  value: "high"
trails: [work-delivery-framework]
---

## Session Arc

### Started
The session started with a request to resolve ambiguities in the Work Delivery Framework specification using an interview-first approach and then updating the spec and resolution plan accordingly. ("interview me until you are 95% confident" (Transcript L1-L1))

### Pivots
- The user constrained scope to resolving **only unresolved ambiguities**, preventing rework of already-settled items and focusing the session on A06 (artifact taxonomy). ("only resolve ambiguities that are unresolved." (Transcript L2-L2))
- The taxonomy definition pivoted from “artifact categories” to a strict distinction: several labels are category labels (not artifacts), while the canonical artifact set is a list of named outputs with triggers and gate timing. ("DevOps and Support is a category label." (Transcript L6-L6); "Solution Design is a category label. TDD is an artifact." (Transcript L6-L6))

### Ended
The session ended with A06 specified as: (1) two packaging modes (Work Brief packet vs separate artifacts), (2) an always-required Decision Log, (3) conditional artifacts with explicit triggers, and (4) “required-by gate” timing for each artifact. ("one packet for small work (work brief), separate files for large work." (Transcript L4-L4); "Decision Log is always required." (Transcript L7-L7); "TDD: Gate 4" (Transcript L7-L7))

## ARTIFACT

### A1
- Artifact: Updated specification and resolution plan capturing A06 as resolved.
- Where:
  - `work_delivery_framework/work_delivery_framework_specification.md`
  - `work_delivery_framework/resolution_plan_work_delivery_framework_specification.md`
- What changed (high level):
  - Added a canonical artifact taxonomy section including packaging modes, always-required artifacts, conditional triggers, and gate timing. ("Work Brief / Project Brief: Gate 2" (Transcript L7-L7))
  - Marked A06 as resolved in the ambiguity register and prioritized plan, as requested by the user’s update-and-checkoff workflow. ("update ... and ... (check off the ambiguity item)" (Transcript L1-L1))

## DECISION

### D1
- Decision: Resolve A06 by defining a canonical artifact taxonomy with (a) a small-work packet artifact (Work Brief), (b) a large-work separate artifact set, (c) an always-required Decision Log, and (d) conditional artifacts driven by explicit triggers and required-by gate timing.
- Issue: A06 was ambiguous because “project documentation / solution definition / delivery approach / support / handoff” were referenced without a canonical artifact set, content expectations, or conditionality rules.
- Positions:
  - P1: Define a minimal canonical set (names + triggers + gate timing) and allow packaging differences (Work Brief packet vs separate artifacts) while leaving scaling thresholds to A09. ("one packet for small work (work brief), separate files for large work." (Transcript L4-L4))
  - P2: Allow teams to pick any artifact set as long as outcomes are met (risk: inconsistent execution and invented templates).
- Arguments:
  - Different delivery modes require different required outputs (e.g., vendor delivery needs a delivery-team charter; authorization needs a project charter). ("external vendor involved - delivery charter, authorization required - project charter" (Transcript L4-L4); "when both apply, produce both." (Transcript L7-L7))
  - Gate timing must be explicit to prevent “late documentation” that cannot influence decisions. ("TDD: Gate 4" (Transcript L7-L7); "Deployment Guide: Gate 6" (Transcript L7-L7))
  - Category labels should not be misread as mandatory files; the framework needs both category labels and concrete artifact definitions. ("Project Governance ... category label" (Transcript L8-L8); "Solution Design is a category label. TDD is an artifact." (Transcript L6-L6))
- Warrant: If artifact names, triggers, and required-by gate timing are not explicit, teams will invent different “packs” and reviewers cannot enforce consistent readiness gates across initiatives.
- Qualifier: The artifact set is expected to evolve as the framework becomes clearer, but evolution must happen by updating the canonical taxonomy in the specification. ("artifacts is expected to change as this framework is made clearer." (Transcript L4-L4))
- Status: settled (captured as the intended artifact taxonomy for A06).

## INSIGHT

### I1
- Insight: A durable artifact taxonomy requires separating (1) category labels that organize required content from (2) concrete artifacts that are gated and auditable; otherwise, labels get misinterpreted as mandatory documents.
- Evidence: "DevOps and Support is a category label." and "Solution Design is a category label. TDD is an artifact." (Transcript L6-L6)
- Confidence: high

## OPEN_QUESTION

### OQ1
- Question: Where the framework ends relative to downstream engineering technical specifications beyond the defined artifact set (the unresolved boundary topic captured as A07 in the resolution plan).
- Why it matters: The boundary determines which technical documents are required by this framework vs derived downstream, which in turn affects readiness criteria and review scope.
- Prompted by: The user’s instruction to resolve ambiguities as registered in the resolution plan, while only resolving unresolved items in this session. ("resolve ambiguities ... as registered in ... resolution_plan_work_delivery_framework_specification.md" (Transcript L1-L1); "only resolve ambiguities that are unresolved." (Transcript L2-L2))

## NEXT_STEP

### NS1
- What: Resolve the A07 boundary between framework outputs and technical specification work using the same interview → synthesize → update-spec approach.
- Prompted by: The remaining unresolved ambiguity set in the resolution plan after completing A06. ("only resolve ambiguities that are unresolved." (Transcript L2-L2))
- Urgency: soon

## Connections

D1 --[led_to]--> A1
I1 --[informed_by]--> D1
D1 --[led_to]--> OQ1
OQ1 --[led_to]--> NS1

## Trail Updates

- Extends the existing `work-delivery-framework` trail and continues the ambiguity-resolution sequence from:
  - `session_digests/2026041107_work_delivery_framework_a05_lifecycle_stages_and_gates_resolved.md`
