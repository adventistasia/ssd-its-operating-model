# Backup, Restore & Recovery Plan Specification

## 1. What This Artifact Is For

The Backup, Restore & Recovery Plan defines how the solution can be backed up, restored, recovered, or rolled back after failure, error, disruption, or failed change.

It exists to make recovery realistic, owned, and reviewable rather than assumed. A useful plan helps the organization restore service or data without relying on undocumented knowledge or untested assumptions.

The intended outcome is that backup, restore, recovery, and rollback can be performed in a controlled way that protects service continuity, data integrity, and operational accountability.

Intended readers include: IT Operations / Service Owner, DevOps teams, support and infrastructure teams, and security and audit reviewers.

## 2. When to Use It

This artifact is required for any initiative that introduces or changes data, services, integrations, or environments where loss, corruption, failed deployment, or outage would matter.

Use this artifact during solution design, before go-live, and as part of readiness and resilience review. It is most useful where recovery obligations, dependency risks, and service continuity expectations must be understood before the solution is accepted into operation.

It should align with NIST contingency-planning guidance, including planning for recovery roles, scenarios, and validation; with CIS Control 11 on data recovery; and with ITIL service continuity intent by making restore and rollback capability credible and governed.

## 3. Stage Fit and Handoffs

- Stage 4: define recovery scope, scenarios, and responsibilities as part of delivery-ready design.
- Stage 6: confirm recovery readiness for what is actually being deployed.
- Stage 7: provide recovery-readiness evidence to support operational acceptance and closure.

Upstream sources:

- [Technical Design Document Specification](technical_design_document_specification.md)
- [Data Asset Specification](../data_governance_and_records_deliverables/data_asset_specification.md)
- [DevOps Guide Specification](devops_guide_specification.md)

Downstream artifacts:

- [Operational Readiness Confirmation Record Specification](operational_readiness_confirmation_record_specification.md)
- [Acceptance Record Specification](../solution_deliverables/acceptance_record_specification.md)

This artifact should align with the Technical Design Document, Solution Module Definitions, DevOps Guide, Operations & Support Model, Data Asset Specification, and Operational Readiness Confirmation Record.

## 4. Before You Start

Confirm the following inputs are available before drafting:

- confirmed scope of systems, data, and services included in the initiative
- named Service Owner and recovery responsibility owners
- understanding of the backup platform, hosting environment, and data dependencies
- review of the Technical Design Document or equivalent for data flows, integration points, and deployment architecture
- clarity on recovery objectives or service continuity expectations (target recovery time or recovery point tolerances where applicable)

## 5. How to Draft It

1. **Define recovery scope** — identify systems, data, configurations, and services covered; note key exclusions and recovery-objective tolerances (see [6.1](#6.1.-recovery-scope)).
2. **Describe recovery scenarios and approaches** — document the backup and restore approach, rollback approach for failed changes, other recovery paths, and invocation triggers for each (see [6.2](#6.2.-recovery-scenarios-and-approaches)).
3. **Document roles, dependencies, and prerequisites** — list recovery responsibilities, required access or tools, critical dependencies, and operational constraints (see [6.3](#6.3.-roles,-dependencies,-and-prerequisites)).
4. **Define validation expectations** — state how the recovery path will be tested or demonstrated, what evidence is required, and when validation should be repeated (see [6.4](#6.4.-validation-expectations)).
5. **Populate the summary table** — complete the recommended recovery summary table using references to detailed procedures rather than embedding every step (see [6.5](#6.5.-template-guide)).

## 6. Minimum Structure

### 6.1. Recovery Scope

Must include:

- systems, data, configurations, or services covered
- key exclusions where relevant
- assumptions about what is backed up or otherwise recoverable
- recovery objectives or tolerances where relevant, such as target recovery time or point expectations

This section defines what the plan actually protects.

### 6.2. Recovery Scenarios and Approaches

Must include:

- backup and restore approach
- rollback approach for failed release or change where relevant
- other recovery paths used for major failure or disruption
- triggers or decision points for when each recovery path should be invoked

This section explains how recovery is expected to happen.

### 6.3. Roles, Dependencies, and Prerequisites

Must include:

- recovery responsibilities
- required access or tools
- critical dependencies and prerequisites
- operational constraints that affect restore or recovery

This section makes the recovery path executable in practice.

### 6.4. Validation Expectations

Must include:

- how the recovery path will be tested, demonstrated, or otherwise validated
- what evidence should exist to show the plan is credible
- when the validation should be repeated, refreshed, or revisited after change

This section prevents the plan from being purely theoretical.

### 6.5. Template Guide

Recommended summary table:

| Recovery area | Scenario | Recovery approach | Owner | Dependency | Validation evidence |
| --- | --- | --- | --- | --- | --- |

Use references for detailed procedures rather than embedding every step in this plan.

## 7. Writing Rules

Include enough detail to show backup scope, restore path, recovery responsibilities, dependencies, recovery constraints, and validation expectations. Do not turn it into a generic business continuity plan for the whole organization.

Keep the following out of this artifact:

- unrelated enterprise continuity planning
- full operating procedures already maintained elsewhere
- vague assurances such as "vendor handles backup" without clarifying scope and dependency

## 8. Traceability, Ownership, and Review

The Service Owner, infrastructure lead, or technical lead usually coordinates this artifact.

It should be reviewed by operations and any team responsible for backup platforms, data stewardship, or security oversight. For solutions with material recovery risk, that review should start during solution design.

Minimum traceability expectation:

- recovery scope references the actual live systems and data in scope
- recovery responsibilities and dependencies align with the operations model
- validation evidence links are visible for readiness and acceptance review

Minimum ownership expectation:

- Service Owner is accountable for recovery capability in live service.
- Support and infrastructure owners are accountable for recoverability execution.
- Delivery Owner ensures recovery obligations are not left unresolved at handover.

## 9. Maintenance Expectations

Update when data scope, hosting, recovery tools, dependencies, or recovery objectives change. Revisit after significant incidents or recovery tests.

## 10. Validation Guide

- Is it clear what can be restored and under what conditions?
- Are recovery roles, dependencies, and constraints explicit?
- Are recovery objectives, invocation triggers, and validation expectations clear enough to make the plan operationally credible?
- Is there a clear expectation that recovery is validated rather than only described?
- Does the artifact stay focused on the solution-level recovery plan rather than enterprise continuity in general?

If weak, define the recovery scope more clearly and make validation expectations explicit.

## 11. Done When

- Recovery scope is defined and exclusions are visible.
- Recovery scenarios, approaches, and invocation triggers are documented for each relevant failure or disruption type.
- Roles, access requirements, and dependencies are explicit and owned.
- Validation expectations are stated, with named owners and a schedule for testing or demonstration.
- The summary table is populated with references to detailed procedures or evidence.

## 12. What Comes Next

1. Review with the Service Owner and infrastructure team before go-live.
2. Reference this plan in the [Operational Readiness Confirmation Record](operational_readiness_confirmation_record_specification.md).
3. Confirm alignment with the [DevOps Guide](devops_guide_specification.md) and [Operations & Support Model](operations_and_support_model_specification.md).
4. Schedule validation and update after recovery tests or significant system changes.

## 13. Prompt Guide

**Starter prompt:**

```
Draft a Backup, Restore & Recovery Plan for this solution.
Explain what is covered, what recovery scenarios are supported, who is responsible, what dependencies or constraints matter, and how the recovery path is validated.
Keep it solution-focused and operationally credible.
```

**Validation prompt:**

```
Review this Backup, Restore & Recovery Plan against the following questions:
- Is it clear what can be restored and under what conditions?
- Are recovery roles, dependencies, and constraints explicit?
- Are recovery objectives, invocation triggers, and validation expectations operationally credible?
- Is there a clear expectation that recovery is validated rather than only described?
- Does the artifact stay focused on solution-level recovery rather than enterprise continuity in general?
Flag any section that is missing, vague, or relies on untested assumptions.
```


