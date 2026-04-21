# Completeness and Review Model

## 1. Purpose

This document defines how artifacts and gates are judged under the framework.

It covers:

1. artifact-level completeness
2. gate-level completeness
3. qualitative ratings
4. blocker and open-item handling
5. review, assurance, and audit rules
6. AI-agent sufficiency
7. anti-bureaucracy guardrails

## 2. Completeness Model Type

The framework uses a hybrid review model.

1. mandatory pass/fail criteria determine whether the artifact or gate passes
2. qualitative ratings describe the quality of the evidence after mandatory checks are applied

The standard ratings are:

1. `weak`
2. `adequate`
3. `strong`

If a mandatory criterion fails, the artifact or gate fails immediately. The rating does not override failure.

## 3. Shared Artifact-Level Core

Every required artifact must satisfy all of the following:

1. clarity
2. internal consistency
3. visibility of decisions, assumptions, unknowns, and open issues
4. actionability for the next consumer
5. AI sufficiency

Each artifact must also define:

1. purpose
2. required contents
3. artifact-specific completeness rules
4. common failure conditions

## 4. Shared Gate-Level Mandatory Checks

Every gate review must confirm that:

1. the documentation set is complete enough for the stage
2. required artifacts are cross-artifact consistent
3. unresolved blockers do not force downstream teams to invent business requirements
4. the named downstream consumer can proceed without redefining the problem
5. the documentation set satisfies the AI-agent sufficiency standard

## 5. Qualitative Rating Definitions

| Rating | Meaning |
| --- | --- |
| `weak` | The downstream team would need to guess or reopen fundamentals |
| `adequate` | The downstream team can proceed safely with limited clarification |
| `strong` | The downstream team can proceed efficiently without material clarification |

Gate thresholds are:

1. Gates 1-3 and 5-8 require at least `adequate`
2. Gate 4 requires `strong`

## 6. Blockers vs Controlled Open Items

The framework distinguishes between:

1. `blocker` entries, which force gate failure when they affect the current gate
2. controlled open items, which may remain open only when they are explicit, owned, actionable, dated where appropriate, and do not invalidate mandatory pass conditions

Any open `blocker` affecting the current gate forces gate failure.

If a non-blocker becomes gate-disqualifying, it must be reclassified or separately recorded as a `blocker` before the gate decision is finalized.

## 7. Open Items Register Rules

The `Open Items Register` is the canonical lifecycle register for:

1. blockers
2. risks
3. issues
4. assumptions
5. dependencies

It must exist for every initiative no later than Gate 2, even if nearly empty.

It must not be replaced by separate RAID logs, meeting notes, or artifact margin comments.

## 8. AI-Agent Sufficiency Standard

AI sufficiency is part of completeness, not a separate advisory check.

Every required artifact and gate must satisfy the baseline AI-sufficiency checklist, including:

1. explicit meaning
2. terminological stability
3. reference clarity
4. scope boundedness
5. decision visibility
6. traceability
7. structural parseability
8. cross-artifact consistency
9. actionability for the next consumer
10. target-state explicitness
11. controlled unknowns only
12. explicit actor/action/object language
13. external-reference discipline

Immediate AI-sufficiency fail patterns include:

1. uncontrolled placeholders such as `TBD`
2. contradictory statements across required artifacts
3. undefined material terms or acronyms
4. unreferenceable external context
5. vague acceptance or target-state language
6. missing identifiers or other material traceability structure

## 9. Acceptance Criteria Quality Rule

Acceptance criteria must be:

1. observable
2. quantifiable where feasible
3. testable with a defined validation method
4. supported by at least one holdout example per major criterion

The canonical format is hybrid Gherkin:

```text
Given [preconditions and context]
When [action or event occurs]
Then [observable outcome]
  - Metric: [quantified threshold]
  - Validation method: [test, query, inspection, or holdout pattern]
  - Holdout example: [concrete example]
```

## 10. Supportability and Maintainability Rule

Before Gate 7 can pass, the documentation set must make the following explicit:

1. support ownership
2. support model
3. observability expectations
4. maintainability commitments
5. transition checklist evidence

If these are absent or materially unclear, Transition Complete fails.

## 11. Review, Assurance, and Audit

The default review model is Delivery Owner-led review with PMO assurance oversight.

### 11.1 Delivery Owner

The Delivery Owner is responsible for:

1. preparing the evidence package
2. convening the review
3. ensuring required artifact owners are present

### 11.2 Gate Decision Owner

The Gate Decision Owner is accountable for the stop/proceed decision at the gate.

### 11.3 PMO

PMO is the framework assurance function. PMO responsibilities include:

1. maintaining the review standard
2. assigning the named Gate Decision Owner
3. checking evidence completeness
4. attending substantive gate reviews
5. auditing a sample of completed reviews
6. intervening on escalation, non-compliance, or dispute

## 12. Review Modes

The framework supports:

1. `quick-pass` review, which requires at minimum a `Decision Log` entry
2. `substantive` review, which requires a live gate review meeting and a written review record

If independent-review trigger conditions are present, PMO decides whether a normally quick-pass gate stays quick-pass with targeted review or becomes substantive.

## 13. Trigger-Based Independent Review

Independent review becomes mandatory when one or more of the following are true:

1. architecture impact
2. security or privacy impact
3. external delivery or vendor handoff
4. material business risk or regulatory exposure

When triggered, the required domain signoff must be present before the gate can pass.

## 14. Review Evidence Retention

For quick-pass gates:

1. a `Decision Log` entry is sufficient

For substantive gates:

1. a committee-action style review record is required
2. the record must include gate reviewed, date, attendees, decision, deficiencies or conditions, and action items

## 15. Anti-Bureaucracy Guardrails

The framework minimizes overhead by:

1. scaling evidence proportionately
2. triggering conditional artifacts only when needed
3. allowing omission only where the framework explicitly permits it

The following controls are non-waivable:

1. all formal gates
2. a named Gate Decision Owner for every gate
3. the required primary artifact
4. the `Decision Log`
5. the `Open Items Register`
6. any conditional artifact whose trigger condition is true

Every approved omission or waiver of a non-core item must be recorded in the `Decision Log`.

## 16. Critical Artifact Mapping Rule

Critical stage-defining artifacts are rule-based, not flat unconditional lists.

From Gate 2 onward, the persistent critical artifacts are:

1. `ARTIFACT-PROJECT-BRIEF`
2. `ARTIFACT-DECISION-LOG`
3. `ARTIFACT-OPEN-ITEMS-REGISTER`

Triggered conditional artifacts become gate-critical when their absence would invalidate the gate's mandatory pass conditions.

Use the YAML files in `machine_readable/` when exact gate-to-artifact mapping is needed.
