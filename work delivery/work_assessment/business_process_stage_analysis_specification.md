# Business Process Stage Analysis Specification

## 1. Purpose and Intended Outcome

The Business Process Stage Analysis breaks a business process into the stages that matter to understanding how work actually flows today.

It exists to make stage-by-stage flow, roles, inputs, data use, outputs, handoffs, dependencies, and control points visible without turning the assessment into solution design. A useful Business Process Stage Analysis is practical, current-state focused, and specific enough that later analysis and definition do not need to rediscover how the work moves now.

The intended outcome is that assessment and definition practitioners can see how the relevant business process works today, where material friction or control points sit, and what current-state realities must be carried forward.

## 2. When It Is Required

This artifact is situational within Work Assessment.

Use it when the current business process materially shapes the work request and a simple current-state summary is not enough to show:

- where work starts and ends
- who performs or receives each stage
- where key handoffs, dependencies, or controls exist
- where pain, delay, rework, or uncertainty appears in the flow

## 3. Intended Readers and Users

- Assessment Owner
- analysis lead or business analysis lead
- requester subject matter experts and process participants
- sponsor or Outcome Owner candidate
- ITS reviewers who need to understand process flow before work proceeds
- practitioners preparing later Work Definition artifacts

## 4. Intended Project Context

Use this artifact during Validation Assessment or focused analysis when the work request is strongly shaped by how a business process currently operates.

It is most useful when the assessment needs a structured view of real operating flow but does not need a full process redesign document.

## 5. How Much Detail to Include

Include enough detail to make the real stage-by-stage flow understandable to someone who did not observe the process directly.

At minimum, the analysis should make visible:

- the major stages in the current process
- the purpose of each stage
- who performs or materially influences the stage
- what inputs, data, and outputs matter
- what decisions, controls, handoffs, dependencies, or exceptions shape flow

The governing principle is:

> Show how the work flows today in enough detail to support assessment and later definition, but stop before redesigning the process or prescribing the future solution.

## 6. Required Content or Minimum Structure

### 6.1. Analysis identity and scope

Must include:

- process or workflow name
- business unit, service, or operational area covered
- Assessment Owner or analysis lead
- date or version
- clear statement of where the process view starts and ends

### 6.2. Process purpose and trigger

Must include:

- what the process is meant to achieve today
- what event, request, condition, or control trigger starts the process
- what event, record, or outcome usually marks the process as complete

### 6.3. Stage list

Must include:

- the stages in the order they normally occur
- clear stage names that reflect the current process rather than future-state ideas

Use as many stages as needed to make the flow understandable, but do not split the process into unnecessary micro-steps.

### 6.4. Stage purpose

For each stage, must include:

- what the stage exists to accomplish
- why the stage matters in the overall flow where that would not otherwise be obvious

### 6.5. Stage actors and participation

For each stage, must include:

- the primary actor
- supporting actors or participating roles where materially relevant
- any role with a control, approval, or gatekeeping function where relevant

### 6.6. Stage inputs and sources

For each stage, must include:

- the required input
- the usual source of that input
- any known dependency, prerequisite, or timing condition that materially affects the stage

### 6.7. Data used or processed

For each stage, must include:

- the main data, record, or information used or updated
- any data quality, completeness, or availability issue that materially shapes the work

### 6.8. Stage activity description

For each stage, must include:

- a short description of what happens at that stage
- any notable variation, exception, or workaround that materially changes how the stage operates

### 6.9. Decision points, controls, and outputs

For each stage, must include:

- the key decision point or control point where relevant
- the record, document, state change, or outcome produced
- the next handoff or receiving stage where relevant

### 6.10. Material handoffs, dependencies, and exceptions

Must include:

- the handoffs most likely to create delay, misunderstanding, duplication, or loss of control
- any cross-team, cross-system, or external dependency that materially shapes flow
- any known exception path important enough to affect the assessment recommendation

### 6.11. Assessment-use notes

Must include:

- the current-state findings from the stage analysis that matter for Work Assessment
- what later definition should carry forward rather than rediscover
- explicit note of any area that still needs deeper validation if the work proceeds

## 7. What to Keep Out

Keep the following out of this artifact:

- future-state process design
- target operating model design
- detailed business requirements
- detailed solution requirements
- automation logic or system design
- implementation sequencing or delivery planning

## 8. Relationships to Other Artifacts

This artifact is usually a supporting input to the [Current State Analysis Report](current_state_analysis_report_specification.md).

It may also support the [Validation Assessment](validation_assessment_specification.md) and the [Work Assessment Report](work_assessment_report_specification.md) where process flow materially shapes the recommendation.

## 9. Ownership, Review, and Acceptance Expectations

The Assessment Owner or analysis lead usually prepares this artifact with input from the people who actually perform, receive, supervise, or control the process.

Review it with process participants and the requester's subject matter experts so the analysis reflects what really happens rather than the ideal process description.

## 10. Maintenance Expectations

This artifact is usually stable within the assessment once the current-state understanding is accepted.

Update it if the process boundary, stage logic, or material current-state facts change during the assessment, or if a reviewer identifies that the documented flow does not reflect actual practice.

## 11. Validation Guide

- Does the stage analysis show how the business process actually flows today rather than how it is supposed to work on paper?
- Are the stage names, purposes, actors, inputs, data, activities, outputs, and handoffs visible enough to support later analysis?
- Are material decisions, controls, dependencies, and exceptions shown where they affect the work request?
- Does the artifact stop short of redesigning the process or prescribing the future solution?
- Is it clear what current-state findings later definition should carry forward?

## 12. Prompt Guide for Drafting the Artifact

### 12.1. Starter prompt

> Draft a Business Process Stage Analysis for the business process most relevant to this work request.
> Break the current process into practical stages and, for each stage, show the stage name, purpose, primary actor, supporting roles where relevant, required input, usual source, data used or processed, what activity happens, any key decision or control point, what output or state change is produced, and any material handoff, dependency, or exception.
> Keep it focused on how the work flows today and do not turn it into future-state design or implementation planning.

### 12.2. Section prompts

> Rewrite the stage descriptions so each stage explains what currently happens, who is involved, what input is needed, and what output is produced without implying a future-state design.

> Add a short note for each material handoff or control point explaining why it matters to the assessment recommendation or later definition.

### 12.3. Validation prompts

> Check whether this Business Process Stage Analysis would help a later team understand the real current flow without needing to interview the same people again immediately.

> Rewrite any section that behaves like a redesigned process, a detailed requirement set, or a delivery plan.
