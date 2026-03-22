# Current State Analysis Report Specification

## 1. Purpose and Intended Outcome

The Current State Analysis Report gives a structured, evidence-based view of the current operating reality relevant to the work request.

It exists to document what actually happens today, what systems, workflows, handoffs, records, constraints, and workarounds shape that reality, and which current-state facts matter enough to remain available as reference for later work. A useful Current State Analysis Report makes the present state visible without turning into future-state design, a transformation roadmap, or a full business architecture study. It should be explicit about what has been observed or validated, what is inferred, and where confidence is limited.

The intended outcome is that Work Assessment can rely on a practical current-state baseline that is strong enough to support recommendation, boundary setting, ownership visibility, supportability thinking, and later handoff into Work Definition.

## 2. When It Is Required

This artifact is situational within Work Assessment.

Use it when the current state is too important, contested, or complex to capture reliably inside the short current-state sections of the Validation Assessment and Work Assessment Report.

It is most commonly justified when:

- multiple systems, teams, or business units materially shape the request
- current workflows involve important handoffs, exceptions, or control points
- workarounds, duplication, rework, or prior attempts are materially affecting the case
- supportability, service ownership, operational control, or dependency concerns are visible
- the team needs a stronger evidence base before recommending whether Work Definition should proceed

For simple work, a concise current-state summary inside any of the work assessment forms i.e. initial, validation or full report is usually sufficient.

## 3. Intended Readers and Users

- Assessment Owner
- analysis lead or business analyst
- sponsor or sponsor candidate
- requester SMEs and operational stakeholders
- ITS leadership or governance reviewers
- practitioners preparing the Work Assessment Report or later definition artifacts

## 4. Intended Project Context

Use this artifact during Validation Assessment or focused analysis when the work request depends on a reliable picture of the current environment.

It is especially useful where the request is shaped by:

- existing operational workflows
- system fragmentation
- manual workarounds
- unclear ownership
- control or compliance implications
- service support realities
- prior failed or incomplete attempts

This artifact should reflect the current state that actually exists. It should not normalize broken practices and it should not quietly replace current-state evidence with future-state recommendations.

## 5. How Much Detail to Include

Include enough detail to show what is happening today, what materially shapes it, and why that matters to the work request.

Focus on the current-state facts that influence assessment decisions, scope boundaries, supportability, ownership, risk, or the likely definition path. Keep supporting detail practical and selective rather than encyclopedic.

Make the evidence basis visible enough that a reviewer can understand how the current-state picture was formed and where it is still incomplete.

The governing principle is:

> Document the current reality clearly enough to support assessment and handoff. Do not turn the artifact into a future-state design pack or enterprise-wide diagnostic.

## 6. Required Content or Minimum Structure

### 6.1. Report identity and assessment boundary

Must include:

- work item or opportunity name
- Assessment Owner or analysis lead
- business area, service area, or process area covered
- date or version
- stated boundary of the current-state view, including what is inside and outside this analysis
- source basis used, such as interviews, observations, records, reports, incident history, or existing documentation

This opening section should make the report boundary and evidence basis easy to find without reading the whole document.

### 6.2. Current-state overview

Must include:

- a plain-language summary of how the relevant area operates today
- what the current state is meant to achieve in practice
- the main business units, roles, or functions involved
- the main systems, tools, records, or channels involved where materially relevant

### 6.3. Actual workflows, handoffs, and operational realities

Must include:

- the actual workflow or workflow summary relevant to the request
- the important handoffs between roles, teams, or units
- where the work slows down, loops back, gets duplicated, or depends on manual coordination
- important exceptions, queues, timing realities, or operational conditions that shape the work

Where useful, this section should reference or incorporate the [Business Process Stage Analysis](business_process_stage_analysis_specification.md).

### 6.4. Systems, records, dependencies, and constraints

Must include:

- the systems, tools, records, data sources, or interfaces that materially shape the current state
- notable dependencies on other teams, services, vendors, policies, data quality, approvals, or timing windows
- operational, technical, policy, staffing, or environmental constraints that materially affect the current state

### 6.5. Workarounds, bottlenecks, duplication, rework, and prior attempts

Must include:

- any material workaround or compensating practice currently in use
- visible bottlenecks, duplication, rework, or repeated failure points
- prior attempts, partial fixes, or abandoned efforts where relevant
- why these matter to the current request or recommendation

### 6.6. Roles, ownership, supportability, and control implications

Must include:

- the roles or business units that perform, own, support, or rely on the current state
- where operational ownership, service ownership, or support ownership is clear
- where ownership is unclear, fragmented, or dependent on individuals
- any control, audit, record, or supportability implication that materially shapes the work request

### 6.7. Current-state reference points

Must include:

- the current-state facts that later definition should reference as starting context
- the facts that materially affect scope, requirements framing, supportability, risk, ownership, or deliverable selection
- any important uncertainty, assumption, or disputed point that still needs confirmation

This section should separate observed current-state facts from later recommendations. It should be clear which points are carry-forward facts for later definition and which questions still need validation before design or delivery decisions are made.

### 6.8. Evidence basis and confidence notes

Must include:

- the main evidence sources used
- where the current-state picture is well supported
- where evidence is partial, outdated, anecdotal, or still needs validation
- any material inference, assumption, or confidence limit that affects how findings should be read

### 6.9. Example content showing the minimum structure

Example only. Adapt to the real work request.

**6.1. Report identity and assessment boundary**

- Work item: Volunteer onboarding delays and inconsistent approvals
- Assessment Owner: ITS business analysis lead
- Area covered: volunteer onboarding current state
- Date: 2026-03-22
- Boundary: covers intake, approval, and start confirmation activities; excludes volunteer orientation after approval
- Source basis: interviews, current checklist, approval spreadsheet, sample email threads

**6.2. Current-state overview**

- Today volunteer onboarding is coordinated through email, spreadsheets, and local office checks
- The current state is meant to move volunteers from application to approval and confirmation
- Main roles involved: mission administrators, local office approvers, HR support staff
- Main tools and records: email, spreadsheet tracker, document attachments, local checklists

**6.3. Actual workflows, handoffs, and operational realities**

- Applications are received centrally, checked manually, then sent to local offices for approval
- The main handoff is from mission administration to local office approvers and back again for confirmation
- Work slows down when approvers are unavailable or when applications come back incomplete
- Staff often use follow-up emails to discover status because no shared live status record exists

**6.4. Systems, records, dependencies, and constraints**

- Key records are stored across email threads and one spreadsheet tracker
- The process depends on local office responsiveness and complete document submission
- Constraint: no single workflow or status record is visible across all participants

**6.5. Workarounds, bottlenecks, duplication, rework, and prior attempts**

- Administrators keep personal follow-up notes to track pending approvals
- Bottleneck: local approval waits can remain idle without escalation visibility
- Duplication: supporting documents are checked more than once
- Prior attempt: a shared spreadsheet improved visibility slightly but did not standardize the approval path

**6.6. Roles, ownership, supportability, and control implications**

- Mission administrators coordinate the work but do not fully control local response times
- Local office approvers own their decision step but not the full end-to-end flow
- Ownership of the full onboarding outcome is not clearly assigned
- Control implication: approval evidence is harder to trace when decisions sit in email

**6.7. Current-state reference points**

- current flow is fragmented across email and spreadsheet tools
- end-to-end ownership is not explicit
- local review delays and repeated document checking materially shape the problem
- the current-state picture is strong for central administration but still needs confirmation across all local offices

**6.8. Evidence basis and confidence notes**

- Strong evidence: mission administrator interviews and sample approval records
- Medium evidence: local office variation, based on a limited sample of offices
- Open point: whether all offices use the same review criteria

## 7. What to Keep Out

Keep the following out of this artifact:

- target-state design
- solution recommendations presented as settled decisions
- detailed requirements
- implementation sequencing or delivery planning
- detailed vendor analysis
- enterprise-wide architecture content that does not materially affect this request

## 8. Relationships to Other Artifacts

This artifact can support the:

- [Validation Assessment](validation_assessment_specification.md)
- [Work Assessment Report](work_assessment_report_specification.md)
- [Business Process Stage Analysis](business_process_stage_analysis_specification.md)

It should help make the current-state summary in those gate artifacts more reliable and more reusable.

If the work proceeds, later definition artifacts should reference this current-state analysis rather than rediscovering the same facts from scratch.

## 9. Ownership, Review, and Acceptance Expectations

The Assessment Owner or analysis lead usually prepares this artifact with input from operational stakeholders, subject matter experts, and any relevant service, support, data, security, or compliance contributors.

Where the current state materially affects ownership, supportability, service continuity, or controls, the relevant owner or lead should review the report for practical accuracy.

Formal acceptance is not normally required, but the report should be reliable enough to support the assessment recommendation and later handoff.

Reviewers should challenge any section that reads like a recommendation without a clear current-state basis behind it.

## 10. Maintenance Expectations

This artifact may be a living assessment document while Validation Assessment or focused analysis is underway.

Update it when material current-state facts change, when major evidence gaps are closed, or when previously assumed ownership, workflow, or dependency information turns out to be wrong.

Once the Work Assessment recommendation is finalized, the report normally becomes a point-in-time assessment record.

## 11. Validation Guide

- Does the report describe what actually happens today rather than an idealized or recommended future state?
- Are the material workflows, handoffs, workarounds, bottlenecks, duplication, constraints, and dependencies visible?
- Are the roles, business units, records, and systems that shape the work request clear enough for assessment use?
- Are supportability, ownership, and control implications visible where they matter?
- Does the report clearly distinguish observed current-state facts from later recommendations or design choices?
- Is the evidence basis visible enough to show what was observed or validated and where confidence is limited?
- Does it identify which current-state facts should remain easy to reference from the Work Assessment Report or later definition?
- Is the detail practical and bounded rather than drifting into a full redesign or architecture pack?

## 12. Prompt Guide for Drafting the Artifact

### 12.1. Starter prompt

> Draft a Current State Analysis Report for this work request.
> Describe what actually happens today, the relevant systems, workflows, handoffs, dependencies, constraints, workarounds, bottlenecks, duplication, rework, ownership realities, support implications, and prior attempts where relevant.
> Make clear which current-state facts later definition should be able to reference directly.
> Show the main evidence sources and note any assumption, inference, evidence gap, or confidence limit that materially affects the picture.
> Keep the report evidence-based, practical, and free of future-state design or implementation planning.

### 12.2. Section prompts

> Rewrite the current-state overview so it reflects the real operating situation today, including the roles, systems, and practical conditions that materially shape the work.

> Summarize the most important current-state facts that later definition should reference without converting them into future-state recommendations.

> Identify any sentence that sounds like a recommendation and rewrite it as an observed current-state fact or a clearly marked open question.

### 12.3. Validation prompts

> Check whether this Current State Analysis Report describes the actual current state clearly enough to support assessment and later handoff without drifting into solution design or roadmap content.

> Rewrite any section that treats assumptions as facts, hides workarounds or ownership gaps, obscures confidence limits, or starts describing the target state instead of the current state.
