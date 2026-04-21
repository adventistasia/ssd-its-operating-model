---
lorespec: "0.1"
id: "work-delivery-framework-eng-ai-goals-assessment"
date: "2026-04-10"
source: "codex"
topic: "Work Delivery Framework assessment for engineering execution and AI-agent delivery"
tags: [work_delivery, operating_model, governance, engineering_delivery, ai_delivery, assessment]
classification:
  type: "drafting"
  secondary_type: "operating-model-assessment"
  domains: [work_delivery_framework, engineering_execution, autonomous_agents, documentation_governance]
  value: "high"
trails: []
---

## Session Arc

### Started
This session centers on a single source “transcript”: `work_delivery/work_delivery_framework_assessment_against_engineering_and_ai_delivery_goals.md`, which frames an assessment of the repository’s `work_delivery` framework against engineering execution and autonomous AI delivery goals. (Transcript L1-L6)

### Pivots
- The assessment distinguishes “strong governance + closure” from “weak execution middle”, focusing on the missing bridge from approved design to executable delivery. (Transcript L10-L26)
- The recommended resolution shifts away from creating a separate AI-only framework and toward a layered model: readable primaries plus structured overlays plus an execution-planning layer. (Transcript L28-L29, Transcript L139-L140, Transcript L262-L309)

### Ended
The assessment ends with a prioritized action plan and an overall conclusion that the core gaps are standardization in the execution layer and machine-readable structure needed for deterministic AI-agent operation. (Transcript L311-L378)

### Working Draft Notes
- Source document declares `working draft` and explicitly lists missing control inputs (owner, reviewer, decision basis, deliverable identity). This digest preserves that status and does not treat recommendations as approved decisions. (Transcript L3-L6)

## ARTIFACT

### A1
- Artifact: `work_delivery/work_delivery_framework_assessment_against_engineering_and_ai_delivery_goals.md` (assessment record).
- Summary: A governed operating-model assessment that recognizes the `work_delivery` framework as strong in stage control, governance, operational readiness, acceptance, and closure, but identifies a key gap for engineering execution and autonomous agents: the absence of a standard method to translate approved design artifacts into executable delivery units (work packages, tasks, dependencies, acceptance evidence). It proposes a unified target state (not a split human vs AI model) that keeps narrative Markdown as authoritative, adds lightweight structured overlays for determinism, and adds an execution-planning layer to bridge Stage 4 to Stage 5. It closes with a prioritized action plan emphasizing (1) a delivery work package/task breakdown specification, (2) tighter architecture view standards, (3) overlays/manifests, and (4) as-built/variance recording for brownfield trustworthiness. (Transcript L8-L29, Transcript L50-L61, Transcript L262-L333)
- Evidence: “Its main weakness is the missing middle between approved design and executable delivery.” (Transcript L19-L19)

## DECISION

### D1
- Decision: Adopt a single shared delivery framework for both humans and autonomous AI agents, supplemented by (a) lightweight structured overlays and (b) a standard execution-planning layer, rather than creating separate “human” and “AI” frameworks.
- Issue: How to evolve the repository’s `work_delivery` framework so it remains governable and readable for humans while becoming deterministic enough for autonomous AI-agent delivery.
- Positions:
  - Keep current prose-first framework only; accept that teams invent execution structure (status quo).
  - Create a separate AI-only framework with agent-specific controls.
  - Keep one shared narrative framework and add the minimum structured overlays + a standard execution layer (recommended).
- Arguments:
  - Pro: Maintaining one shared set of authoritative narrative documents preserves governance usability and review practicality. (Transcript L268-L279)
  - Pro: Structured overlays/annexes minimize duplication while providing deterministic parsing for artifact identity, inventories, evidence references, and execution units. (Transcript L80-L89, Transcript L282-L295)
  - Pro: A standard planning artifact bridges the current gap between approved design and executable work, improving consistency and enabling modular delivery. (Transcript L50-L61, Transcript L296-L309)
  - Con: Adding overlays introduces schema and lifecycle overhead that must be governed to avoid drift and fragmentation. (Transcript L130-L138, Transcript L164-L165)
- Warrant: If the framework is intended to be an operational system (not just a governance record), it must keep a single human-auditable baseline while adding only the minimum deterministic structure required for reliable execution and future maintenance.
- Qualifier: recommended target state / best-fit approach for this repository; requires explicit ownership and acceptance of new artifacts before being treated as “the framework”. (Transcript L3-L6, Transcript L264-L265, Transcript L369-L376)
- Status: proposed
- Source: “The right target state is one shared framework, not separate human and AI frameworks.” (Transcript L28-L28)

## INSIGHT

### I1
- Insight: The framework’s biggest engineering-delivery gap is not a lack of design and governance artifacts; it is the missing conversion step from approved design to executable delivery units with defined dependencies and acceptance evidence.
- Confidence: high (explicitly stated as the “missing middle” and linked to concrete missing specs/fields).
- Source: “What is missing is the standard step that turns those approved artifacts into executable delivery units.” (Transcript L50-L50)

### I2
- Insight: For AI agents, the limiting factor is structural determinism rather than language complexity: cross-document joins across prose create inconsistent inference risk unless IDs, fields, and relationships are normalized.
- Confidence: medium-high (argued in narrative + reinforced by usability/gap tables).
- Source: “The main problem is not language complexity. The main problem is structural overhead.” (Transcript L130-L132)

## PATTERN

### P1
- Pattern: Three-layer documentation architecture for governed engineering + AI delivery.
- Scope: local (repository pattern for this operating model).
- Steps/components:
  1. Keep primary narrative Markdown documents as the authoritative human-readable control baseline (scope, architecture narrative, ops readiness, acceptance, closure). (Transcript L266-L279)
  2. Add lightweight structured overlays/sidecars for deterministic fields AI agents and maintainers must parse reliably (manifests/inventories for initiative/module/interface/validation/deployment/brownfield baseline). (Transcript L280-L295)
  3. Add an execution layer: one standard planning artifact that translates approved scope/design into sequenced, dependency-aware, acceptance-linked delivery work units. (Transcript L296-L309)
- Why it works: It preserves governance usability and review practicality while enabling consistent parsing and task derivation for autonomous delivery without duplicating narrative artifacts. (Transcript L28-L29, Transcript L294-L295)
- Source: “The recommended target state is one shared framework with three layers.” (Transcript L264-L264)

## OPEN_QUESTION

### OQ1
- Question: What is the minimal, governed schema set for “structured overlays” (field names, IDs, status models, inventories), and how will those overlays be validated and kept consistent with the narrative documents across change, acceptance, and as-built drift?
- Why it matters: Without an explicit schema + lifecycle governance, overlays can become another fragmentation point, weakening determinism and trust for both agents and future maintainers.
- Partial progress: Candidate resolutions are described (YAML/JSON sidecar/front matter; specific overlay types; need for strict IDs and a unified traceability model), but schemas and validation mechanisms are not defined here. (Transcript L159-L165, Transcript L251-L260, Transcript L339-L353)
- Source: “Keep Markdown as the primary artifact and add a small YAML or JSON sidecar or front matter” (Transcript L159-L159)

## REFERENCE

### R1
- Reference: `work_delivery/work_delivery_framework.md`
- Relevance: Defines the stage model and expectation that Stage 5 includes a delivery plan/task breakdown, which the assessment cites as underspecified (missing a corresponding decomposition specification). (Transcript L52-L61)
- Source: “The framework requires a delivery plan or initial task breakdown in Stage 5…” (Transcript L52-L52)

### R2
- Reference: `work_delivery/ai_assisted_authoring_standard.md`
- Relevance: Establishes prompt order/guardrails for AI-assisted drafting, but does not define deterministic data structures for autonomous agents to read/update/validate/hand off. (Transcript L90-L92)
- Source: “...but it does not define the data structure an agent should reliably read, update, validate, or hand off.” (Transcript L90-L91)

## NEXT_STEP

### NS1
- What: Add `delivery_work_package_and_task_breakdown_specification.md`.
- Why: Standardizes conversion of approved design into executable delivery (work packages, tasks, dependencies, acceptance evidence), closing the largest execution gap.
- Urgency: now
- Source: “This is the most urgent gap…” (Transcript L317-L318)

### NS2
- What: Strengthen the Technical Design Document requirements or add a separate architecture view standard so initiatives produce a minimum consistent architecture view set.
- Why: Improves cross-initiative consistency and reduces reconstruction burden for delivery and brownfield maintenance.
- Urgency: soon
- Source: “...so every engineering initiative produces a minimum consistent architecture view set.” (Transcript L321-L321)

### NS3
- What: Add lightweight machine-readable overlays/manifests and an as-built/implementation-variance artifact.
- Why: Provides deterministic inventories and an explicit runtime truth baseline for agent execution and brownfield trustworthiness.
- Urgency: soon
- Source: “Add lightweight machine-readable overlays…” (Transcript L325-L333)

## SOLUTION

### S1
- Solution: Introduce a “Delivery Work Package and Task Breakdown” planning artifact/specification that becomes the standard bridge between Stage 4 (approved design) and Stage 5 (delivery mobilization).
- What it fixes: Eliminates the need for each team to invent its own task decomposition method, reducing variability and enabling consistent acceptance-linked slicing for both human and AI execution. (Transcript L50-L61)
- Why the fix works: It defines a canonical derivation from existing IDs (`FC-###`, `SM-###`, `UC-###`, `QA-###`, `INT-###`) into execution units with dependencies, ownership, reviewers, evidence, and acceptance linkage—making “executable work” a governed artifact instead of an implicit step. (Transcript L187-L207)
- Caveats: Requires explicit governance for IDs, lifecycle status, and alignment with acceptance/closure so the planning artifact and overlays do not drift from the narrative baseline. (Transcript L153-L154, Transcript L339-L353)
- Source: “Add one standard planning artifact that converts approved scope and design into executable delivery units.” (Transcript L298-L298)

## Connections

D1 --[led_to]--> NS1
D1 --[led_to]--> P1
I1 --[informed_by]--> A1
I2 --[informed_by]--> A1
P1 --[depends_on]--> OQ1
S1 --[instance_of]--> NS1

## Trail Updates

- No trail name was provided for this session digest; `trails` remains empty.
- Candidate future trail: if you are tracking framework evolution work, consider adding a trail and linking follow-on sessions that draft the new specifications and overlays.
