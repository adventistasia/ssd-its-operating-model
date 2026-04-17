---
lorespec: "0.1"
id: "2026041204"
date: "2026-04-12"
source: "other"
topic: "Resolved A09: scaling rules for small-work vs large-work with two-tier model and single-factor classification trigger"
tags: [work-delivery-framework, ambiguity-resolution, scaling, A09]
classification:
  type: "drafting"
  secondary_type: "strategy"
  domains: [work-delivery-framework, process-design]
  value: "high"
trails: [work-delivery-framework]
---

## Session Arc

### Started
The session resumed the sequential ambiguity-resolution process for the Work Delivery Framework Specification. A09 (Scaling rules for simple versus complex work) was the next unresolved item in the prioritized plan. The assistant reviewed both the specification and resolution plan, then began an interview to resolve A09.

### Pivots
- The user narrowed classification factors to four: scope, effort/complexity, business impact, and external involvement — rejecting risk level and regulatory/compliance exposure.
- When probed on primary vs secondary factors, the user identified scope, effort/complexity, and business impact as the primary large-work drivers, with external involvement as relevant but not forcing.
- Single-factor trigger (OR logic) was confirmed: any one primary factor at "large" forces large-work classification.
- Greenfield was confirmed as an always-forcing scope criterion, even for single-team projects.
- Business impact uses OR logic across three sub-criteria: cross-department, material impact, or requires approved budget.
- The user rejected a middle tier, confirming only two tiers (small-work and large-work).
- For gate passage, the user chose "same gates, but more can be passed quickly" rather than skipping or merging gates.
- For small-work conditional artifacts, the user decided only the Work Brief is required; additional artifacts are at Delivery Owner/team discretion with no automatic upgrade mechanism.
- Classification documentation was explicitly not required; reclassification is required if thresholds are exceeded mid-stream.

### Ended
A09 was resolved and both files updated. The specification now includes Section 2.7 with the full scaling model including YAML. The resolution plan was updated with A09 checked off (9 of 17 resolved). The session was beginning A10 (Acceptance criteria and observable validation model) when the user requested a LORE extraction.

## DECISION

### D1
- Decision: Adopt a two-tier scaling model (small-work and large-work) with single-factor OR classification.
- Issue: How the framework balances rigor with usability across work of varying size, scope, and complexity.
- Positions: Multi-tier (3+); two-tier with combination triggers; two-tier with single-factor triggers.
- Arguments: Two tiers keeps the model simple; single-factor OR logic ensures nothing large slips through as small; greenfield always large because even simple greenfield carries foundational design risk.
- Warrant: If a single primary dimension (scope, business impact, or effort/complexity) is large, the project carries enough risk or breadth to warrant the full artifact and gate model.
- Qualifier: for this framework's definition of "large"
- Status: settled
- Source: "single-factor trigger" (Transcript user response to Question 3)

### D2
- Decision: All gates apply to small-work, with a quick-pass profile for lighter-evidence gates.
- Issue: Whether small-work should skip gates, merge gates, or keep all gates with faster passage.
- Positions: Same gates lighter evidence; condensed gate path; same gates with quick-pass.
- Arguments: Keeping all gates preserves the control model; quick-pass acknowledges that small-work can satisfy many gates efficiently without bypassing them.
- Warrant: If the control model is the same for all work, consistency is maintained while allowing proportionate evidence.
- Qualifier: for small-work that genuinely stays within its classification
- Status: settled
- Source: "same gates, but more can be passed quickly" (Transcript user response to Question 7)

### D3
- Decision: Small-work requires only the Work Brief; conditional artifacts are at Delivery Owner discretion.
- Issue: Whether triggering a conditional artifact (e.g., security impact) should force upgrade to large-work or stay in small-work with appended artifacts.
- Positions: Force upgrade to large-work; stay small-work with appended artifacts; Delivery Owner decides.
- Arguments: The user's intent is that small-work stays small unless the primary classification factors change; conditional artifact triggers are handled pragmatically by the team.
- Warrant: If conditional artifacts alone don't change the fundamental size/complexity of the work, they shouldn't force a tier change.
- Qualifier: provided the primary classification factors remain small
- Status: settled
- Source: "Delivery owner and the team will make a judgment call on what other artifacts will be required" (Transcript user response to Question 9)

### D4
- Decision: Reclassification from small-work to large-work is mandatory when thresholds are exceeded mid-stream.
- Issue: Whether initial classification is final or can be revisited.
- Positions: Classification is final; reclassification allowed.
- Arguments: Work can grow; the framework must accommodate scope creep or newly discovered complexity without leaving it in an under-governed tier.
- Warrant: If the work genuinely exceeds small-work thresholds, the governance model should reflect that reality regardless of initial classification.
- Qualifier: when primary forcing factors are triggered after initial classification
- Status: settled
- Source: "yes, the work should be reclassified" (Transcript user response to Question 10)

## PATTERN

### P1
- Pattern: Single-factor classification with conservative default.
- Steps: (1) Define primary forcing factors; (2) Apply OR logic — any single factor at "large" triggers large-work; (3) When uncertain on judgment-based factors, default to the more rigorous tier.
- Scope: local (this framework's scaling model)
- Source: "single-factor trigger" and "Default to large-work" (Transcript user responses to Questions 3 and 5a)

## ARTIFACT

### A1
- Artifact: Section 2.7 (Scaling rules for small-work vs large-work) added to `work_delivery_framework_specification.md`.
- Summary: New section with subsections on tiers (2.7.1), classification factors (2.7.2), classification timing (2.7.3), reclassification (2.7.4), small-work gate passage profile (2.7.5), small-work conditional artifacts (2.7.6), and machine-consumable YAML (2.7.7). Also updated boundary note in Section 2.4, packaging note in Section 2.5.2, and Authorization applicability note in Section 2.4.
- Evolution: Replaced the placeholder "scaling unresolved" notes that referenced A09 as still open.
- Source: All edits applied to `work_delivery_framework_specification.md` (Transcript L~assistant-edit-operations)

## NEXT_STEP

### NS1
- What: Resolve A10 (Acceptance criteria and observable validation model) — the next ambiguity in the prioritized sequence.
- Prompted by: A09 completion; resolution plan priority order 10.
- Urgency: now
- Source: Resolution plan priority order and session flow (Transcript assistant's transition to A10)

### NS2
- What: Resolve A17 (Critical stage-defining artifact mapping) — deferred but depends on A09 and A08 (both now resolved).
- Prompted by: Gate YAML definitions still contain `TBD-DEFERRED-TO-A17` placeholders.
- Urgency: soon
- Source: Resolution plan line 96-107 and specification gate YAML blocks (Transcript L299, L318, L335, L352, L370, L387, L402, L418)

## OPEN_QUESTION

### OQ1
- Question: What format should acceptance criteria take (BDD, structured statement, free-form testable, or other)?
- Blocks: A10 resolution
- Partial progress: Question was posed to user but not answered before LORE extraction was requested.
- Source: "What should acceptance criteria look like in practice?" (Transcript assistant Question 1 of A10)

## Connections

D1 --[led_to]--> D2
D1 --[led_to]--> D3
D1 --[led_to]--> D4
D1 --[led_to]--> A1
P1 --[instance_of]--> D1
D2 --[led_to]--> A1
D3 --[led_to]--> A1
D4 --[led_to]--> A1
A1 --[led_to]--> NS1
A1 --[led_to]--> NS2
NS1 --[depends_on]--> A1

## Trail Updates

- Extends `work-delivery-framework`.
- A09 is the 9th of 17 ambiguities resolved. 8 remain (A10, A11, A12, A13, A14, A15, A16, A17).
- Links to prior session `2026041203` (A08 completeness model resolution) since A09 depended on A08.
