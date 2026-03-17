# Work Delivery Framework

## 1. Purpose

This framework is the main staged operating path for planned ITS work from intake to closure.

It governs planned work delivery initiatives, including projects, significant enhancements, and smaller governed initiatives.

It puts the Define-Decide-Deliver (DDD) Work Management Model into practice by defining the minimum decisions, documents, ownership, and controls needed to deliver work clearly, accountably, and sustainably.

## Related Documents

- [Repository Start Here](../README.md)
- [ITS Operating Model](../its_operating_model.md)
- [ITS Work Management Model](../its_work_management_model.md)
- [Work Assessment Process](work_assessment/work_assessment_process.md)
- [Work Brief Specification](work_brief/work_brief_specification.md)
- [Standard Deliverables Guide](standard_deliverables_guide.md)
- [Deliverable Specifications Index](deliverable_specifications_index.md)
- [Solution Design Process](solution_design_process.md)

### 1.1. How This Framework Fits with the Other Core Documents

Use the core repository documents in this order:

- The [ITS Operating Model](../its_operating_model.md) explains the control intent and why ITS work must be visible, owned, traceable, and supportable.
- The [ITS Work Management Model](../its_work_management_model.md) states the governing control logic in simple terms: define the work, decide whether to commit to it, then deliver and close it properly.
- This Work Delivery Framework turns that control logic into the practical seven-stage operating path for planned work.
- The [Standard Deliverables Guide](standard_deliverables_guide.md) helps teams decide which deliverables are needed.
- The [Deliverable Specifications Index](deliverable_specifications_index.md) points to the detailed drafting specifications for those deliverables.

If a reader only needs one document to understand how planned ITS work should move from intake to closure in practice, this is the anchor document.

## 2. Intended Outcome

When applied consistently:

- work does not start informally
- scope and outcomes are clear before authorization
- ownership and decision rights are explicit
- delivery progress is visible through accepted outputs, not activity alone
- changes are traceable and controlled
- operational support is prepared before handover
- acceptance and closure are formal, attributable, and evidence-based

## 3. Applicability and Scaling

This framework applies to:

- projects
- significant enhancements
- smaller planned initiatives that still require governance, coordination, and formal acceptance

To keep the framework practical:

- use the minimum viable level of detail needed for the work's size, risk, and impact
- one document may satisfy multiple outputs if the required information is explicit and traceable
- smaller initiatives may use concise versions of artifacts, but they must not skip decision points, ownership, or acceptance controls
- small governed work items may use a Work Brief as the scaled definition and control artifact where a full Initiative Definition Document would be too heavy

The framework is intentionally control-light for low-complexity work and should scale up only where risk, cost, impact, or cross-team coordination require it.

## 4. Operating Principles

1. Define before authorizing.
2. Authorize before delivering.
3. Elaborate without expanding authorized scope.
4. Measure progress by accepted deliverables and evidence.
5. Transition to operations with named ownership.
6. Keep artifacts practical, readable, and usable by both humans and AI.

### 4.1. Relationship to the Define-Decide-Deliver Model

The Define-Decide-Deliver model is the control logic underneath this framework.

- **Define** happens across Stage 1 Work Assessment, Stage 2 Work Definition, and Stage 4 Work Definition Details.
- **Decide** happens at the formal decision points, especially Stage 3 Work Authorization, major change decisions during delivery, and Stage 7 acceptance and closure decisions.
- **Deliver** happens across Stage 5 Delivery Mobilization, Stage 6 Work Delivery, and Stage 7 Acceptance, Transition & Closure.

This means the repository is not describing two competing models. The DDD model is the simple control rule. The Work Delivery Framework is the practical staged operating path that puts that rule into day-to-day use.

## 5. Core Roles

| Role                              | Accountable for                                                      | Practical working expectation                                                                       |
| --------------------------------- | -------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| Sponsor                           | Sponsorship, priority, funding support, risk sponsorship             | Confirms why the work matters and keeps it supported                                                |
| Decision Authority                | Formal go / no-go and major governance decisions                     | May be the committee itself or a formally delegated person acting within recorded delegation limits |
| Outcome Owner                     | Intended business outcome and success measures                       | Confirms the work is solving the right problem                                                      |
| Delivery Owner                    | Stage discipline, coordination, delivery control, evidence readiness | Usually leads the operating rhythm of the work                                                      |
| Project Manager (if assigned)     | Delivery coordination on behalf of the Delivery Owner                | Maintains plans, status, risks, decisions, dependencies, and follow-up actions                      |
| Acceptance Authority              | Formal sign-off for a deliverable domain or deliverable              | Accepts based on defined acceptance focus and evidence                                              |
| Support Owner / Operational Owner | Ongoing operational support and service continuity                   | Confirms readiness to run and support the solution                                                  |
| Subject Matter Leads              | Domain-specific content quality                                      | Draft or review specialist inputs as required                                                       |

### 5.1. Delegated Decision Authority

For organizational initiatives, a committee may be the ultimate approving body.

It is not necessary for the committee to make every decision directly. A named person may act as the Decision Authority on behalf of the committee when delegation is explicit and recorded.

Where decision authority is delegated, the record should make visible:

- the committee or authority delegating the decision right
- the named delegated person
- the kinds of decisions covered by the delegation
- any limits on scope, cost, risk, policy, or acceptance authority
- when the matter must return to the committee or higher authority

Delegated authority must not be assumed or inferred. If delegation is not explicit, the decision should be treated as reserved to the committee or other formal approving authority.

## 6. Decision Record Minimum

The minimum standard for a decision record in Stages 1, 2, 3, and 7 is:

- decision taken
- date
- decision authority
- artifact or evidence used
- conditions or follow-up actions
- owner for each follow-up action

The decision record may be a standalone artifact or a clearly identified section in another approved record.

## 7. AI-Assisted Delivery Rules

AI may be used to speed up drafting, summarization, traceability checks, review preparation, and revision cycles.

AI must not:

- authorize work
- approve scope changes
- assign or change accountable owners without instruction
- mark deliverables accepted
- invent evidence that does not exist

AI-generated outputs should include clear source context, stable IDs where used, and a concise change summary when materially revised.

Use the [AI-Assisted Authoring Standard](ai_assisted_authoring_standard.md) for the default prompt order, review loop, and guardrails across governed artifact drafting.

If an AI agent is asked to draft or revise a governed artifact and any of the following are missing, unclear, or contradictory:

- approved scope boundary
- required deliverable identity
- named owner or Acceptance Authority
- decision basis
- evidence basis
- status of authorization

the AI should:

- label the output as a working draft
- state the missing control inputs explicitly
- avoid presenting assumptions as approved facts
- avoid marking status as authorized, accepted, or complete
- route the matter back to the Delivery Owner or named human owner for resolution

Where AI or humans draft governed artifacts with multiple sections or sub-sections, visible section numbering is recommended so content can be referenced unambiguously during review, decision-making, acceptance, and change control.

Use numbering consistently in headings where practical, for example:

- `## 1. Purpose`
- `## 7. Required Content or Minimum Structure`
- `### 7.1. Baseline context`
- `### 12.2. Section prompts`

## 8. Practical TL;DR - How This Framework Works in Practice

If you only read one section, read this one.

This framework is meant to answer five practical questions before work becomes difficult to control:

- should this work proceed at all
- what exactly is being approved
- who is allowed to approve it
- how will progress and changes be controlled
- what proves the work is complete and supportable

In practice, the framework works like this:

- Stage 1 Work Assessment - screens the work through three increasingly rigorous assessment steps before definition begins
- Stage 2 Work Definition - defines what is being asked for approval, including required deliverables and owners
- Stage 3 Work Authorization - gives formal authority to proceed
- Stage 4 Work Definition Details - turns the approved intent into delivery-ready detail without quietly expanding scope
- Stage 5 Delivery Mobilization - sets up the team rhythm, controls, and trackers needed to execute visibly
- Stage 6 Work Delivery - delivers the approved outputs and gathers evidence as the work progresses
- Stage 7 Acceptance, Transition & Closure - formally accepts the result, transfers operational responsibility, and closes the work

For small governed work, the Work Brief may be used as the scaled artifact across Stages 2 and 3 and may continue as the live control record through delivery and closure.

Within a larger initiative, multiple Work Briefs may be used as child work orders under the approved initiative baseline.

The practical reading path across the repository is:

`README -> ITS Operating Model -> ITS Work Management Model -> Work Delivery Framework -> Work Assessment or Work Brief -> Initiative Definition and deliverable specifications -> Delivery evidence -> Acceptance and closure records`

Accountable means accountable for moving the stage forward.

| Stage                               | What it means in practice                                                          | Primary Decision                                      | Accountable                                      | Core artifacts                                                                                                      | Minimum outcome                                                                                                     |
| ----------------------------------- | ---------------------------------------------------------------------------------- | ----------------------------------------------------- | ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| 1. Work Assessment                  | Screen the request through initial triage, validation, and final assessment before Work Definition | Proceed / Defer / Reject                              | ITS with Assessment Owner and sponsor candidate | Initial Review, Validation Assessment, Work Assessment Report, decision record                                      | Clear recommendation on whether the work should enter Work Definition, with Stage 2 handoff basis if proceeding    |
| 2. Work Definition                  | Define the initiative clearly enough for an authorization decision                 | Ready / Not ready for authorization                   | Delivery Owner with Outcome Owner                | Initiative Definition Document, or Work Brief for small governed work, required deliverables and Acceptance Authority map, supporting authorization artifacts as needed, Functional Capabilities (if applicable), draft Project Charter, Stage 2 readiness decision record | Decision-ready definition baseline with required deliverables and supporting detail appropriate to the work size    |
| 3. Work Authorization               | Formally approve the work, funding, and accountability before delivery starts      | Approve / Defer / Reject / Approve with conditions    | Sponsor with Decision Authority                  | Decision record or decision log, approved Project Charter where applicable, funding confirmation, Work Brief where used for small governed work | Work formally authorized with funding and accountability.<br><br>Appropriate committee approval may be necessary  |
| 4. Work Definition Details          | Elaborate the approved work into the detail needed to build, test, and transition  | Ready to mobilize / Rework / Return to Stage 2        | Delivery Owner with design leads                 | Delivery-ready elaboration set, additional definition deliverables as needed, detailed domain artifacts, acceptance test approach | Detailed design, elaborated roadmap, and delivery-ready artifact set                                               |
| 5. Delivery Mobilization            | Put delivery controls, roles, cadence, roadmap, and trackers in place              | Ready to execute                                      | Delivery Owner                                   | Delivery Charter, team-confirmed Delivery Roadmap, communication plan, change and escalation rules, delivery plan, trackers | Delivery rhythm, controls, and team-aligned roadmap and setup in place                                             |
| 6. Work Delivery                    | Produce the approved deliverables, manage change visibly, and collect evidence     | Continue / Escalate / Change / Prepare for acceptance | Delivery Owner                                   | Deliverables, evidence, status reports, decision and change records                                                 | Authorized deliverables produced with evidence                                                                      |
| 7. Acceptance, Transition & Closure | Formally accept the work, confirm handover, and close with ownership still visible | Accept / Conditionally accept / Reject / Close        | Acceptance Authorities and Sponsor as applicable | Acceptance records, handover confirmation, closure record                                                           | Formal acceptance, handover, and closure                                                                            |

The practical implication is simple: work should not move forward because people are busy or because effort has already started. It should move forward because the previous stage produced a clear decision, named ownership, and usable artifacts that make the next stage governable.

## 9. Stage 1 - Work Assessment

**Purpose:** Determine whether the request is worth entering Work Definition by screening it through three increasingly rigorous assessment steps.

**Primary Decision:** Proceed, Defer, or Reject.

**Primary Owner:** ITS, supported by intake / portfolio governance and the named Assessment Owner.

### 9.1. Operating Intent

Stage 1 is not one large assessment done at the same depth for every request.

Its purpose is to screen work practically:

- start with the lightest viable triage
- deepen scrutiny only when the previous step justifies it
- stop weak, unsupported, misaligned, or low-value work early
- hand forward only work that is worth defining

The normal three-step sequence is:

1. Initial Review
2. Validation Assessment
3. Work Assessment Report

The normal progression from Stage 1 into Stage 2 is:

`Work Assessment Report -> Initiative Definition Document`

For smaller governed work, the Stage 1 handoff may instead move into a [Work Brief](work_brief/work_brief_specification.md) when that gives enough definition, ownership, and control for the size and risk of the work.

### 9.2. Minimum Outputs

- Initial Review
- Validation Assessment
- Work Assessment Report
- decision record
- named sponsor or sponsor candidate by the end of Stage 1 if proceeding

### 9.3. Stage Output Checklist

| Output                  | Required  | Accountable              | Practical note                                                              |
| ----------------------- | --------- | ------------------------ | --------------------------------------------------------------------------- |
| Initial Review          | Yes       | Assessment Owner         | Fast front-door triage; stop or defer quickly where value, fit, or sponsorship is weak |
| Validation Assessment   | Yes       | Assessment Owner         | Add higher-confidence validation with requester SMEs and immediate team; decide whether full business analysis is justified |
| Work Assessment Report  | Yes       | Assessment Owner with ITS leadership | Final Stage 1 recommendation based on completed business analysis and handoff basis for Work Definition |
| Early stakeholder input | As needed | Assessment Owner         | Keep notes inside the assessment artifacts unless separate notes are necessary |
| Decision record         | Yes       | ITS / Decision Authority | Record proceed / defer / reject and any conditions                          |

### 9.4. Three-Step Practical Flow

#### 9.4.1. Initial Review

Use this step to decide whether the request is worth any further assessment effort at all.

This step should:

- capture the need and desired outcome in plain language
- identify who is affected and why it matters
- check obvious dealbreakers
- result in stop, defer, or proceed to Validation Assessment

#### 9.4.2. Validation Assessment

Use this step only for requests that survive Initial Review.

This step should:

- validate the need with limited evidence
- confirm business alignment, sponsorship, outcomes, success measures, scope boundaries, and high-level capabilities without design detail
- compare broad options, including doing nothing
- surface obvious risk and feasibility concerns
- result in stop, defer, or proceed to full business analysis

#### 9.4.3. Work Assessment Report

Use this step only for work that survives Validation Assessment.

This step should:

- synthesize the business analysis findings, validated need, options, risks, constraints, and timing
- recommend whether the work should enter Work Definition
- identify what Stage 2 must define or resolve next
- provide the final Stage 1 handoff basis if the work proceeds

### 9.5. AI Use in This Stage

AI can:

- summarize intake material
- help structure the problem statement, options, and recommendations
- draft any of the three Stage 1 assessment artifacts from supplied inputs

Humans must:

- confirm sponsorship and ownership signals
- decide whether the work should proceed
- confirm the recorded decision and any conditions

AI must not:

- treat a recommendation to proceed as authorization to deliver
- claim funding, sponsorship, or authority that has not been confirmed
- invent evidence or stakeholder support

### 9.6. Exit Criteria

- the need and desired outcome are clear enough to explain why the work matters
- sponsorship is confirmed or explicitly unresolved and treated accordingly
- high-level options, risks, and feasibility concerns are visible enough for Stage 1 decision-making
- the final Stage 1 recommendation is explicit and attributable
- if proceeding, the Work Assessment Report gives Stage 2 a practical handoff basis

## 10. Stage 2 - Work Definition

**Purpose:** Define the initiative enough to support a sound Work Authorization decision - no more, no less.

**Primary Decision:** Ready or not ready for Work Authorization.

**Primary Owner:** Delivery Owner, with Outcome Owner accountability for business intent.

### 10.1. What Stage 2 Must Produce

Stage 2 stays at authorization-level detail. It defines what the initiative is expected to deliver, why it matters, who owns it, what acceptance will focus on, and what level of cost and risk the organization is being asked to approve.

Stage 2 should normally begin from the completed Work Assessment Report, not from raw intake notes or an unstructured rediscovery exercise.

For small governed work using a Work Brief, the same rule still applies: the brief should be based on the completed Stage 1 assessment and should not restart definition from scratch.

Deliverable domains may be used to organize the delivery view, but they do not replace visibility of the actual deliverables expected from the initiative.

The **Initiative Definition Document** is the primary artifact for Stage 2. Supporting artifacts may be attached or referenced only when they are needed to hold additional detail that enables a sound Work Authorization decision.

As much as possible, the Initiative Definition Document should contain enough information to support authorization without forcing readers to assemble the decision case from many separate documents.

Deliverables not needed for authorization may still be listed in Stage 2 at summary level so the likely delivery footprint and effort remain visible, but they should be elaborated only in Stage 4. A high-level Delivery Roadmap should be drafted in Stage 2 to support authorization discussions and planning visibility.

### 10.2. Initiative Definition Document Minimum Content

- problem and current-state summary
- future-state intent and expected value
- outcome statement and measurable success criteria
- in-scope and out-of-scope boundaries
- required deliverables for the initiative, grouped by deliverable domain where useful
- named Acceptance Authority for every required deliverable or clearly defined deliverable grouping
- delivery owner, outcome owner, sponsor, and key stakeholders
- approval-level cost, financial impact, and major risk summary
- support and operational ownership expectations
- approval-level functional scope where solution behavior is in scope

Additional expected deliverables not needed for authorization may be listed at summary level so likely effort is visible without forcing premature elaboration.

### 10.3. Stage Output Checklist

| Output                                          | Required                                                                           | Accountable                                   | Practical note                                                                                       |
| ----------------------------------------------- | ---------------------------------------------------------------------------------- | --------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| Initiative Definition Document                  | Yes                                                                                | Delivery Owner                                | Primary authorization artifact; keep it decision-ready, not design-heavy                             |
| Functional Capabilities                         | When solution behavior is in scope and the ID cannot hold enough clarity concisely | Delivery Owner with business / solution leads | Approval-level only; do not turn Stage 2 into detailed design                                        |
| Required deliverables and Acceptance Authority map | Yes                                                                              | Delivery Owner                                | Prefer to keep this inside the Initiative Definition Document; domains may be used only as organizing structure |
| Cost, funding, and risk summary                 | Yes                                                                                | Sponsor with Delivery Owner                   | Prefer to keep this inside the Initiative Definition Document unless detail must sit separately      |
| Support / operational impact summary            | When service or system impact exists                                               | Delivery Owner with operations                | May be summarized in the Initiative Definition Document with supporting detail referenced separately |
| Supporting authorization artifacts              | As needed                                                                          | Relevant owner                                | Use only where additional detail is necessary for a sound authorization decision                     |
| Draft Project Charter                           | Yes                                                                                | Delivery Owner                                | Prepare the decision-ready charter for Stage 3                                                       |
| Initial Delivery Roadmap (high level)           | Yes                                                                                | Delivery Owner with Project Manager support   | Draft high-level phases, milestones, dependencies, and risks to support authorization-level planning visibility |
| Stage 2 readiness decision record               | Yes                                                                                | Delivery Owner with Outcome Owner             | Record whether the package is ready or not ready for Work Authorization, with basis and follow-up    |

### 10.4. AI Use in This Stage

AI can:

- draft the Initiative Definition Document from structured inputs
- suggest scope wording, outcome statements, and artifact structure
- help identify candidate deliverables from the [Standard Deliverables Guide](standard_deliverables_guide.md)
- help list additional expected deliverables that may need elaboration after authorization

AI must not:

- decide what is in or out of scope
- decide which deliverables are required without instruction
- assign Acceptance Authorities without instruction
- approve the authorization package

### 10.5. Exit Criteria

- the initiative is defined clearly enough for a go / no-go decision
- required deliverables are explicitly identified at authorization level
- Acceptance Authorities are named for each required deliverable or deliverable grouping
- additional expected deliverables not needed for authorization may be listed at summary level so likely effort remains visible
- owners, cost, risks, and support implications are visible
- the readiness decision is recorded
- the package is ready for Work Authorization

## 11. Stage 3 - Work Authorization

**Purpose:** Formally authorize delivery by committing people, time, funding, and risk to the defined work.

**Primary Decision:** Approve, Defer, Reject, or Approve with conditions.

**Primary Owner:** Decision Authority.

### 11.1. Minimum Outputs

- approved or rejected Project Charter
- decision record
- funding confirmation or explicit funding condition
- any conditions, limits, or phased authorization notes

### 11.2. Stage Output Checklist

| Output | Required | Accountable | Practical note |
| --- | --- | --- | --- |
| Decision record | Yes | Decision Authority | Record the actual decision and any conditions |
| Approved Project Charter | Yes for approved work | Decision Authority with Delivery Owner support | Confirms the formal commitment to proceed |
| Funding confirmation | Yes for approved work | Sponsor / Finance / Decision Authority | Must identify the source or condition of funding |
| Authorization conditions log | When applicable | Delivery Owner | Track what must be satisfied after authorization |

### 11.3. AI Use in This Stage

AI can:

- prepare concise approval briefs
- summarize risks, decisions needed, and open conditions
- draft the decision record after the meeting

AI must not:

- make the authorization decision
- claim funding is approved when it is not

### 11.4. Exit Criteria

- delivery is explicitly approved, deferred, or rejected
- the Project Charter status is clear
- funding and accountability are clear enough to proceed
- any conditions are recorded with owners

### 11.5. Hard Rule

No delivery work may start without explicit Work Authorization.

## 12. Stage 4 - Work Definition Details

**Purpose:** Elaborate the authorized initiative into the delivery-ready detail needed to build, test, transition, and accept what was authorized, without changing approved scope, outcomes, capabilities, or acceptance structure.

**Primary Decision:** Ready to mobilize, rework, or return to Stage 2.

**Primary Owner:** Delivery Owner, working with solution and domain leads.

### 12.1. Minimum Outputs

- elaborated versions of required Stage 2 deliverables where further detail is needed
- elaborated Delivery Roadmap aligned to authorized scope, milestones, and dependencies
- additional definition deliverables needed for controlled delivery
- detailed solution and domain-specific design or elaboration artifacts for in-scope work
- acceptance test approach aligned to Stage 2 acceptance focus
- rollout, migration, and recovery approach as applicable

### 12.2. Stage Output Checklist

| Output                                    | Required                               | Accountable                                 | Practical note                                                                                    |
| ----------------------------------------- | -------------------------------------- | ------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| Delivery-ready elaboration set            | Yes                                    | Delivery Owner with design leads            | Elaborate the authorized initiative into the detailed artifact set needed for controlled delivery |
| Additional definition deliverables        | When needed for controlled delivery    | Delivery Owner with domain leads            | May be identified in Stage 2 at summary level, but elaborated here only when needed               |
| Solution Modules and Use Case Narratives  | When solution behavior is in scope     | Solution lead                               | Must remain traceable to approved Functional Capabilities                                         |
| Acceptance test approach                  | Yes for deliverables requiring testing | Delivery Owner with testers / reviewers     | Show how acceptance will be evidenced                                                             |
| Data move, rollout, and recovery approach | When applicable                        | Delivery Owner with operations / data leads | Make transition and recovery practical                                                            |
| Detailed operational design summary       | When system impact exists              | Operations / support lead                   | Confirm how the solution will be run and supported                                                |
| Delivery Roadmap (elaborated baseline)    | Yes                                    | Delivery Owner with Project Manager support  | Expand Stage 2 roadmap with release sequence, dependencies, and control checkpoints               |

### 12.3. AI Use in This Stage

AI can:

- draft detailed design sections from approved scope
- help structure modules, use cases, test outlines, and traceability tables
- identify obvious mismatches between Stage 2 scope and Stage 4 detail
- help elaborate Stage 2 deliverables into delivery-ready detail

AI must not:

- introduce new capabilities
- silently expand scope through design detail

### 12.4. Exit Criteria

- design and deliverable detail are complete enough to execute
- traceability to authorized scope is clear
- acceptance approach is defined
- no material scope expansion has been introduced
- the work is ready for Delivery Mobilization

## 13. Stage 5 - Delivery Mobilization

**Purpose:** Prepare the team and governance rhythm to execute in a controlled, visible, and sustainable way.

**Primary Decision:** Ready to execute.

**Primary Owner:** Delivery Owner.

### 13.1. Minimum Outputs

- Delivery Charter
- Delivery Roadmap confirmed with the delivery team
- delivery plan or initial task breakdown
- communication plan
- change and escalation rules
- working cadence for status, risks, decisions, and acceptance readiness

### 13.2. Stage Output Checklist

| Output | Required | Accountable | Practical note |
| --- | --- | --- | --- |
| Delivery Charter | Yes | Delivery Owner | Charter and mobilize the team with clear operating expectations, communication methods, and governance controls |
| Delivery Roadmap (team-confirmed) | Yes | Delivery Owner with delivery team leads | Confirm scope-aligned sequencing, milestones, dependencies, and ownership with the mobilized team |
| Initial delivery plan / task breakdown | Yes | Project Manager or Delivery Owner | Enough to start controlled execution |
| Communication plan | Yes | Delivery Owner | Keep key audiences informed at the right level |
| Change and escalation rules | Yes | Delivery Owner | Clarify who decides what and how issues are escalated |
| RAID / dependency log setup | Yes | Project Manager or Delivery Owner | Risks, assumptions, issues, dependencies in one maintained place |
| Acceptance tracker setup | Yes | Delivery Owner | Track domain-level readiness, evidence, and sign-off status |

### 13.3. Minimum Operating Rhythm

At minimum, the delivery team should establish:

- a regular status review
- a maintained risk / issue / dependency view
- a change review path
- a decision log
- a clear path for preparing acceptance evidence

### 13.4. AI Use in This Stage

AI can:

- draft plans, meeting agendas, working agreements, and status templates
- summarize open risks and dependencies from notes
- help maintain structured trackers from confirmed inputs

AI must not:

- close risks, approve changes, or assign decisions without human confirmation

### 13.5. Exit Criteria

- the team knows how work will be executed and governed
- the roadmap is confirmed with the delivery team and understood by key stakeholders
- plans and trackers exist and are usable
- status, escalation, and acceptance preparation rhythms are in place
- the work is ready to begin controlled execution

## 14. Stage 6 - Work Delivery

**Purpose:** Produce the authorized deliverables, collect evidence, manage changes visibly, and progress work toward acceptance.

**Primary Decision:** Continue as planned, escalate, change, or prepare for Stage 7 acceptance.

**Primary Owner:** Delivery Owner.

### 14.1. Minimum Outputs

- in-scope deliverables
- acceptance evidence
- decision and change records
- current status, risk, and dependency reporting
- updated acceptance tracker

### 14.2. Stage Output Checklist

| Output                                            | Required           | Accountable                       | Practical note                                                  |
| ------------------------------------------------- | ------------------ | --------------------------------- | --------------------------------------------------------------- |
| Deliverables as approved in Initiative Definition | Yes                | Assigned Delivery Owners          | Build and validate only what was authorized or formally changed |
| Evidence linked to deliverables                   | Yes                | Delivery Owner with domain leads  | Evidence must be attributable and reviewable                    |
| Status reporting                                  | Yes                | Project Manager or Delivery Owner | Report progress by deliverable status and major outcomes        |
| RAID / dependency log updates                     | Yes                | Project Manager or Delivery Owner | Keep risks, issues, and dependencies current                    |
| Change records                                    | When change occurs | Delivery Owner                    | Record scope, decision, and impact of changes                   |
| Acceptance tracker updates                        | Yes                | Delivery Owner                    | Show what is ready, blocked, or pending sign-off                |

### 14.3. Minimum Control Expectations

During execution:

- progress should be reported by deliverable status, evidence status, and decision needs
- unapproved scope expansion should be treated as a governance issue
- material changes should be routed through the agreed change path
- evidence should be collected as work is completed, not reconstructed at the end
- the Delivery Owner or project manager should keep the operating picture current

### 14.4. AI Use in This Stage

AI can:

- draft status reports, evidence summaries, and change summaries
- check traceability and flag missing links
- help convert meeting notes into action lists and risk summaries

AI must not:

- declare deliverables accepted
- hide unresolved risks or gaps
- substitute generated text for real evidence

### 14.5. Exit Criteria

- all in-scope deliverables are produced and validated against defined acceptance focus
- evidence is complete and linked
- unresolved sign-off blockers are visible and addressed
- the work is ready for formal acceptance, transition, and closure

## 15. Stage 7 - Acceptance, Transition & Closure

**Purpose:** Formally accept the delivered outcomes, transition responsibility, and close the work.

**Primary Decision:** Accept, conditionally accept, reject, or close.

**Primary Owner:** Acceptance Authorities for their domains, coordinated by the Delivery Owner.

### 15.1. Minimum Outputs

- acceptance records for in-scope deliverables or domains
- operational handover confirmation where applicable
- closure record
- final unresolved actions list if any conditions remain
- final financial and delivery summary

### 15.2. Stage Output Checklist

| Output | Required | Accountable | Practical note |
| --- | --- | --- | --- |
| Acceptance records | Yes | Acceptance Authorities | Acceptance must be explicit and attributable |
| Operational handover confirmation | When operational ownership is impacted | Support / Operational Owner | Confirm the work is supportable beyond the delivery team |
| Closure record | Yes | Delivery Owner with Sponsor / Decision Authority as applicable | Record final status, closure basis, and any follow-up obligations |
| Outstanding conditions list | When applicable | Delivery Owner | Make remaining actions visible and owned |
| Final financial / delivery summary | Yes | Delivery Owner with Sponsor | Record actual vs approved at an appropriate level |

### 15.3. AI Use in This Stage

AI can:

- assemble closure packs from confirmed records
- summarize acceptance evidence and outstanding conditions
- draft closure summaries and handover notes

AI must not:

- approve acceptance
- claim transition is complete without confirmation from the receiving owner

### 15.4. Exit Criteria

- all required deliverables are accepted or explicitly conditionally accepted
- operational ownership is confirmed where needed
- closure is recorded
- any remaining follow-up actions are assigned and visible

### 15.5. Hard Rule

Delivered without acceptance is not complete.
