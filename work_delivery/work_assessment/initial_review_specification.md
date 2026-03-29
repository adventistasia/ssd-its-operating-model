# Initial Review Specification

## 1. What This Artifact Is For

The Initial Review makes a fast, disciplined IT-side decision on whether a request, problem, risk, or opportunity is worth any further assessment effort.

It exists to stop weak, unsupported, misaligned, or low-value work early before the organization spends time on deeper validation. It is also a quick sanity check on whether the request broadly aligns with what the organization does. A useful Initial Review is short, practical, and explicit about why the work should stop, defer, or proceed.

Intended readers include the Assessment Owner, requestor or submitter, sponsor candidate, ITS intake or governance leads, and decision-makers who need a quick triage view.

## 2. When to Use It

This artifact is required at the start of Work Assessment for any proposed planned work that may need governance, definition, or later authorization.

Use it as the front-door screening record for potential planned work when the IT team needs to decide quickly whether a request is worth the time to assess further and whether it broadly fits organizational mandate and direction.

This document should be understandable in minutes. It is not a mini business case and not a project approval document.

## 3. Stage Fit and Handoffs

This artifact is used in **Stage 1 (Work Assessment)** as the first gate in the assessment process.

Upstream sources:

- Work request, problem report, risk escalation, or manager instruction that triggered the intake.

Downstream artifacts:

- [Challenges and Needs Specification](challenges_and_needs_specification.md) — may be used before or alongside this artifact where the request needs clearer problem framing.
- [Validation Assessment Specification](validation_assessment_specification.md) — receives this artifact if the item proceeds.

## 4. Before You Start

Make sure you have:

- a description of the request, problem, risk, or opportunity
- the name or role of the requestor or source
- a named Assessment Owner
- enough context to check basic organizational fit and obvious stop signals

If these inputs are absent or unclear, treat the output as a working draft only.

## 5. How to Draft It

1. Record the review identity: title, requestor, date, and Assessment Owner.
2. Write the statement of need in plain language — what the problem or opportunity is and why it surfaced now.
3. State the desired outcome as an improvement, not as a solution.
4. List the current challenges or friction points visible at this stage.
5. Identify the affected parties and explain why the issue matters if left unresolved.
6. Assess the cost of inaction directionally: low, moderate, or high, with a brief rationale.
7. Check strategic and organizational fit and flag any obvious stop signals or dealbreakers.
8. Make an explicit recommendation: stop, defer, or proceed to Validation Assessment.

## 6. Minimum Structure

### 6.1. Review Identity

Must include:

- request or opportunity title
- requestor or source
- date identified
- Assessment Owner

### 6.2. Statement of Need

Must include:

- the problem, risk, or opportunity that exists today
- the trigger or reason it surfaced now

### 6.3. Desired Outcome

Must include:

- a short outcome-focused statement of what would be better if the issue were addressed

### 6.4. Current Challenges or Friction Points

Must include:

- the main blockers, pain points, or conditions making the issue difficult today

### 6.5. Who Is Affected and Why It Matters

Must include:

- primary stakeholders or users affected
- why the issue matters if left unresolved

### 6.6. Cost of Inaction

Must include:

- the likely consequence of doing nothing over the next 12 to 24 months
- a directional impact level such as low, moderate, or high
- a brief rationale

### 6.7. Strategic and Organizational Fit

Must include:

- a quick view of whether the item aligns with strategy, priorities, mandate, known risks, or stakeholder support
- brief note where fit is weak or unclear

### 6.8. Obvious Constraints or Dealbreakers

Must include:

- any factor that would immediately make further assessment unjustified

### 6.9. Initial Feasibility Sanity Check

Must include:

- a very high-level view of whether the work appears feasible, clearly infeasible, or unclear without deeper assessment

### 6.10. Review Recommendation

Must include one explicit recommendation:

- stop
- defer
- proceed to Validation Assessment

Include a brief rationale.

### 6.11. Decision Record

Must include:

- decision authority
- decision taken
- decision date
- evidence basis used for the decision
- notes or conditions if applicable
- owner for each follow-up action where conditions are set

## 7. Writing Rules

Keep it brief. Include only enough detail to understand:

- what the need is
- why it matters
- who is affected
- whether it broadly aligns with organizational direction and mandate
- whether obvious stop signals exist
- what should happen next

The governing principle is:

> Capture enough to support a clear triage decision. Do not deepen analysis unless the item earns the right to move forward.

Keep the following out:

- solution design
- detailed requirements
- detailed option analysis
- vendor comparisons
- estimates or schedules beyond basic triage observations
- detailed risk mitigation planning

## 8. Traceability, Ownership, and Review

The Assessment Owner usually prepares this artifact as a quick IT-side review with input from the requestor and any immediately relevant stakeholders.

The triage decision should be confirmed by the relevant ITS lead, intake governance owner, or other delegated decision-maker.

This artifact traces forward to the [Validation Assessment Specification](validation_assessment_specification.md) if the item proceeds.

## 9. Done When

This artifact is ready when:

- the need is understandable without specialist knowledge
- the desired outcome is written as an outcome rather than a solution
- the affected parties and cost of inaction are visible enough to support triage
- obvious dealbreakers have been checked rather than ignored
- the recommendation is explicit and attributable
- the decision record is complete

## 10. What Comes Next

1. If the recommendation is to **proceed**, open the [Challenges and Needs Specification](challenges_and_needs_specification.md) to sharpen the problem basis where needed.
2. Move to the [Validation Assessment Specification](validation_assessment_specification.md) to test business alignment, sponsorship, and the case for focused analysis.
3. If the recommendation is to **stop or defer**, record the decision, assign follow-up ownership where conditions apply, and close the item or schedule a re-review date.

## 11. Prompt Guide

Starter prompt:

```text
Draft an Initial Review for a proposed work item.
Summarize the need, desired outcome, who is affected, the cost of inaction, obvious dealbreakers, and a clear recommendation to stop, defer, or proceed to Validation Assessment.
Keep it concise, practical, and free of solution design.
```

Validation prompt:

```text
Check whether this Initial Review functions as a fast triage record rather than a business case or design brief.
Rewrite any section that drifts into design, requirements, or premature analysis.
```
