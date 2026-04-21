---
lorespec: "0.1"
id: "2026041206"
date: "2026-04-12"
source: "other"
topic: "Resolved A13 by defining a Delivery Owner-led review model with PMO assurance oversight, trigger-based independent review, and committee-action gate records"
tags: [work-delivery-framework, ambiguity-resolution, A13, review-model, PMO, assurance, audit, lore]
classification:
  type: "drafting"
  secondary_type: "operational"
  domains: [work-delivery-framework, governance, review-process]
  value: "high"
trails: [work-delivery-framework]
---

## Session Arc

### Started
The session focused on the next ambiguity in sequence, `A13 - Review, assurance, and audit mechanism`. The user asked to resolve ambiguities one by one by interview, reach high confidence in intent, then update the specification and resolution plan. The conversation began by selecting a baseline review model for gates and artifact sets.

### Pivots
- The user first selected `Delivery Owner-led review with PMO oversight only` as the baseline review model, but then paused and asked for pros/cons of each review-model option before confirming that choice. Source: "Could we go back to the previous question? Give me pros and cons of each approach." and "2 is good." (Transcript L4-L6)
- PMO oversight was narrowed into a specific assurance role: PMO defines the review standard, assigns the Gate Decision Owner, checks evidence completeness, audits samples, and may intervene on escalation, non-compliance, or dispute. Source: "PMO defines the review standard and audits samples. PMO also assigns Gate Decision Owner and checks evidence completeness. PMO may intervene..." (Transcript L8-L8)
- Independent review was constrained to trigger-based cases only, specifically architecture impact, security/privacy impact, external vendor handoff, and material business/regulatory risk, with required domain signoff when triggered. Source: "Trigger-based only." and "1, 2, 5, 7" and the follow-up authority answer selecting domain signoff required. (Transcript L10-L14)
- The review mechanism was aligned to the existing gate profile from Section 2.7 after clarifying what that profile currently means for small-work vs large-work. Source: "what is this gate profile again?" and "yes I want that" (Transcript L36-L38)
- The user approved the synthesized A13 design and requested both document updates and a session digest. Source: "this looks right. after updating, create a session digest." (Transcript L46-L46)

### Ended
`work_delivery_framework_specification.md` now includes a resolved Section 2.10 defining the A13 review model, and Section 6.12 now states the ambiguity is resolved. `resolution_plan_work_delivery_framework_specification.md` marks A13 resolved, updates progress counts, and sets `A14` as the next active ambiguity.

## DECISION

### D1
- Decision: Use a Delivery Owner-led review model as the default, with PMO acting as the assurance function rather than the default content decision-maker.
- Issue: What review model should govern gate and artifact evaluation in the framework.
- Positions: PMO-led checkpoint; Delivery Owner-led with PMO oversight; panel-style board; lightweight peer review except key gates.
- Arguments: The user preferred local accountability and pragmatic execution over a centralized checkpoint or formal board, while still wanting explicit PMO control rails.
- Warrant: Gate quality is best preserved when decision accountability stays close to delivery, provided the assurance function is explicit and standardized.
- Qualifier: as the framework-wide default model
- Status: settled
- Source: "2" and later "2 is good." (Transcript L3-L6)

### D2
- Decision: PMO's role is to define the review standard, assign the Gate Decision Owner, check evidence completeness, attend every substantive gate review, audit samples, and intervene on escalation, non-compliance, or dispute.
- Issue: What "PMO oversight" should mean in practice.
- Positions: Standards/audits only; countersign selected gates; intervene only on disputes; completeness-only check; hybrid assurance model.
- Arguments: The chosen hybrid creates enforceable assurance and auditability without shifting normal content ownership away from delivery.
- Warrant: The framework needs a durable control function for consistency and audit, but not one that becomes the routine bottleneck for content judgment.
- Qualifier: for substantive gate governance under A13
- Status: settled
- Source: "PMO defines the review standard and audits samples. PMO also assigns Gate Decision Owner and checks evidence completeness. PMO may intervene..." (Transcript L8-L8)

### D3
- Decision: Independent review is trigger-based only, with explicit domain signoff required when triggered.
- Issue: When independent reviewers are mandatory and what authority they should have.
- Positions: Always required at key gates; required at all substantive gates; large-work only; trigger-based only; hybrids.
- Arguments: The user wanted independence only where risk justifies it, and chose architecture impact, security/privacy impact, external vendor handoff, and material business/regulatory risk as the forcing triggers.
- Warrant: Independent review adds value when a specialized risk domain is in play; making it universal would add avoidable bureaucracy.
- Qualifier: within the gate review mechanism defined for A13
- Status: settled
- Source: "Trigger-based only." and "1, 2, 5, 7" and the selected authority rule requiring domain signoff. (Transcript L10-L14)

### D4
- Decision: Review mode must align to the existing Section 2.7 gate profile; substantive gates require live meetings, quick-pass gates require only a Decision Log entry, and substantive gates retain a committee-action style written record.
- Issue: How the review mechanism should map onto the already-defined scaling model and what evidence each gate should retain.
- Positions: Reuse the existing gate profile; define a separate review split; full written record at every gate; Decision Log only except failures; other hybrids.
- Arguments: Reusing the existing gate profile keeps the framework internally consistent and avoids inventing a second gate taxonomy. The user also preferred minimal retention for quick-pass gates and formal disposition-style records for substantive gates.
- Warrant: A single coherent gate model is easier to apply, audit, and consume than separate scaling and review frameworks.
- Qualifier: as encoded in the resolved A13 operating model
- Status: settled
- Source: "yes I want that" plus the related answers selecting live meetings, Decision Log only for quick-pass, and committee-action style for substantive gates. (Transcript L16-L18, L24-L26, L31-L38)

### D5
- Decision: PMO audit findings may reopen a previously passed gate only when a material completeness failure or material control failure is discovered.
- Issue: Whether audits are advisory only or can affect prior gate passage.
- Positions: Never reopen; reopen only for procedural non-compliance; reopen for material completeness/control failure; reopen for any failed audit.
- Arguments: The user wanted real corrective power for significant failures, but not routine instability from minor audit findings.
- Warrant: Audit should protect framework integrity without making all gate passage provisional.
- Qualifier: after a gate has already passed
- Status: settled
- Source: "3" in response to whether PMO audit findings should reopen or invalidate a passed gate for material completeness or control failure. (Transcript L29-L30)

## INSIGHT

### I1
- Insight: The user's preferred control pattern is not "lightweight" in the abstract; it is "local ownership with explicit assurance rails." PMO is present and active, but not the default content approver.
- Domain: governance, review-process
- Confidence: high
- Source: The combined answers defining Delivery Owner-led review, PMO assurance duties, PMO attendance at every substantive gate, and Gate Decision Owner override ability when PMO flags incomplete evidence. (Transcript L6-L8, L41-L44)

### I2
- Insight: The user consistently prefers trigger-based escalation over universal mandatory review. That pattern is likely to recur in later ambiguities involving blockers, AI sufficiency, and anti-bureaucracy guardrails.
- Domain: framework-design, control-model
- Confidence: high
- Source: "Trigger-based only." and the selected trigger list, plus PMO case-by-case handling when a quick-pass gate hits a trigger. (Transcript L10-L14, L39-L40)

## PATTERN

### P1
- Pattern: "Delivery-led, assurance-railed gate review"
- Scope: local
- Steps:
  1. Use the Delivery Owner-led model by default.
  2. Have PMO define the standard, assign the Gate Decision Owner, and check evidence completeness.
  3. Apply substantive vs quick-pass review according to the existing Section 2.7 gate profile.
  4. Trigger independent domain review only when specific risk conditions are present.
  5. Retain a committee-action style record for substantive gates and a Decision Log entry for quick-pass gates.
- Source: The approved A13 synthesis and final document update request. (Transcript L45-L46)

## ARTIFACT

### A1
- Artifact: Updated `work_delivery_framework/work_delivery_framework_specification.md`
- Change: Added Section `2.10 Review, assurance, and audit mechanism (resolved: A13)` and converted Section `6.12` into a resolved-decision summary referencing Section 2.10.
- Purpose: Makes the framework's human review model explicit, enforceable, and machine-consumable.
- Status: complete
- Source: Final approved synthesis plus the user's request to update the specification. (Transcript L45-L46)

### A2
- Artifact: Updated `work_delivery_framework/resolution_plan_work_delivery_framework_specification.md`
- Change: Marked `A13` resolved, added a resolution note, corrected progress counts, and advanced the next active ambiguity to `A14`.
- Purpose: Keeps the ambiguity register and sequence state accurate.
- Status: complete
- Source: User request to update the resolution plan and check off the ambiguity item. (Transcript L1-L1, L46-L46)

### A3
- Artifact: New session digest `session_digests/2026041206_work_delivery_framework_a13_review_assurance_audit_resolved.md`
- Change: Captures the A13 decisions, review pattern, and next-step trail linkage.
- Purpose: Preserve this ambiguity resolution as durable project memory.
- Status: complete
- Source: "after updating, create a session digest." (Transcript L46-L46)

## NEXT_STEP

### NS1
- What: Resolve `A14 - Blocker, risk, and open-issue handling model`.
- Prompted by: The updated resolution plan now lists A14 as the next active ambiguity after A13.
- Urgency: soon
- Source: The updated tracking note in the resolution plan and the user's original instruction to follow the proposed sequence. (Transcript L1-L1, L46-L46)

## Connections

D1 --[led_to]--> D2
D2 --[led_to]--> D4
D3 --[constrains]--> D4
D4 --[led_to]--> A1
D5 --[embedded_in]--> A1
A2 --[led_to]--> NS1
A3 --[extends]--> 2026041205
I1 --[instance_of]--> P1
I2 --[informs]--> NS1

## Trail Updates

- Extends the `work-delivery-framework` trail.
- Builds directly on `2026041205_resolved_a10_a11_acceptance_supportability_and_lore_digest.md`, because the A13 review model now governs how those acceptance and supportability rules are evaluated at gates.
- Establishes a reusable control pattern for later ambiguities: prefer explicit triggers and documented authority over universal mandatory ceremony.

Transcript reference map used in this digest:
- L1: user asked to resolve ambiguities one by one, follow sequence, interview to high confidence, then update spec and plan
- L3-L46: A13 interview, options review, synthesis approval, and session-digest request
