# Decision Record Log Specification

## 1. Purpose and Intended Outcome

The Decision Record Log maintains an attributable history of material decisions affecting scope, funding, sequencing, risk treatment, architecture direction, compliance position, or acceptance.

It exists to make important decisions visible after the meeting or conversation where they were made. A useful Decision Record Log helps delivery teams, reviewers, and future maintainers understand what was decided, why, by whom, and what changed as a result.

The intended outcome is that material decisions remain traceable, do not need to be rediscovered or re-litigated, and can be followed through into delivery, governance, and acceptance actions.

## 2. When It Is Required

This artifact is required when the initiative involves material governance, scope, risk, acceptance, or design decisions that should remain reviewable over time.

It is strongly recommended for initiatives with multiple authorities, material risk, or likely audit needs.

## 3. Intended Readers and Users

- Sponsor and Decision Authorities
- Delivery Owner
- governance and audit reviewers
- future maintainers
- leads affected by recorded decisions

## 4. Intended Project Context

Use this artifact from definition through closure. It is most useful where decisions need to remain traceable across changing teams, phases, and artifacts.

It should align with PMI governance and integrated change-control discipline by making material decisions attributable and easy to review without searching across email, meeting notes, or chat history.

## 5. How Much Detail to Include

Keep each entry short but decision-useful. Include enough context that another reader can understand the decision, the rationale, the decision-maker, and the impact on delivery or governance.

## 6. Required Content or Minimum Structure

This artifact should be table-driven.

### 6.1. Log context

Must include:

- initiative or solution name
- log owner
- current version or last updated date

This section identifies the log and who maintains it.

### 6.2. Required content for each decision row

Each decision row must include:

- Decision ID
- decision date
- decision title
- decision category
- decision summary
- decision maker or approving authority
- rationale or basis
- impacted artifacts or deliverables
- baseline impact or change implication where the decision alters approved scope, cost, authority, risk position, or acceptance approach
- follow-up owner where action is required
- current status

Recommended columns:

| Decision ID | Date | Title | Category | Decision | Authority | Rationale | Impacted artifacts | Baseline impact | Follow-up owner | Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Use controlled status values such as:

- `proposed`
- `approved`
- `superseded`
- `withdrawn`

This row structure is the main information model of the log.

### 6.3. Decision logging rules

Must include:

- what kinds of decisions belong in the log
- rule that superseded decisions remain visible rather than deleted
- rule that routine low-impact operational choices should not overload the log
- rule that decisions requiring artifact updates, re-approval, or new acceptance conditions must identify the affected baseline or record explicitly

This section keeps the log useful and governable.

### 6.4. Template guide

Use short entries:

- `Category`: scope, funding, risk, architecture, privacy, acceptance, or other defined category
- `Decision`: the conclusion, not the meeting discussion
- `Rationale`: a short reason, not full minutes
- `Impacted artifacts`: name the records or specifications that must align to the decision
- `Baseline impact`: state whether the decision confirms the current baseline, changes it, or creates a follow-up action to revise it

## 7. What to Keep Out

Keep the following out of this artifact:

- full meeting minutes
- raw discussion history
- large attachments copied into the log
- routine operational choices that do not affect governance or delivery direction

## 8. Relationships to Other Artifacts

The log should reference the Initiative Definition Document, Project Charter, major scope baselines, risk acceptance records, and closure records where applicable.

## 9. Ownership, Review, and Acceptance Expectations

The Delivery Owner or governance coordinator usually maintains the log. Decision makers remain accountable for the recorded decision itself.

## 10. Maintenance Expectations

Update the log as decisions occur. If a decision changes, mark the original entry as superseded and add the new one rather than overwriting history.

## 11. Validation Guide

- Does each entry identify the decision, authority, rationale, and impacted artifacts clearly?
- Can a reader tell whether the decision changed an approved baseline or only clarified it?
- Can a reader tell which decisions are still current?
- Is the log short enough to scan and strong enough to support audit or future change review?
- Does the log avoid becoming a copy of meeting minutes?

If weak, shorten entries, improve status handling, and make impacts on artifacts more explicit.

## 12. Prompt Guide for Drafting the Artifact

### 12.1. Starter prompt

> Create or update a Decision Record Log for this initiative.
> Capture only material decisions, with clear decision IDs, authority, rationale, impacted artifacts, follow-up ownership, and current status.
> Keep each entry short enough to scan quickly.

### 12.2. Section prompts

> Convert these meeting outcomes into Decision Record Log entries using the required row fields in this specification.

> Review the log and mark any entries that should be superseded, withdrawn, or removed because they are not material enough for this artifact.

### 12.3. Validation prompts

> Check whether this log distinguishes clearly between decisions, rationale, and follow-up actions.

> Check whether any current decision affecting scope, funding, or acceptance is missing from the log.
