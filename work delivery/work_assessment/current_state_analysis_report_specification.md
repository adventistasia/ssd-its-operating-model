# Current State Analysis Report Specification

## 1. Purpose and Intended Outcome

The Current State Analysis Report gives a structured, evidence-based view of the current state relevant to a work request.

It exists to show what actually happens today, what systems and workflows are involved, where handoffs and dependencies sit, what constraints and workarounds shape the work, and which current-state facts matter enough to carry into later definition. A useful Current State Analysis Report is grounded in observed or validated evidence, practical for assessment decisions, and explicit about the difference between current-state findings and later recommendations.

The intended outcome is that decision-makers and later definition practitioners can rely on one current-state view rather than reconstructing the same operational facts from scratch.

## 2. When It Is Required

This artifact is situational within Work Assessment.

Use it when the work request depends on a clearer understanding of current operations than a brief snapshot can provide, especially where the assessment needs to show:

- what actually happens today across systems, teams, and handoffs
- what constraints, dependencies, bottlenecks, or workarounds materially shape the work
- what roles, business units, records, and control realities the later definition must not rediscover

## 3. Intended Readers and Users

- Assessment Owner
- analysis lead or business analysis lead
- sponsor or sponsor candidate
- requester subject matter experts and operational leads
- ITS reviewers assessing viability, supportability, and control implications
- practitioners preparing the later Work Definition artifacts

## 4. Intended Project Context

Use this artifact during Validation Assessment or focused analysis when the current-state picture materially affects the assessment recommendation.

It is especially useful when the work spans multiple teams, systems, records, or controls and the current-state facts need to be assembled into one reusable assessment artifact.

## 5. How Much Detail to Include

Include enough detail to make the current state understandable, evidence-based, and usable for later definition.

At minimum, the report should make visible:

- the operational context the work sits inside
- what actually happens today
- what systems, records, handoffs, dependencies, and controls shape the work
- what problems, bottlenecks, duplication, rework, or workaround behavior are visible
- what current-state facts are important enough to preserve for later definition

The governing principle is:

> Describe the current state as it is observed or validated today, make material realities visible, and stop before turning the report into a future-state design, option paper, or transformation roadmap.

## 6. Required Content or Minimum Structure

### 6.1. Report identity and scope

Must include:

- work request or analysis title
- Assessment Owner or analysis lead
- date or version
- business area, service, or operational scope covered
- clear statement of what part of the current state this report covers and what it does not

### 6.2. Evidence basis

Must include:

- the main evidence sources used such as interviews, observation, existing documents, records, metrics, tickets, audits, or prior assessments
- any notable evidence gaps or confidence limits

### 6.3. Current-state overview

Must include:

- a plain-language summary of how the relevant area operates today
- the main trigger, workflow, service, or operational context involved
- the major systems, records, or channels materially involved

### 6.4. Roles, business units, and operational ownership

Must include:

- the roles or teams materially involved in the current state
- the business units or operational areas materially shaping the work
- any visible operational ownership, support ownership, approval ownership, or control ownership relevant to the assessment

### 6.5. Workflows, handoffs, and dependencies

Must include:

- the main workflows or activity patterns relevant to the work request
- the material handoffs between people, teams, systems, or external parties
- the dependencies or prerequisite conditions that shape how work moves today

Reference a [Business Process Stage Analysis](business_process_stage_analysis_specification.md) where one is used.

### 6.6. Systems, records, and data realities

Must include:

- the systems, tools, records, or data sets that materially shape the current state
- any fragmentation, duplication, manual transfer, data quality issue, or access constraint that matters to the work request

### 6.7. Constraints, controls, and operational realities

Must include:

- the policy, compliance, timing, capacity, support, service, or control conditions that materially shape current operations
- any practical condition that makes the current state harder to change, operate, or support than it may first appear

### 6.8. Pain points, bottlenecks, duplication, rework, and workarounds

Must include:

- the major sources of friction visible in the current state
- where delay, duplication, rework, workaround behavior, or avoidable manual effort occurs
- who is most affected and why the issue persists where that is visible

### 6.9. Prior attempts, history, and unresolved issues

Should include where relevant:

- prior initiatives, changes, or local fixes already attempted
- what those attempts improved, failed to improve, or left unresolved
- any stakeholder history or sensitivity that later definition should not rediscover

### 6.10. Assessment implications

Must include:

- the current-state facts that materially shape the Work Assessment recommendation
- the current-state facts that later definition must carry forward
- explicit separation between observed current-state findings and any later recommendation or design decision that still belongs elsewhere

## 7. What to Keep Out

Keep the following out of this artifact:

- target-state architecture
- recommended solution design
- detailed requirements
- implementation sequencing
- full transformation roadmap
- vendor selection material
- broad recommendations that are not grounded in current-state evidence

## 8. Relationships to Other Artifacts

This artifact may be informed by the [Work Request Challenges and Needs](work_request_challenges_and_needs_specification.md) and may reference a [Business Process Stage Analysis](business_process_stage_analysis_specification.md) where process flow needs a separate stage view.

It can support the [Validation Assessment](validation_assessment_specification.md) and the [Work Assessment Report](work_assessment_report_specification.md) by providing a reusable current-state baseline.

## 9. Ownership, Review, and Acceptance Expectations

The Assessment Owner or analysis lead usually prepares this artifact with input from the requester's subject matter experts, operational participants, service or support leads where relevant, and any reviewers needed to confirm control or dependency realities.

Review it with people who know the current operation well enough to challenge an idealized or incomplete picture.

## 10. Maintenance Expectations

Update this artifact if new evidence materially changes the current-state picture during assessment or if a reviewer identifies that the documented current state does not match current practice.

If the work proceeds, keep the accepted version available as a handoff reference for later definition.

## 11. Validation Guide

- Does the report describe what actually happens today rather than an idealized process or a proposed future state?
- Are systems, workflows, handoffs, dependencies, constraints, workarounds, bottlenecks, duplication, and rework visible where they materially shape the work?
- Are the roles, business units, records, and operational ownership realities clear enough to support later definition?
- Is the evidence basis visible enough that a reviewer can understand how the current-state view was formed?
- Does the report clearly separate current-state findings from later recommendations, design choices, or delivery planning?

## 12. Prompt Guide for Drafting the Artifact

### 12.1. Starter prompt

> Draft a Current State Analysis Report for this work request.
> Describe what actually happens today, the relevant systems, workflows, handoffs, dependencies, constraints, controls, workarounds, bottlenecks, duplication, rework, roles, business units, records, and prior attempts where they materially shape the work.
> Make the evidence basis visible, show what current-state facts later definition must carry forward, and keep a clear boundary between observed current-state findings and any future recommendation or design choice.

### 12.2. Section prompts

> Rewrite the current-state summary so it reflects actual observed or validated practice rather than an ideal process description.

> Extract the current-state facts that most materially shape supportability, operational ownership, control, and later Work Definition, and present them as explicit carry-forward points.

### 12.3. Validation prompts

> Check whether this Current State Analysis Report gives a practical, evidence-based current-state baseline without drifting into future-state design or a transformation roadmap.

> Rewrite any section that sounds like a solution recommendation, implementation plan, or detailed requirement set.
