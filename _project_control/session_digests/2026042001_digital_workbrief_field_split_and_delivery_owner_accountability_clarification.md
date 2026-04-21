---
lorespec: "0.1"
id: "2026042001"
date: "2026-04-20"
source: "other"
topic: "Resolve delivery ownership ambiguity and simplify roles by making the Delivery Owner the sole core role while splitting digital Work Brief fields for clearer requirements vs scope/constraints."
tags: [work_delivery_framework, delivery_owner, governance, work_brief, roles, ambiguity_resolution]
classification:
  type: drafting
  secondary_type: operational
  domains: [operating_model, delivery_governance]
  value: medium
trails: [work_delivery_framework, digital_workbrief]
---

## Session Arc

### Started
Questions and decisions were raised to remove ambiguity in ITS governance artifacts: (1) how the digital Work Brief should structure "Requirements" vs "Scope/Constraints", and (2) what "Delivery Owner" means relative to "doing the work".

### Pivots
- The "Delivery Owner" question resolved toward accountability (owns delivery control and outcomes) vs assuming hands-on execution responsibility.
- The Core Roles design pivoted to simplify: remove "Project Manager" as a core role; Delivery Owner remains accountable and can choose to bring in delivery coordination support as needed.

### Ended
A clear governance stance was established: Delivery Owner is the accountable role; project management support is optional and not a core role. The Work Delivery Framework was updated accordingly.

## DECISION

### D1 - Split digital Work Brief "Requirements/scope/constraints" into two fields
- **Decision:** Split the Work Brief field `Requirements, scope, constraints` into (a) `Requirements` and (b) `Scope, Constraints`.
- **Issue:** The combined field was creating ambiguity and hiding operational/support requirements inside "scope/constraints".
- **Positions:**
  - Keep combined field (status quo).
  - Split into two fields (chosen).
- **Arguments:**
  - For split: clearer separation of "what must be true" (requirements) vs "what is included/excluded and bounded" (scope/constraints); reduces misclassification of operational/support needs.
- **Warrant:** Clarity of definition artifacts reduces downstream delivery and acceptance confusion; requirements deserve explicit visibility.
- **Qualifier:** usually
- **Status:** settled (per user statement)
- **Source excerpt:** "split Requirements, scope, constraints field into Requirements then a separate Scope, Constraints field. Support and operational model requirements will be defined under Requirements field."

### D2 - Remove "Project Manager" from Work Delivery Framework Core Roles
- **Decision:** Remove the Project Manager role from the Work Delivery Framework "Core Roles" section.
- **Issue:** The presence of a separate Project Manager role was creating confusion about accountability vs optional support functions.
- **Positions:**
  - Keep Project Manager as a core role.
  - Remove it as a core role and treat it as optional support (chosen).
- **Arguments:**
  - For removal: simplifies governance; preserves single point of accountability (Delivery Owner) while allowing the Delivery Owner to decide what support they need.
- **Warrant:** Core governance roles should represent accountability boundaries; optional delivery coordination is a resourcing choice, not a governance role.
- **Qualifier:** in this case
- **Status:** settled (per user statement)
- **Source excerpt:** "we decided to remove the Project Manager role from the Core roles section. Everything should now fall to the Delivery Owner... which can include hiring/getting a Project Manager."

## INSIGHT

### I1 - "Delivery Owner" is accountable for delivery control, not necessarily the executor
- **Insight:** In this operating model, "Delivery Owner" should be interpreted as the accountable role for stage discipline and delivery control (coordination, evidence readiness, acceptance readiness), not automatically the individual doing all hands-on execution work.
- **Why it matters:** Avoids mis-assigning execution responsibility and supports clearer delegation/resourcing without losing governance accountability.
- **Confidence:** medium (framed as "typically" / unless explicitly defined otherwise)
- **Source excerpt:** "Is delivery owner the person responsible for doing the actual work? Or just in charge?" + assistant framing: "typically accountable rather than the one doing all execution."

## ARTIFACT

### A1 - Updated `work_delivery/work_delivery_framework.md` to reflect Delivery Owner accountability and optional support
- **Artifact:** `work_delivery/work_delivery_framework.md`
- **Change summary (durable):**
  - Clarified that Delivery Owner is accountable for delivery control/stage discipline; execution is typically performed by delivery teams/domain leads/deliverable owners.
  - Removed "Project Manager (if assigned)" from the Core Roles table.
  - Reframed checklist accountability references to "Delivery Owner (or delegate)" / "Delivery Owner (may delegate)" rather than "Project Manager or Delivery Owner".
  - Clarified deliverable execution ownership language in Stage 6 to use "Deliverable Owners (assigned)" to avoid conflating deliverable execution with "Delivery Owner".
- **Source excerpt:** "remove the Project Manager role from the Core roles section... Delivery Owner to determine what they need..."

## NEXT_STEP

### N1 - Update the digital Work Brief template/fields and guidance
- **Action:** Implement the field split in the digital Work Brief: create separate `Requirements` and `Scope, Constraints` fields; ensure "Support and operational model requirements" are explicitly captured under `Requirements`.
- **Urgency:** soon
- **Prompted by:** D1

### N2 - Align "Delivery Owner" wording in ITS Working Policy and related docs
- **Action:** Ensure the ITS Working Policy (and any related guidance) uses the "accountable vs responsible" framing for Delivery Owner, consistent with the Work Delivery Framework.
- **Urgency:** someday
- **Prompted by:** I1 and D2

## Connections

- D2 -[led_to]-> A1
- I1 -[informed_by]-> D2
- D1 -[related_to]-> A1

## Trail Updates

- Extends trail: `work_delivery_framework` (clarified accountability boundaries and removed PM as a core governance role)
- Extends trail: `digital_workbrief` (field split decision for better definition quality)
