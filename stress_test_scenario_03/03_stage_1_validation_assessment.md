# Stage 1 Validation Assessment

Status: working draft  
Stage: Stage 1 - Work Assessment  
Specification used: [Validation Assessment Specification](../work_delivery/work_assessment/validation_assessment_specification.md)

## 1. Assessment identity

- Opportunity / work name: SSD staff itinerary status control
- Assessment Owner: Delivery Owner / Project Manager (simulated)
- Sponsor or sponsor candidate: Angie, Sponsor and budget holder
- Primary organizational beneficiary: SSD office operations, committee secretariat, and administrative coordination
- Assessment timebox: short-form simulation assessment, same-day working draft

## 2. Refined statement of need

SSD office staff need a reliable, low-maintenance visibility tool that tells them whether a staff member is away on an approved itinerary, away on leave, or expected to be in the office, without relying on fragmented conversations or manual reconstruction.

The issue matters now because current coordination relies on interruptions, inconsistent updates, and unofficial assumptions. Frequent itinerary revisions make the latest status easy to lose.

## 3. Business alignment, outcome, and success measures

The request aligns with operational visibility, reduction of repeated follow-up, clearer support coordination, improved traceability of staff availability signals, and stronger auditability for status changes.

Success measures for later definition include fewer follow-up interruptions, fewer scheduling delays, visible distinction between approved itinerary, leave, and in-office status, and a visible who / what / when / why trail for every status change.

Angie is willing to sponsor the work if the control model is explicit, the ownership story is clean, and the work does not become a free-form data mashup.

## 4. Current-state snapshot

- itinerary information has an official approval path, but visibility is poor
- leave information lives in a separate owner path
- office staff currently infer availability from mixed informal and formal channels
- itinerary revisions occur and are easy to lose track of
- duplicate encoding risk is already visible
- audit and records concerns are real, not theoretical

## 5. Scope boundaries

Likely in scope for further definition:

- a staff-facing status control app or controlled visibility solution
- itinerary status precedence logic
- leave status visibility
- latest-approved-record display
- revision history and audit trail
- role-based update and approval rules

Out of scope at this stage:

- full HR leave-management redesign
- travel expense and liquidation workflow redesign
- enterprise attendance management
- ad hoc spreadsheet ownership
- any build that cannot preserve auditability

## 6. High-level requirements and capabilities

Any viable solution appears to need to show whether a staff member is on an approved itinerary, on leave or vacation, or otherwise expected in office; show the next known return or office date; show whether the displayed status is based on the latest valid approved or authoritative record; preserve prior itinerary versions and changes; enforce role-based update and approval rules; and keep a visible audit trail for status-affecting changes.

## 7. Viable options

| Option | Summary | Advantages | Drawbacks |
| --- | --- | --- | --- |
| Do nothing | keep the current informal coordination pattern | no setup effort | confusion, interruptions, and unreliable status continue |
| Shared sheet / simple tracker | fast manual visibility tool | low effort, quick to launch | weak authority control, weak revision discipline, high drift risk |
| Structured Microsoft 365 tracker | list/form/workflow-based tracker | better status control, history, permissions, and traceability | still needs clear rule ownership and source-of-truth decisions |
| Custom app | tailored workflow, status precedence, and audit logging | strongest long-term control and auditability | higher cost and more governance work |

Working preference from the assessment: a custom app is the best fit if the work proceeds, because the business rules and auditability needs are too specific for a casual tracker.

## 8. Risk and feasibility check

Sponsorship is low to moderate risk because Angie is willing to sponsor if the governance model is explicit. Strategy fit is low risk. Security and privacy are moderate risk because leave status and travel details are personal information. Operational sustainability is moderate risk because the app must not depend on one person manually reconciling sources. Delivery feasibility is low to moderate risk if source precedence, update rules, and acceptance ownership are settled.

Overall risk signal: moderate.

## 9. Cost of inaction

Impact level: High.

The current process wastes time repeatedly, the office remains exposed to status disputes, audit and records confidence stays weak, and the same questions will keep being answered manually.

## 10. Known dependencies and timing constraints

- sponsor confirmation
- Outcome Owner confirmation
- Acceptance Authority confirmation
- clarification of itinerary-source ownership
- clarification of leave-source ownership
- decision on status precedence and conflict handling
- security and privacy review
- records retention and audit expectations

## 11. Validation recommendation

Recommendation: Proceed to focused analysis.

Rationale: the need is real, sponsor willingness exists if governance is clear, and the source-of-truth, precedence, and audit questions are too important to skip.

## 12. Decision record

- Decision authority: simulated ITS leadership / delegated governance authority
- Decision taken: proceed to focused analysis
- Decision date: 2026-04-10
- Evidence basis used: Initial Review, stakeholder interviews, Delivery Owner synthesis
- Notes / conditions:
  - keep the next assessment pass decision-focused
  - define source precedence before any build assumption is made
  - determine whether the work needs a full Initiative Definition Document
- Follow-up owner: Delivery Owner / Project Manager

## 13. Handoff notes

- Jane is the requestor, not a sufficient sponsor
- Angie is a viable sponsor candidate and is willing to invest if governance is clear
- likely Outcome Owner should be the office operations owner, not the technical team
- likely Acceptance Authority will need to cover business usefulness, records correctness, and auditability
- this work is already trending beyond a Work Brief
- definition must decide whether the solution is a custom app, a controlled workflow, or a reporting layer over multiple authoritative sources
