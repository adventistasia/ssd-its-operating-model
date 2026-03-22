# Business Process Stage Analysis Specification

## 1. Purpose and Intended Outcome

The Business Process Stage Analysis makes the current business process visible stage by stage so later assessment and definition do not have to guess how the work actually flows today.

It exists to show the real flow of work, who does what, what inputs and records are used, where decisions or controls happen, and what outcomes or handoffs each stage produces. A useful Business Process Stage Analysis helps the team understand the present business process without drifting into process redesign, solution design, or implementation planning. It should also make cross-stage handoffs, dependencies, and exception paths visible enough that later assessment does not have to rediscover them.

The intended outcome is that Work Assessment can reference a clear stage-by-stage view of the current business process where that understanding materially affects the recommendation, scope boundary, supportability view, or later definition work.

## 2. When It Is Required

This artifact is situational within Work Assessment.

Use it when the work request materially depends on understanding a business process across stages, handoffs, decision points, controls, or multiple participating roles.

It is most commonly justified when:

- the request affects a business workflow rather than one isolated task
- delays, rework, duplication, or missed controls appear between stages
- multiple teams, business units, or records are involved
- later definition will need a reliable view of how the current process actually operates

It is usually unnecessary when the current process can be explained accurately in a short narrative inside the Validation Assessment or Current State Analysis Report.

## 3. Intended Readers and Users

- Assessment Owner
- analysis lead or business analyst
- requester's subject matter experts
- process owner or service owner
- sponsor or sponsor candidate
- practitioners who later prepare the Work Assessment Report or Work Definition artifacts

## 4. Intended Project Context

Use this artifact for process-driven work where the current flow of activities matters to understanding the problem, unmet need, control issue, or service impact.

It is especially useful when the request involves:

- operational process friction
- handoff failures
- unclear ownership between stages
- control or record weaknesses
- workflow exceptions that materially shape the work request

This is an assessment artifact. It should describe the current process as it operates today, not the desired future process.

## 5. How Much Detail to Include

Include enough detail to let a reader understand how the process moves from one stage to the next and where the important actors, inputs, records, decisions, outputs, and handoffs sit.

Do not try to document every edge case, every task instruction, or every exception path. Focus on the stages that materially shape the work request, the visible pain points, and the facts that later assessment or definition should not need to rediscover.

Keep the stage fields explicit. Do not collapse purpose, actors, inputs, activities, outputs, and handoffs into vague narrative if that would hide how the process actually operates.

If a diagram is used, choose the lightest diagram type that answers the assessment question clearly and pair it with short text or a companion table so the meaning stays explicit. Use the [Types of Diagrams Guide](types_of_diagrams_guide.md) when choosing between diagram styles.

The governing principle is:

> Make the current business flow understandable and usable for assessment. Do not turn the artifact into process redesign, operating procedure detail, or solution design.

## 6. Required Content or Minimum Structure

### 6.1. Analysis identity and scope

Must include:

- work item or opportunity name
- process name or process area being analyzed
- Assessment Owner or analysis lead
- business area or service area covered
- analysis boundary showing where the process starts and ends for this assessment
- source basis used, such as interviews, walkthroughs, records, or existing process notes

### 6.2. Process summary

Must include:

- a short plain-language summary of what the process is meant to achieve
- the trigger that starts the process within the assessment boundary
- the normal end point or business outcome produced
- any boundary note explaining what connected upstream or downstream process areas are outside this analysis

### 6.3. Stage-by-stage process analysis

Must include a stage-by-stage structure.

Each stage entry must include:

- stage sequence or identifier
- stage name
- stage purpose
- primary actor
- supporting actors or participating roles where materially relevant
- required input
- usual source of the input
- data used or processed
- stage activity description in plain language
- key decision point or control point where relevant
- record, document, state change, or outcome produced
- notable handoff, dependency, or exception where relevant

The stage entries may be presented as a table or as repeated stage sections, but the fields above must stay visible and consistent.

Where a process diagram is used, it should support the stage analysis rather than replace the required content fields.

### 6.4. Observed process issues and practical notes

Must include:

- the stage-level or cross-stage issues that materially shape the work request
- any visible bottlenecks, duplication, rework, waiting points, ownership gaps, or weak controls
- any important exception path, dependency, or record issue that later analysis should not overlook

This section should point to what is happening today. It should not propose the future solution.

### 6.5. Cross-stage handoffs, dependencies, and exceptions

Must include:

- the handoffs most likely to create delay, misunderstanding, duplication, or loss of control
- any cross-team, cross-system, or external dependency that materially shapes the overall flow
- any known exception path important enough to affect the assessment recommendation or later definition

This section may summarize the most important cross-stage points already visible in the stage entries, but it should bring them together so they are easy to assess as a whole.

### 6.6. Assessment-use summary

Must include:

- the current-process facts that Validation Assessment, Current State Analysis, or the Work Assessment Report should be able to reference directly
- any areas where the process understanding is still partial, disputed, or needs confirmation

### 6.7. Example content showing the minimum structure

Example only. Adapt to the real work request.

**6.1. Analysis identity and scope**

- Work item: Volunteer onboarding delays and inconsistent approvals
- Process name: Volunteer onboarding and approval
- Assessment Owner: ITS business analysis lead
- Business area covered: mission administration and local office approval flow
- Boundary: starts when a volunteer application is submitted and ends when the volunteer is confirmed ready to start
- Source basis: interviews with mission administrators, review of email trails, review of current checklist and approval spreadsheet

**6.2. Process summary**

- Process purpose: move a volunteer from application to confirmed start
- Trigger: volunteer application and supporting documents are received
- End point: volunteer is approved and receives start confirmation
- Boundary note: post-start orientation is outside this analysis

**6.3. Stage-by-stage process analysis**

| Stage | Purpose | Primary actor | Supporting roles | Required input | Usual source | Data used or processed | Activity description | Decision or control point | Output produced | Handoff, dependency, or exception |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1. Intake | capture the request | mission administrator | volunteer applicant | application form and ID documents | applicant email or portal upload | applicant identity, role, location | administrator checks that the submission is complete and logs it | completeness check before review starts | intake record and pending file | incomplete applications are returned for clarification |
| 2. Local review | verify local suitability | local office approver | mission administrator | intake record and supporting documents | mission administrator | applicant details and local placement information | local office reviews the applicant and confirms suitability | local approval or rejection | review decision and comments | delays occur when approver is unavailable |
| 3. Final confirmation | confirm start readiness | mission administrator | HR support staff | local approval and checked documents | local office approver | approval status, required documents, start date | administrator confirms that all required steps are complete and notifies the volunteer | final check that all required documents exist | confirmation notice and updated status | repeated document checking occurs when records are scattered |

**6.4. Observed process issues and practical notes**

- approval waits are longest between intake and local review
- the same documents are checked again during final confirmation because earlier checks are not always visible
- status is tracked in email and spreadsheets rather than one clear record

**6.5. Cross-stage handoffs, dependencies, and exceptions**

- the handoff from intake to local review is the main waiting point
- the process depends on local office approver availability and complete supporting documents
- incomplete applications create a repeat loop back to intake

**6.6. Assessment-use summary**

- current flow depends heavily on mission administrators manually chasing approvers
- status visibility and repeated document checking are likely material causes of delay
- it is still unclear whether all local offices follow the same review path

## 7. What to Keep Out

Keep the following out of this artifact:

- future-state workflow design
- solution architecture or system design
- detailed requirements
- implementation tasks or delivery plans
- detailed procedure manuals or work instructions
- full control redesign or approval matrices

## 8. Relationships to Other Artifacts

This artifact can support the:

- [Validation Assessment](validation_assessment_specification.md)
- [Current State Analysis Report](current_state_analysis_report_specification.md)
- [Work Assessment Report](work_assessment_report_specification.md)
- [Types of Diagrams Guide](types_of_diagrams_guide.md)

It is a supporting assessment artifact, not one of the three core Work Assessment gate artifacts.

If Work Definition proceeds, later artifacts may reference this analysis rather than recreating the same current-process breakdown from scratch.

## 9. Ownership, Review, and Acceptance Expectations

The Assessment Owner or analysis lead usually prepares this artifact with input from the people who perform or oversee the process today.

Where the process materially affects operations, controls, compliance, service delivery, or supportability, the relevant process owner, service owner, or subject matter lead should review it for accuracy.

Formal acceptance is not normally required, but the artifact should be reliable enough to support assessment decisions and later handoff.

Reviewers should check that stage fields remain explicit and that important handoffs or exceptions are not lost inside a simplified diagram or summary.

## 10. Maintenance Expectations

This artifact is usually a point-in-time assessment record.

Update it if the team learns that the stage breakdown, actors, inputs, or outputs were materially wrong or incomplete before the Work Assessment recommendation is finalized.

If the work is deferred and later revisited, refresh the analysis if the underlying process has changed.

## 11. Validation Guide

- Does the analysis show the current process as it actually operates today rather than an ideal or proposed future state?
- Are the stages, actors, inputs, outputs, and handoffs clear enough that another practitioner can understand the flow without major guessing?
- Are the stage entries consistent and complete enough to support later assessment work?
- Are material decisions, controls, dependencies, or exception points visible where they matter?
- Are the most important cross-stage handoffs, dependencies, and exceptions easy to identify without reconstructing them manually?
- Does the artifact stop short of becoming process redesign, requirements, or delivery planning?
- Does it identify which current-process facts should remain easy to reference in later assessment or definition?

## 12. Prompt Guide for Drafting the Artifact

### 12.1. Starter prompt

> Draft a Business Process Stage Analysis for the current-state process relevant to this work request.
> Break the process into stages and show the stage purpose, primary actor, supporting roles where relevant, required input, usual source, data used, activity description, decision or control point where relevant, output produced, and notable handoff, dependency, or exception.
> Then summarize the cross-stage handoffs, dependencies, and exceptions that matter most to the assessment.
> Keep it practical, evidence-based, and focused on the current process rather than future design.

### 12.2. Section prompts

> Rewrite the stage entries so each one describes what actually happens today, who does it, what input is needed, what output is produced, and what handoff or control matters.

> Summarize the cross-stage issues that materially affect the work request without proposing solutions.

> Check whether any important dependency or exception is only implied inside a stage description and make it explicit.

### 12.3. Validation prompts

> Check whether this Business Process Stage Analysis is detailed enough to support assessment and later handoff without becoming a redesign document or operating procedure.

> Rewrite any stage description that assumes a future state, names a solution, or hides the real current handoff, dependency, control, or record issue.
