# Validation Assessment Specification

## 1. Purpose and Intended Outcome

The Validation Assessment tests whether a screened opportunity is strong enough to justify focused analysis.

It exists to validate business alignment, test sponsorship, confirm the primary organizational beneficiary, confirm outcomes and success measures, clarify current state, scope boundaries, stakeholder needs, and high-level requirements, compare conceptual options, and identify obvious kill risks before more effort is invested. A useful Validation Assessment is evidence-based enough to support a stop, defer, or proceed decision without becoming a design pack.

The intended outcome is that only opportunities with credible need, plausible sponsorship, clear organizational value, and manageable risk move into focused analysis.

## 2. When It Is Required

This artifact is required for work that passes the Initial Review and needs a stronger evidence base before deciding whether to invest in focused analysis.

## 3. Intended Readers and Users

- Assessment Owner
- sponsor or sponsor candidate
- outcome owner candidate
- requester's subject matter experts and immediate team
- ITS leadership or governance reviewers
- subject matter contributors needed to test risk or feasibility

## 4. Intended Project Context

Use this artifact in the middle of Work Assessment after the request survives initial triage but before the organization decides whether to do focused analysis.

## 5. How Much Detail to Include

Include enough detail to answer five practical questions:

- is the need real and current
- is the work aligned with business and organizational interests
- is there a real sponsor willing to take the initiative
- what must any viable answer be able to do
- what broad approaches exist
- what major risks or feasibility concerns are visible now
- is focused analysis justified

The governing principle is:

> Add enough evidence to decide whether focused analysis should happen, but stop short of detailed definition, design, or planning.

## 6. Required Content or Minimum Structure

### 6.1. Assessment Identity

Must include:

- opportunity or work name
- Assessment Owner
- sponsor or sponsor candidate
- primary organizational beneficiary or interest served
- assessment timebox

### 6.2. Refined Statement of Need

Must include:

- a concise validated summary of the problem, risk, or opportunity
- why the matter is important now

This section should be informed by the [Challenges and Needs](challenges_and_needs_specification.md) artifact so the validated need remains traceable to the original challenge, visible impacts, and underlying unmet need.

### 6.3. Business Alignment, Outcome, and Success Measures

Must include:

- how the work aligns with business or organizational interests
- the meaningful change expected if the opportunity is addressed
- the success measures or indicators that would show the work was worthwhile

Where no sponsor is willing to own and advocate for the initiative, treat this as a major red flag.

### 6.4. Current-State Snapshot

Must include:

- the relevant current systems, workflows, constraints, dependencies, or prior attempts that shape the opportunity

Where current-state understanding cannot be captured reliably in a short summary, reference a supporting [Current State Analysis Report](current_state_analysis_report_specification.md) and, where relevant, a [Business Process Stage Analysis](business_process_stage_analysis_specification.md).

### 6.5. Scope Boundaries

Must include:

- what appears in scope for further analysis
- what is clearly out of scope at this stage
- key assumptions or boundary conditions

### 6.6. High-Level Requirements and Capabilities

Must include:

- a short list of what any viable solution must be able to do
- any material stakeholder requirements, conditions, or non-negotiables already visible at this stage

These requirements or capabilities must be:

- outcome-oriented
- technology-agnostic
- concise enough to support option comparison
- light enough to guide later definition without behaving like detailed specifications

### 6.7. Viable Options

Must include:

- at least one credible path forward
- the do-nothing option
- key advantages and drawbacks for each option

### 6.8. Risk and Feasibility Check

Must include:

- a practical signal check across sponsorship, strategy, security, privacy, compliance, operational sustainability, delivery feasibility, and funding
- an overall risk signal

### 6.9. Cost of Inaction

Must include:

- likely effect of not acting in the next 12 to 24 months
- directional impact level
- brief rationale

### 6.10. Known Dependencies and Timing Constraints

Must include:

- known dependencies, sequencing constraints, funding-cycle issues, policy timing, or external readiness concerns

### 6.11. Validation Recommendation

Must include one explicit recommendation:

- stop
- defer
- proceed to focused analysis

Include rationale and optional relative priority where useful.

### 6.12. Decision Record

Must include:

- decision authority
- decision taken
- decision date
- evidence basis used for the decision
- notes or conditions where applicable
- owner for each follow-up action where conditions are set

### 6.13. Handoff Notes

Required when the item proceeds.

Must include:

- key context to carry forward
- assumptions that need testing
- priority risks or constraints
- stakeholder sensitivities or history that the later analysis should not rediscover
- key stakeholder groups and their material needs or requirements to carry forward
- likely sponsor, Outcome Owner candidate, and Delivery Owner candidate signals where known
- early signal on whether the work appears likely to remain small enough for a Work Brief or is more likely to require an Initiative Definition Document
- likely Acceptance Authority or a clear note that acceptance ownership is still unresolved
- operational or support ownership signals where service impact already appears likely

## 7. What to Keep Out

Keep the following out of this artifact:

- detailed requirements
- detailed scope definition
- detailed design
- implementation plans or schedules
- vendor evaluation packs
- full mitigation plans or full business cases

## 8. Relationships to Other Artifacts

This artifact builds on the [Initial Review](initial_review_specification.md).

It should normally be informed by the [Challenges and Needs](challenges_and_needs_specification.md) artifact.

It may also use supporting assessment inputs such as:

- [Current State Analysis Report](current_state_analysis_report_specification.md)
- [Business Process Stage Analysis](business_process_stage_analysis_specification.md) where stage-by-stage process flow materially shapes the assessment

If the item proceeds, it justifies focused analysis and provides input to the later [Work Assessment Report](work_assessment_report_specification.md).

## 9. Ownership, Review, and Acceptance Expectations

The Assessment Owner usually prepares this artifact with focused input from the requester's subject matter experts, immediate team, sponsor candidate, affected stakeholders, and any subject matter leads needed to test obvious risks or feasibility concerns.

The proceed/defer/stop decision should be confirmed by the relevant ITS leadership or delegated governance authority.

## 10. Maintenance Expectations

This artifact is usually stable once the recommendation and decision are recorded. If significant new information changes the opportunity materially before the final assessment is completed, update the artifact or issue a new version so the change is visible.

## 11. Validation Guide

- Is the need validated enough to justify or reject focused analysis?
- Is business alignment clear?
- Is there a willing sponsor, or is the lack of sponsorship being treated as a major red flag?
- Are the primary organizational beneficiary, desired outcomes, success measures, scope boundaries, and current-state constraints visible?
- Are the high-level requirements or capabilities outcome-oriented and free of design detail?
- Are credible options compared, including doing nothing?
- Are major risk and feasibility concerns visible?
- Does the recommendation clearly state whether the item should stop, defer, or proceed?

## 12. Prompt Guide

### 12.1. Starter Prompt

```
Draft a Validation Assessment for a proposed work item that has passed initial triage.
Validate business alignment, sponsorship, the primary organizational beneficiary, desired outcomes, success measures, current state, scope boundaries, stakeholder needs, high-level requirements or capabilities, viable options, major risk and feasibility signals, cost of inaction, and a clear recommendation to stop, defer, or proceed to focused analysis.
Keep it evidence-based, practical, and free of detailed design or delivery planning.
```

### 12.2. Section Prompts

```
Rewrite the high-level requirements or capabilities so they describe what a viable solution must do without naming technology, implementation detail, or vendor choices.
```

```
Compare the conceptual options in a short table that includes advantages, drawbacks, and the do-nothing option.
```

### 12.3. Validation Prompts

```
Check whether this Validation Assessment supports an evidence-based decision on whether focused analysis should happen without drifting into Work Definition.
```

```
Rewrite any section that behaves like a requirement set, design brief, or implementation plan.
```
