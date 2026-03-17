# Work Brief Specification

## 1. Purpose and Intended Outcome

The Work Brief is a short control record for a discrete piece of work.

Use it to make the work clear before delivery starts, keep it visible while it is in progress, and confirm who owns delivery, acceptance, and decision-making.

It is lighter than an Initiative Definition Document but stronger than a task note or Kanban card title.

By reading the brief, people should be able to answer:

- what problem or need this work addresses
- what outcome and deliverables are expected
- what is in scope and out of scope
- who requested it
- who owns value, delivery, acceptance, and decision authority
- what decision has been made about the work
- what evidence will show the work is complete

## 2. When It Is Required

Use a Work Brief when work is small enough to be governed as a discrete work item rather than as a full initiative, but important enough that ownership, scope, decision, and closure must be explicit.

Typical use cases include:

- a small standalone improvement, change, investigation, or tightly related piece of work
- a work order inside a larger initiative
- a discrete deliverable package within an approved initiative
- a task-sized unit of controlled delivery that needs visible ownership and acceptance

## 3. When It Is Not Enough

The Work Brief is not the right primary artifact when the work is large enough that it needs a broader governance baseline across multiple related deliverables, multiple dependent work briefs, material budget or operating-cost commitments, or material change to systems, services, data, security posture, support load, or organizational operating model.

If Definition shows that the work is larger than first understood, the Work Brief should either:

- be superseded by an Initiative Definition Document, or
- become a child work brief under a newly defined initiative

The point of conversion is to preserve clarity, not to punish early underestimation.

## 4. Intended Readers and Users

- requester
- Outcome Owner
- Delivery Owner
- Acceptance Owner or Acceptance Authority
- Decision Authority
- delivery team or implementer
- ITS leadership and management
- operations and support where impacted
- future maintainers or reviewers

## 5. Intended Project Context

Use this artifact from initial definition through formal closure for one controlled work item.

The Work Brief may operate in either of the following contexts:

- as the primary governing artifact for a genuinely small standalone piece of work
- as an inner work control artifact inside a parent initiative, deliverable set, or delivery stream

Where it sits inside a larger initiative, it should reference the parent initiative or parent deliverable baseline and should not redefine the initiative's overall scope or authorization.

## 6. How Much Detail to Include

Include enough detail to make the work item understandable, actionable, reviewable, and closeable without turning the brief into an Initiative Definition Document, Project Charter, detailed design, or task plan.

The governing principle is:

> Include enough information to let the right people agree on the work, start the work intentionally, track it visibly, and accept it formally. Put deeper design, build, or operational detail in referenced artifacts when needed.

The Work Brief should usually stay short. For most work items, one concise markdown document should be enough.

## 7. Required Content or Minimum Structure

### 7.1. Work identity and control

Must include:

- work brief title
- work brief ID where used
- current status
- current stage
- date raised
- last updated date
- requester
- parent initiative, parent deliverable, or parent work reference where applicable
- work classification

Recommended status values:

- Draft
- Defined
- Approved
- In Delivery
- Delivered
- Closed
- Deferred
- Rejected
- Converted

Recommended stage values:

- Define
- Decide
- Deliver
- Close

This section lets the work item function as a visible control record on or behind the Kanban board.

### 7.2. Outcome, need, and success

Must include:

- plain-language statement of the problem, request, or need
- intended outcome
- success criteria or acceptance focus
- consequence of not doing the work where relevant

This section explains why the work exists and what "good" looks like.

### 7.3. Scope boundaries

Must include:

- in-scope content
- out-of-scope content
- assumptions
- constraints

This section is the main boundary control for the work item.

### 7.4. Roles and accountability

Must include:

- requester
- Outcome Owner
- Delivery Owner
- Acceptance Owner or Acceptance Authority
- Decision Authority

Where helpful, also include:

- implementer or delivery contributors
- operational owner
- support owner

Control rule: acceptance ownership must be explicit before delivery starts. It may not be implied from the Outcome Owner or Delivery Owner unless the same person is named in both roles.

### 7.5. Deliverables and acceptance evidence

Must include:

- the discrete deliverables or outputs required for this work item
- Delivery Owner for each deliverable where different
- Acceptance Owner or Acceptance Authority for each deliverable where different
- acceptance evidence or acceptance focus for each deliverable
- current status where helpful

Recommended columns:

| Deliverable | Description | Delivery Owner | Acceptance Owner | Acceptance Evidence / Focus | Status | Reference |
| ----------- | ----------- | -------------- | ---------------- | --------------------------- | ------ | --------- |
|             |             |                |                  |                             |        |           |

This section turns the work item from intent into an accountable delivery commitment.

### 7.6. Risks, dependencies, and supportability

Must include:

- material risks or constraints that could affect delivery or outcome
- key dependencies or prerequisites
- support, operational, security, privacy, recovery, or sustainability concerns where relevant

This section keeps small work from bypassing practical operational thinking.

### 7.7. Decision record

Must include:

- decision being requested
- Decision Authority
- decision taken
- decision date
- rationale
- conditions or risk acceptance where applicable

Recommended decision values:

- Approve
- Defer
- Reject
- Convert to Initiative Definition

No delivery work begins without a recorded decision.

### 7.8. Delivery and board control

Must include enough visibility to support stage movement and management review.

Recommended content:

- current Kanban stage or lane
- target completion date where used
- blocked or waiting indicator where relevant
- links to child tasks, tickets, or implementation records where used
- note of any material scope, owner, or decision change

The Work Brief may remain a concise summary and control point even when detailed tasks are tracked elsewhere.

### 7.9. Closure and acceptance

Must include:

- closure criteria
- acceptance confirmation
- closure date
- post-delivery owner where relevant
- references to supporting evidence or resulting artifacts

Control rule: work is not closed simply because execution tasks are complete. It is closed when the named acceptance authority confirms that the defined outcome and deliverables have been met.

## 8. Scaling and Relationship to Parent Initiatives

Multiple Work Briefs may exist under one initiative.

When used inside a larger initiative or deliverable set, a Work Brief should:

- reference the parent initiative or deliverable baseline
- inherit higher-level scope and authorization constraints from the parent
- define only the discrete inner work item being controlled
- avoid restating the full initiative case, budget, or governance baseline unless needed for local understanding

Use the Work Brief like a controlled work order inside the parent structure, not like a parallel initiative-definition artifact.

## 9. Conversion Rule

If the work item grows during Definition such that it no longer behaves like a discrete inner work item, the brief should record a decision to convert or escalate.

Conversion indicators include:

- the work now spans multiple workstreams or multiple dependent work briefs
- the work requires broader scope, funding, or authorization decisions
- the work materially changes service ownership, security posture, support load, or operating model
- leadership needs a broader outcome and deliverable baseline than the brief can reasonably hold

When conversion happens, the Work Brief should remain as the traceable originating record and should reference the superseding Initiative Definition Document.

## 10. What to Keep Out

Keep the following out of this artifact unless the work is genuinely so small that no separate artifact is warranted:

- full business cases
- detailed architecture or configuration
- full project schedules
- detailed task-by-task execution plans
- repeated copies of downstream deliverables
- runbooks and SOPs in full
- large decision narratives better kept in separate decision records

## 11. Relationships to Other Artifacts

This artifact should align with:

- [ITS Work Management Model](../its_work_management_model.md)
- [Initiative Definition Document Specification](../work%20delivery/governance_and_control_deliverables/initiative_definition_document_specification.md)
- [Work Delivery Framework](../work%20delivery/work_delivery_framework.md)
- relevant deliverable specifications under [work delivery](../work%20delivery)

For small standalone work, the Work Brief may be the main controlling artifact.

For work inside a larger initiative, it should sit below the parent initiative baseline and above detailed implementation tasks.

## 12. Ownership, Review, and Acceptance Expectations

The Delivery Owner usually coordinates the document with input from the requester, Outcome Owner, Acceptance Owner, and Decision Authority.

The brief should be reviewed early enough that scope, ownership, and acceptance are agreed before delivery starts.

The Decision Authority confirms whether the work is authorized to proceed.

The Acceptance Owner or Acceptance Authority confirms whether the work can be closed.

## 13. Maintenance Expectations

This artifact should be updated when any of the following changes:

- scope boundaries
- named owners
- decision status
- target dates where materially tracked
- closure basis
- conversion or escalation outcome

It should remain short, current, and usable as a live control artifact throughout the work item's life.

## 14. Validation Guide

- Does the brief make the work understandable without extra verbal explanation?
- Is the requester visible and are accountability roles explicit?
- Is acceptance ownership named before delivery starts?
- Is the work item's scope small and discrete enough for a Work Brief rather than an Initiative Definition Document?
- If this work sits inside a larger initiative, is the parent reference visible?
- Could management see what the work is, who owns it, what stage it is in, and what decision has been made without asking around?
- Could a new implementer or reviewer understand what must be delivered and how it will be accepted?
- If the work has grown, does the brief clearly show whether it was converted or escalated?

## 15. Prompt Guide for Drafting the Artifact

### 15.1. Starter prompt

> Draft a Work Brief for a discrete work item.
> Make the work understandable, accountable, visible, and closeable.
> Keep it lighter than an Initiative Definition Document but stronger than a task note.
> Name the requester, Outcome Owner, Delivery Owner, Acceptance Owner, and Decision Authority.
> Define the outcome, scope boundaries, deliverables, acceptance evidence, risks, decision record, and closure basis.
> If the work sits under a larger initiative, reference the parent initiative and keep the brief limited to the inner work item.

### 15.2. Scaling prompt

> Review this Work Brief and determine whether it still behaves like a discrete work item or now needs conversion into an Initiative Definition Document.
> Explain the reason clearly and identify what should remain in the brief versus what should move to the initiative baseline.

### 15.3. Validation prompt

> Check whether this Work Brief works as a practical work-control artifact for a small or inner work item.
> Rewrite any section that behaves like a project charter, detailed design, or task plan.
