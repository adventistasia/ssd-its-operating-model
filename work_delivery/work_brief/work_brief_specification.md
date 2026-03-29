# Work Brief Specification

## 1. What This Artifact Is For

The Work Brief is the ITS standard tool for defining any planned work so that the work is understood before it is executed and delivered. It gives every piece of work clear purpose, named ownership, delivery basis, and acceptance criteria — regardless of the size or complexity of the work.

A Work Brief can be used to partially implement the Work Delivery Framework, concentrating on the definition, decision, delivery, and closure elements without requiring the full staged structure a larger initiative would need.

For larger planned work, multiple Work Briefs may be used together — each defining a specific deliverable or discrete work item while staying traceable to the broader purpose of the work.

It is lighter than an Initiative Definition Document but stronger than a task note, chat thread, or Kanban card title.

## 2. When to Use It

Use a Work Brief when the work is small enough to manage as one item, but important enough that scope, ownership, decision, and closure need to be clear.

Escalate to an Initiative Definition Document when:

- the work spans multiple workstreams or dependent Work Briefs that need a governing baseline
- the work needs broader funding, scope, or approval decisions
- the work materially changes service ownership, security posture, support load, or operating model
- leadership needs a broader control record than a brief can hold clearly

When escalating, keep the Work Brief as the originating record and reference the superseding Initiative Definition Document.

## 3. Stage Fit and Handoffs

The Work Brief operates across multiple stages of the Work Delivery Framework. The stage mapping is:

- **Define** → [Stage 2 (Work Definition)](../work_delivery_framework.md): draft, scope, and define the work item
- **Decide** → [Stage 3 (Work Authorization)](../work_delivery_framework.md): record the authorization decision
- **Deliver** → [Stage 6 (Work Delivery)](../work_delivery_framework.md): track delivery progress and maintain evidence
- **Close** → [Stage 7 (Acceptance, Transition & Closure)](../work_delivery_framework.md): confirm acceptance and close the record

Upstream sources:
- [Work Assessment Report Specification](../work_assessment/work_assessment_report_specification.md) — assessment outputs inform the work definition when a Work Brief is the appropriate governance vehicle
- [ITS Work Management Model](../../its_work_management_model.md)

Downstream artifacts or escalation paths:
- [Initiative Definition Document Specification](../governance_and_control_deliverables/initiative_definition_document_specification.md) — the escalation destination when a Work Brief is no longer sufficient
- [Work Delivery Framework](../work_delivery_framework.md) — the governing framework this brief operates within

## 4. Before You Start

Before starting a Work Brief, confirm:
- the work item has a clear triggering request, problem, or need
- a named Outcome Owner is identified or can be named
- a named Acceptance Authority can be confirmed before delivery starts
- the work is appropriately scoped for a Work Brief (not so broad it needs an Initiative Definition Document)
- any relevant work assessment outputs or prior decisions are available to inform scope and ownership

If Outcome Owner or Acceptance Authority cannot be named, treat the brief as a draft until they are confirmed.

## 5. How to Draft It

1. **Complete Document Information** (section 6.1): assign the brief ID, status, stage, and any parent reference.
2. **Name Accountable Owners** (section 6.2): identify Requester, Outcome Owner, Delivery Owner, Acceptance Authority, Decision Authority, and Operational Owner where relevant.
3. **State Why the Work Needs to Be Done** (section 6.3): describe the triggering problem, need, or request and the consequence of inaction.
4. **Define the Intended Outcome and Scope** (section 6.4): describe what success looks like, set the scope boundary, and name the assumptions and constraints.
5. **List the Deliverables** (section 6.5): for each deliverable, state what must be produced, who owns delivery, who accepts it, and what evidence confirms it is done.
6. **Describe the Delivery Basis** (section 6.6): document timing, approach, risks, dependencies, and any operational or compliance considerations.
7. **State the Acceptance Criteria** (section 6.7): define what the Acceptance Authority will check, both per deliverable and for the work as a whole.
8. **Open the Decision Log** (section 6.8): record the authorization decision before delivery starts; log all subsequent significant decisions.
9. **Close the Record** (section 6.9): when delivery is complete, record the Acceptance Authority confirmation, closure date, and any resulting handover.

## 6. Minimum Structure

Every Work Brief must address the following questions in enough detail for the work to be understood, owned, authorized, delivered, and closed.

### 6.1. Document Information

- work brief title
- work brief ID (where used)
- current status and current stage
- date raised and last updated date
- parent initiative or parent deliverable reference (where applicable)
- board or tracking reference (where used)

### 6.2. Who Are the Accountable Owners

Name the people who own and are accountable for the work:

- Requester
- Outcome Owner — accountable for the intended result
- Delivery Owner — accountable for delivery, stage discipline, and evidence
- Acceptance Authority — accountable for confirming that deliverables satisfy the acceptance criteria, and for working with the Outcome Owner to ensure the acceptance criteria are set to produce the intended outcomes and meet the success criteria; must be named before delivery starts
- Decision Authority — authorizes the work to proceed and approves major decisions
- Operational or Support Owner (where relevant)

### 6.3. Why Does This Work Need to Be Done

State the reason the work exists:

- problem, need, or request that triggered the work
- why it needs to be addressed now
- consequence of not doing it (where relevant)

### 6.4. What Is the Intended Outcome and How Will We Know We Achieved It

State what success looks like and how it will be recognized:

- intended outcome — the result the work is expected to produce
- success criteria — how stakeholders will know the outcome has been achieved
- scope boundaries — what is in scope, out of scope, and what assumptions and constraints apply

### 6.5. What Is Going to Be Delivered

List the specific deliverables the work must produce. For each deliverable, record:

- what must be produced
- who owns delivery
- who accepts it
- what evidence confirms it is complete

### 6.6. When and How Is This Going to Be Delivered

Describe the delivery basis — how the work will be organized and executed:

- target completion date or key milestones
- approach or method of delivery
- linked tasks, tickets, or tracking references
- material risks, dependencies, or prerequisites
- access requirements and any operational, support, security, privacy, or recovery considerations (where relevant)

### 6.7. What Is the Acceptance Criteria

State what acceptance means both at the deliverable level and for the work as a whole:

- acceptance criteria for each deliverable (aligned with section 6.5)
- overall acceptance focus — what the Acceptance Authority will check before confirming the work is done
- closure criteria — the specific conditions that must be met before the work can be formally closed

### 6.8. Decision Log

Keep a running decision log for each important decision made about the work. At minimum, record:

- decision being requested or made
- decision taken
- Decision Authority
- decision date
- artifact or evidence basis used
- rationale
- conditions or risk acceptance (where applicable)
- owner for each follow-up action

No delivery starts without a recorded authorization decision.

### 6.9. Closure

When closing the work, record:

- acceptance confirmation from the named Acceptance Authority
- closure date
- resulting owner (where relevant — operational handover, support ownership)
- references to evidence or resulting artifacts
- any remaining follow-up actions and owners

Work is not closed just because tasks are finished. It closes when the named Acceptance Authority confirms that the required outcome, deliverables, and acceptance criteria have been met.

### 6.10. Status and Stage Values

Suggested status values:

- Draft
- Defined
- Approved
- In Delivery
- Delivered
- Closed
- Deferred
- Rejected
- Converted

Suggested stage values for the Work Brief operating path:

- Define
- Decide
- Deliver
- Close

Stage mapping to the Work Delivery Framework:

- Define → Stage 2 (Work Definition)
- Decide → Stage 3 (Work Authorization)
- Deliver → Stage 6 (Work Delivery)
- Close → Stage 7 (Acceptance, Transition & Closure)

Suggested authorization decision values:

- Approve
- Approve with Conditions
- Defer
- Reject

## 7. Writing Rules

Keep the Work Brief focused and current. Include only enough detail for the work to be understood, owned, authorized, delivered, and closed.

Keep the Work Brief focused. Do not turn it into:

- a full business case
- an Initiative Definition Document
- a Project Charter
- a detailed design
- a full task plan
- a runbook or SOP

Link to the right supporting document where more detail is needed.

## 8. Traceability, Ownership, and Review

Update the Work Brief when any of the following change:

- scope boundaries
- named owners
- decision status
- target dates (where materially tracked)
- closure basis
- escalation or conversion outcome

The brief should stay short, up to date, and usable throughout the life of the work item.

The Delivery Owner is accountable for keeping the brief current and accurate. The Acceptance Authority confirms the final closure.

## 9. Done When

A Work Brief is working properly if:

- the work can be understood without extra verbal explanation
- management can see what the work is, who owns it, and what stage it is in
- Acceptance Authority is named and explicit
- delivery does not start without a recorded authorization decision
- the brief is short enough to stay current
- the work can be escalated cleanly if it grows beyond work-brief level

## 10. What Comes Next

Use this standard alongside:

1. [ITS Work Management Model](../../its_work_management_model.md)
2. [Initiative Definition Document Specification](../governance_and_control_deliverables/initiative_definition_document_specification.md)
3. [Work Delivery Framework](../work_delivery_framework.md)
4. [Work Brief Form](work_brief_form.md)
5. Escalate to an [Initiative Definition Document](../governance_and_control_deliverables/initiative_definition_document_specification.md) if the work grows beyond Work Brief scope.

## 11. Prompt Guide

### Starter Prompt

```
Draft a Work Brief for a new planned work item.
Define the purpose, outcome, scope boundaries, deliverables, delivery approach, acceptance criteria, and named owners.
Use the Minimum Structure sections 6.1 through 6.9 as the drafting framework.
Keep it concise — this is a work-level control record, not a full initiative document.
```

### Validation Prompt

```
Review this Work Brief against its specification.
Check: Is the Acceptance Authority named? Is there a recorded authorization decision before delivery? Are scope boundaries visible? Are deliverables linked to acceptance criteria and evidence? Is the brief short enough to stay current through the life of the work?
Identify any missing required fields or sections that would prevent the brief from being used to govern the work.
```
