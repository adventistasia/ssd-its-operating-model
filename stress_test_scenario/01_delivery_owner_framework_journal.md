# Delivery Owner Framework Journal

Status: working draft  
Perspective: Delivery Owner / Project Manager  
Purpose: show the Delivery Owner's real-time interpretation of the framework rather than a retrospective summary.

## 1. Starting position

The request arrived as a practical office need, not as a defined project.

Immediate uncertainty:

- no named sponsor
- no named Outcome Owner
- no named Acceptance Authority
- no confirmed source of truth for itinerary status
- no clear system owner for leave records
- no stated decision authority for whether this work should proceed

Per [README](../README.md), [ITS Operating Model](../its_operating_model.md), [ITS Work Management Model](../its_work_management_model.md), and the [Work Delivery Framework](../work_delivery/work_delivery_framework.md), that means the safe starting point is Stage 1 rather than jumping to solution drafting.

## 2. Real-time reading path taken

The Delivery Owner followed this repository path:

1. [README](../README.md)
2. [ITS Operating Model](../its_operating_model.md)
3. [ITS Work Management Model](../its_work_management_model.md)
4. [Work Delivery Framework](../work_delivery/work_delivery_framework.md)
5. [Deliverable Specifications Index](../work_delivery/deliverable_specifications_index.md)
6. [Work Assessment Process](../work_delivery/work_assessment/work_assessment_process.md)
7. [Standard Deliverables Guide](../work_delivery/standard_deliverables_guide.md)
8. [Work Brief Specification](../work_delivery/work_brief/work_brief_specification.md)
9. [Delivery Owner Runbook](../work_delivery/delivery_owner_runbook.md)
10. Relevant assessment and solution specifications only as needed

## 3. Early interpretation notes

### 3.1. What the framework made clear quickly

- If the current stage is unclear, start at Stage 1.
- Small work is allowed to use a lighter control set.
- The framework expects explicit ownership and acceptance even for small governed work.
- A [Work Brief](../work_delivery/work_brief/work_brief_specification.md) is the likely scaled definition record if the work remains small enough.

### 3.2. What was not clear immediately

- Whether Stage 1 can stay very lean for a request this small without feeling ceremonial.
- How a Delivery Owner should resolve split authority between office usefulness and record correctness.
- Whether a tracker that combines itinerary and leave status is still one small governed work item or the start of a broader operational data problem.
- Whether minimum Stage 2 content for a Work Brief is enough for a programmer when revision control and record authority are disputed.

## 4. Working hypothesis after first framework pass

Initial view:

- The work appears small in delivery size.
- The work is not small in ownership ambiguity.
- The correct operating move is not to build immediately.
- The correct next step is a right-sized Stage 1 assessment to test whether the work stays small enough for a Work Brief.

## 5. What stakeholder conversations changed

### 5.1. Jane

Jane confirmed the need is immediate and operational, but also pushed back against heavy process.

Effect on Delivery Owner thinking:

- strengthens the case for a lightweight path
- increases urgency for a practical solution direction
- does not remove the need for ownership and source-of-truth clarity

### 5.2. Programmer

The programmer made the hidden complexity explicit:

- source-of-truth choice is unresolved
- revision handling is unresolved
- edit rights and approval logic are unresolved
- a quick build would hard-code an unapproved process

Effect on Delivery Owner thinking:

- confirms this is still small work, but not a "just build a form" request
- suggests a Work Brief alone may be too thin unless it explicitly carries rules, ownership, and acceptance focus

### 5.3. Committee Secretary

The Committee Secretary drew a firm line:

- approved itinerary records must remain the controlling source
- revisions need a visible approval trail
- the tracker cannot display informal assumptions as approved status

Effect on Delivery Owner thinking:

- reduces ambiguity about one part of the source-of-truth issue
- increases delivery friction because Jane wants simplicity while the official recorder wants strict control

### 5.4. Disbursing Accountant

Finance added a second pressure:

- timeliness matters
- incomplete records create follow-up waste
- a lightweight first release is acceptable if status is current and searchable

Effect on Delivery Owner thinking:

- confirms usefulness can improve before the full process is perfected
- suggests the first delivery should be a reporting and visibility solution, not a full approval engine

## 6. Path chosen through the framework

The Delivery Owner chose this path:

`Stage 1 Work Assessment -> recommend proceed -> Stage 2 Work Definition using a Work Brief -> stop before formal authorization and detailed design become authoritative`

Why:

- The framework clearly says not to guess the stage and to start at Stage 1 when unclear.
- The work still looks small enough for one controlled record.
- A full Initiative Definition Document felt too heavy for the request as currently framed.
- The unresolved ownership and source-of-truth questions are significant, but they do not yet justify a full initiative pack.
- The main delivery risk is not technical complexity. It is ambiguity in business rules and record authority.

## 7. Main Delivery Owner judgment during the exercise

The framework was usable enough to orient the work.

The difficult part was not the stage model. The difficult part was deciding how much documentation is enough once the work is obviously small but still contains genuine governance questions.

That tension shaped the rest of this scenario.
