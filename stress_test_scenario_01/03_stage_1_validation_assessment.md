# Stage 1 Validation Assessment

Status: working draft  
Stage: Stage 1 - Work Assessment  
Specification used: [Validation Assessment Specification](../work_delivery/work_assessment/validation_assessment_specification.md)

## 1. Assessment identity

- Opportunity / work name: SSD staff itinerary tracker
- Assessment Owner: Delivery Owner / Project Manager (simulated)
- Sponsor candidate: Angie, the Sponsor
- Primary organizational beneficiary: SSD office operations and administrative coordination
- Assessment timebox: short-form simulation assessment

## 2. Refined statement of need

SSD office staff need a reliable, low-maintenance visibility tool that tells them whether a staff member is away on an approved itinerary, away on leave, or expected to be in the office, without relying on fragmented conversations or manual reconstruction.

The issue matters now because current coordination relies on interruptions, inconsistent updates, and unofficial assumptions.

## 3. Business alignment, outcome, and success measures

### 3.1. Business alignment

The request aligns with:

- operational visibility
- reduction of repeated follow-up
- clearer support coordination
- improved traceability of staff availability signals

### 3.2. Desired outcome

Office staff can answer basic availability questions quickly using one trusted view that distinguishes:

- approved itinerary
- leave / vacation
- expected in office

### 3.3. Success measures

Potential success indicators for later definition:

- fewer follow-up interruptions to confirm staff whereabouts
- fewer scheduling delays caused by unclear availability
- visible distinction between approved itinerary, leave, and in-office status
- displayed status tied to a dated approved or authoritative record

### 3.4. Sponsorship signal

Angie is skeptical of overbuild, but she is a real sponsor signal. That matters because she is pushing the work toward a proportionate solution rather than a large new system.

## 4. Current-state snapshot

Current-state signals from the stakeholder conversations:

- itinerary information is held through an official recorder and is not yet visible in the needed operational form
- leave information is held in a separate owner path
- office staff currently infer availability from mixed informal and formal channels
- itinerary revisions can be lost if the latest approved version is not visible
- duplicate encoding risk is already visible

No separate Current State Analysis Report was created because the current-state picture was understandable enough for a small-item assessment.

## 5. Scope boundaries

### 5.1. Likely in scope for further definition

- a staff-facing status tracker for SSD staff availability
- distinction between itinerary status, leave status, and expected in-office status
- visibility of latest valid source-backed record
- handling of itinerary revision visibility

### 5.2. Out of scope at this stage

- full travel approval workflow redesign
- finance liquidation workflow redesign
- HR leave-management redesign
- enterprise attendance management
- mobile application development
- custom application build unless justified later

### 5.3. Key assumptions

- itinerary approval records already exist in some official form
- leave records already exist in some separate official form
- the first useful release can be a controlled visibility layer rather than a full transaction platform

## 6. High-level requirements and capabilities

Any viable solution appears to need to:

- show whether a staff member is on an approved itinerary
- show whether a staff member is on leave or vacation
- show whether a staff member is otherwise expected in office
- show the next known return or office date
- show whether the displayed status is based on the latest approved or authoritative record
- avoid parallel unofficial versions of the same itinerary
- make revisions visible instead of silently overwriting them

## 7. Viable options

| Option | Summary | Advantages | Drawbacks |
| --- | --- | --- | --- |
| Do nothing | keep the current informal coordination pattern | no setup effort | confusion, interruptions, and unreliable status continue |
| Shared sheet / simple tracker | fast manual visibility tool | low effort, quick to launch | weak authority control, weak revision discipline, high drift risk |
| Structured Microsoft 365 tracker | list / form / workflow-based tracker | better status control, history, permissions, and traceability | still needs clear rule ownership and source-of-truth decisions |
| Custom app | tailored workflow and logic | strongest long-term control | disproportionate for the current request size |

Working preference from the assessment: structured Microsoft 365 tracker is the best current direction if the work proceeds.

## 8. Risk and feasibility check

### 8.1. Sponsorship

Risk signal: moderate.

Reason: Angie is now visible, but the sponsor role still needs to stay proportionate and explicit.

### 8.2. Strategy / organizational fit

Risk signal: low.

Reason: the problem is practical and aligned to operational visibility.

### 8.3. Security / privacy

Risk signal: moderate.

Reason: leave status and travel details may require access boundaries and minimum disclosure rules.

### 8.4. Operational sustainability

Risk signal: moderate.

Reason: the tracker must not depend on one person maintaining it informally.

### 8.5. Delivery feasibility

Risk signal: low to moderate.

Reason: technically feasible, but blocked by business-rule clarity.

### 8.6. Funding

Risk signal: low.

Reason: likely small if built on existing Microsoft 365 capability, but still unconfirmed.

### 8.7. Overall risk signal

Overall: moderate.

The work itself is small. The main risks are governance and data authority, not platform feasibility.

## 9. Cost of inaction

Impact level: moderate.

Rationale:

- the current process wastes time repeatedly
- coordination is slowed
- trust in status information remains weak

## 10. Known dependencies and timing constraints

- sponsor identification
- outcome owner identification
- acceptance authority identification
- clarification of leave-record ownership
- decision on whether the tracker is a reporting view only or also a submission / revision tool

## 11. Validation recommendation

Recommendation: proceed to focused analysis.

Rationale:

- the need is credible
- a lightweight solution is plausible
- the unresolved source-of-truth, ownership, and revision questions are too important to skip

## 12. Decision record

- Decision authority: simulated ITS leadership / delegated governance authority
- Decision taken: proceed to focused analysis
- Decision date: 2026-04-10
- Evidence basis used: Initial Review, stakeholder interviews, Delivery Owner synthesis
- Conditions / follow-up:
  - keep the next assessment pass small and decision-focused
  - determine whether a Work Brief is still the likely next artifact
  - identify acceptance and source-of-truth implications before definition
- Follow-up owner: Delivery Owner / Project Manager

## 13. Handoff notes

- Jane is the requestor, not the sponsor
- Angie is the sponsor signal and is pushing for proportionate control
- the likely outcome owner is an office operations owner, not the technical team
- the Acceptance Authority may be split unless definition explicitly resolves the record-correctness question
- the work still appears small enough for a Work Brief
