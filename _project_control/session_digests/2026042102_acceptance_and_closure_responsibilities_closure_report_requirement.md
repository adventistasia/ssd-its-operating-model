---
lorespec: "0.1"
id: "2026042102"
date: "2026-04-21"
source: "other"
topic: "Clarify acceptance and closure responsibilities in the ITS Department Working Policy draft (Delivery Owner informs Acceptance Owner; Closure Report required for formal closure)."
tags: [its_department_working_policy, workboard, acceptance, closure, closure_report, delivery_owner, acceptance_owner]
classification:
  type: drafting
  secondary_type: operational
  domains: [operating_model, work_management, governance]
  value: medium
trails: [workboard_policy, its_department_working_policy]
---

## Session Arc

### Started
User requested the policy markdown be placed into a canvas for verbatim editing. (Transcript L3-L5)

### Pivots
- Closure criteria was tightened by making submission of a Closure Report a requirement for formal closure. (Transcript L7-L13)
- Acceptance workflow trigger was clarified: Delivery Owner informs the Acceptance Owner that the delivered work is ready for review, then the Workboard Manager triggers acceptance review. (Transcript L15-L17)

### Ended
User requested a downloadable transcript excluding the canvas contents. (Transcript L19)

## ARTIFACT

### A1 - Updated ITS Department Working Policy draft (acceptance + closure responsibilities)
- **Artifact:** `workboard_policy/its_department_working_policy_draft.md`
- **Change context:** Git commit `a1ac746a18c0a0a2d273c0dcbb580d43c87464d6` (“Clarify acceptance and closure responsibilities”).
- **What changed (high level):**
  - Delivery Owner responsibilities expanded to include informing the Acceptance Owner when work is ready for review and preparing/submitting the Closure Report.
  - Acceptance review trigger clarified to occur after the Acceptance Owner is informed.
  - Formal closure gated on submission of the Closure Report.
- **Source excerpts:**
  - (Transcript L7): "Requirements for closing a work is to have a Closure Report submitted."
  - (Transcript L11): "The Delivery Owner is responsible for writing the Closure Report."
  - (Transcript L15): "The Delivery Owner is responsible for informing the Acceptance Owner that the delivered work is ready for review."

### A2 - Conversation transcript (canvas excluded)
- **Artifact:** `C:\Users\rmicua\Downloads\conversation_transcript.md`
- **What it contains:** A short edit-instruction exchange capturing the closure/acceptance responsibility clarifications without including the canvas contents.
- **Source excerpt (Transcript L19):** "create a downloadable transcript of this conversation but do not include the contents of the canvas in the transcript."

## DECISION

### D1 - Delivery Owner informs Acceptance Owner when delivered work is ready for review
- **Decision:** After declaring delivery is complete, the Delivery Owner informs the Acceptance Owner that the delivered work is ready for review.
- **Issue:** What explicit responsibility triggers acceptance review readiness communication?
- **Positions:**
  - Delivery completion declaration alone is sufficient (not chosen in this session).
  - Delivery completion plus explicit notification to Acceptance Owner (chosen).
- **Arguments:** Not fully stated in transcript; captured as an explicit responsibility assignment.
- **Warrant:** Acceptance review should be initiated only after the Acceptance Owner has been explicitly notified that review can begin.
- **Qualifier:** in this case
- **Status:** settled
- **Source excerpt (Transcript L15):** "The Delivery Owner is responsible for informing the Acceptance Owner that the delivered work is ready for review."

### D2 - Closure Report submission is required before a work may be formally closed
- **Decision:** Formal closure requires that a Closure Report is prepared and submitted.
- **Issue:** What documentary evidence is required to formally close work?
- **Positions:**
  - Closure review confirmation is sufficient (not chosen in this session).
  - Closure review confirmation plus Closure Report submission (chosen).
- **Arguments:** Not fully stated in transcript; captured as a closure requirement.
- **Warrant:** A work is not “closed” unless closure documentation exists and is submitted as part of the control process.
- **Qualifier:** in this case
- **Status:** settled
- **Source excerpts:**
  - (Transcript L7): "Requirements for closing a work is to have a Closure Report submitted."
  - (Transcript L11): "The Delivery Owner is responsible for writing the Closure Report."

### D3 - Delivery Owner is accountable for preparing and submitting the Closure Report
- **Decision:** Delivery Owner is accountable for preparing and submitting the Closure Report.
- **Issue:** Who owns the Closure Report deliverable?
- **Positions:**
  - Workboard Manager prepares the Closure Report (not chosen in this session).
  - Acceptance Owner prepares the Closure Report (not chosen in this session).
  - Delivery Owner prepares/submits the Closure Report (chosen).
- **Arguments:** Not fully stated in transcript; captured as an explicit accountability assignment.
- **Warrant:** Closure documentation is part of delivery accountability, and should be owned by the role accountable for delivery outcomes.
- **Qualifier:** in this case
- **Status:** settled
- **Source excerpt (Transcript L11):** "The Delivery Owner is responsible for writing the Closure Report."

## REFERENCE

### R1 - Prior related digest: ITS Department Working Policy draft (baseline)
- **Reference:** `_project_control/session_digests/2026042101_its_department_working_policy_workboard_governance.md`
- **Why relevant:** Captures the broader policy draft context and the initial acceptance/closure workflow framing that this session tightens.

## Connections

- D1 -[led_to]-> A1
- D2 -[led_to]-> A1
- D3 -[led_to]-> A1
- A1 -[related_to]-> R1
- A2 -[related_to]-> A1

## Trail Updates

- Extends trail: `workboard_policy` (workboard governance policy edits and clarifications)
- Extends trail: `its_department_working_policy` (acceptance/closure responsibilities and closure criteria)

