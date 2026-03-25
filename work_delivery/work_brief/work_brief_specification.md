# Work Brief Specification

## 1. Purpose

The Work Brief is the ITS standard tool for defining work. It gives each piece of work a clear purpose, scope, ownership, and delivery control, whether the work stands alone or sits inside a larger initiative.

Use it to show the problem, need, or intended outcome, make the work clear before delivery starts, keep it visible while it is in progress, and confirm who owns delivery, acceptance, and decisions.

It is lighter than an Initiative Definition Document but stronger than a task note, chat thread, or Kanban card title.

## 2. When to Use It

Use a Work Brief when the work is small enough to manage as one item, but important enough that scope, ownership, decision, and closure need to be clear.

For standalone governed work, the brief should normally be created from the completed Stage 1 assessment output rather than from raw intake notes.

For that reason, Stage 2 should normally carry forward the validated need, intended outcome, success measures, scope boundary, preferred path, key risks, key dependencies, and owner signals already established in Stage 1.

Stage 2 does not need to rediscover those basics. It does need to confirm, complete, and formalize the work-level control details that assessment may only indicate at signal level, especially:

- Acceptance Authority
- deliverables and acceptance evidence
- parent or child governance position
- operational and support ownership where relevant
- any approval conditions that must become explicit before delivery starts

Within the Work Delivery Framework, it is mainly used as:

- a scaled Stage 2 Work Definition artifact for small governed work
- a supporting Stage 3 authorization artifact for that same small work
- a live control record through Stage 6 and Stage 7 for that same small work
- a child work order under an approved initiative during delivery

Common use cases:

- a small standalone improvement, change, investigation, or correction
- a work order inside a larger initiative
- a controlled deliverable package within an initiative
- a task-sized item that needs visible ownership and formal acceptance

## 3. When Not to Use It

Do not use a Work Brief as the main control record when the work is too large, too broad, or too dependent to behave like one clear work item.

Escalate to an Initiative Definition Document when:

- the work spans multiple workstreams or multiple dependent work briefs
- the work needs broader funding, scope, or approval decisions
- the work materially changes service ownership, security posture, support load, or operating model
- leadership needs a broader record than a brief can hold clearly

If this happens, keep the Work Brief as the originating record and reference the superseding Initiative Definition Document.

## 4. How It Fits with Larger Initiatives

Multiple Work Briefs may sit under one initiative.

In that case, the Work Brief acts like a work order inside the parent initiative or deliverable set. It should:

- reference the parent initiative, deliverable, or work package
- stay within the parent scope and approval boundaries
- define only the specific piece of work being controlled
- avoid restating the full initiative case unless needed for local clarity

In Work Delivery Framework terms:

- use the Work Brief in Stage 2 when the work is small enough that a full Initiative Definition Document would be too heavy
- use the Work Brief in Stage 3 as part of the approval basis for that small work
- keep using the same Work Brief through Stage 6 and Stage 7 as the live control record
- use child Work Briefs under a parent initiative when one initiative contains multiple controlled work items

## 5. Minimum Content

Every Work Brief must include the following.

### 5.1. Work details and visibility

- work brief title
- work brief ID where used
- current status
- current stage
- date raised
- last updated date
- parent initiative or parent deliverable reference where applicable
- board or tracking reference where used

### 5.2. Why the work exists

- problem, request, or need
- intended outcome
- success criteria or what acceptance will focus on
- consequence of not doing the work where relevant

### 5.3. Scope boundaries

- in scope
- out of scope
- assumptions
- constraints

### 5.4. Named owners

- requester
- Outcome Owner
- Delivery Owner
- Acceptance Authority
- Decision Authority

Acceptance Authority must be named before delivery starts.

### 5.5. Deliverables and acceptance

For each deliverable, record:

- what must be produced
- who owns delivery
- who accepts it
- what evidence shows it is complete

### 5.6. Risks and dependencies

- material risks or constraints
- dependencies or prerequisites
- access requirements
- operational, support, security, privacy, or recovery concerns if they matter

### 5.7. Decision log

Keep a decision log in the Work Brief to record important decisions made about the work item over time.

At minimum, each decision log entry should include:

- decision being requested or made
- decision taken
- Decision Authority
- decision date
- artifact or evidence basis used for the decision
- rationale
- conditions or risk acceptance where applicable
- owner for each follow-up action

No delivery work starts without a recorded approval decision.

### 5.8. Closure and acceptance

- closure criteria
- acceptance confirmation
- closure date
- resulting owner where relevant
- references to evidence or resulting artifacts

Work is not closed just because tasks are finished. It closes when the named acceptance authority confirms that the required outcome and deliverables have been met.

## 6. Suggested Status and Stage Values

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

Suggested decision values for the work-level authorization entry:

- Approve
- Approve with Conditions
- Defer
- Reject

Suggested stage values for the Work Brief operating view:

- Define
- Decide
- Deliver
- Close

Practical stage mapping to the Work Delivery Framework:

- Define -> Stage 2 (Work Definition)
- Decide -> Stage 3 (Work Authorization)
- Deliver -> Stage 6 (Work Delivery)
- Close -> Stage 7 (Acceptance, Transition & Closure)

## 7. What to Keep Out

Keep the Work Brief focused. Do not turn it into:

- a full business case
- an Initiative Definition Document
- a Project Charter
- a detailed design
- a full task plan
- a runbook or SOP

If more detail is needed, link to the right supporting document.

## 8. Maintenance Standard

Update the Work Brief when any of the following change:

- scope boundaries
- named owners
- decision status
- target dates where materially tracked
- closure basis
- escalation or conversion outcome

The brief should stay short, up to date, and usable throughout the life of the work item.

## 9. Quick Check

A Work Brief is working properly if:

- a team member can understand the work quickly without extra verbal explanation
- management can see what the work is, who owns it, and what stage it is in
- Acceptance Authority is explicit
- delivery does not start on assumed approval
- the brief is short enough to stay current
- the work can be escalated cleanly if it grows beyond work-brief level

## 10. Related References

Use this standard alongside:

- [ITS Work Management Model](../../its_work_management_model.md)
- [Initiative Definition Document Specification](../governance_and_control_deliverables/initiative_definition_document_specification.md)
- [Work Delivery Framework](../work_delivery_framework.md)
- [Work Brief Form](work_brief_form.md)
