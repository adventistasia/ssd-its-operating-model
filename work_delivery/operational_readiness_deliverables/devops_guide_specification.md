# DevOps Guide Specification

## 1. What This Artifact Is For

The DevOps Guide defines how the solution is deployed, configured, operated, monitored, supported, and recovered in day-to-day live service.

It exists to convert delivery and implementation knowledge into repeatable operational guidance that a DevOps team can use without relying on the original implementer. A useful guide supports handover, continuity, supportability, controlled operational change, safe release activity, and sustainable live-service ownership.

The intended outcome is that a competent DevOps team can run, support, maintain, and recover the deployed system or application consistently, safely, and independently after handover.

Intended readers include: DevOps teams, platform or site reliability teams, support teams, and Service Owner and Support Owner.

## 2. When to Use It

This artifact is required when a solution will be handed to a DevOps, platform, operations, or support team and has repeatable deployment, configuration, maintenance, troubleshooting, monitoring, or recovery tasks.

Use this artifact during detailed design, operational readiness, handover, and live-service transition. It is most useful where another team must safely deploy, update, operate, monitor, support, and recover the solution after delivery.

It should align with ITIL 4 Service Configuration Management, Monitoring and Event Management, Change Enablement, and Service Desk practices by making operational ownership, release activity, monitoring, and support interactions clear. It should also reflect NIST planning discipline by making operational prerequisites, roles, dependencies, and evidence expectations explicit.

## 3. Stage Fit and Handoffs

- Stage 4: start drafting the guide when operational design, release, support, and recovery expectations become clear.
- Stage 6: complete and validate the guide against what is actually deployed and how it will really be run.
- Stage 7: use this guide as part of operational handover and readiness evidence.

Upstream sources:

- [Technical Design Document Specification](technical_design_document_specification.md)
- [Solution Module Definition Specification](../solution_deliverables/solution_module_definition_specification.md)
- [Deployed Solution Specification](../solution_deliverables/deployed_solution_specification.md)

Downstream artifacts:

- [Operations & Support Model Specification](operations_and_support_model_specification.md)
- [Operational Readiness Confirmation Record Specification](operational_readiness_confirmation_record_specification.md)

This guide should align with the Technical Design Document, Solution Module Definitions, Operations & Support Model, Access Control guidance, and Backup, Restore & Recovery Plan.

## 4. Before You Start

Confirm the following inputs are available before drafting:

- confirmed operational design or deployed scope
- named DevOps owner and Support Owner
- access and tooling inventory for the environments in scope
- understanding of environments, deployment pipeline, and release process
- reference to the Technical Design Document or equivalent
- understanding of recovery obligations, monitoring requirements, and escalation paths

## 5. How to Draft It

1. **Set operational context** — identify the system, covered environments, DevOps owner, and the live-service boundary this guide covers (see [6.1](#6.1.-operational-context)).
2. **Document access, tools, and prerequisites** — list required roles, tools, consoles, pipelines, scripts, prerequisite conditions, and secure handling notes (see [6.2](#6.2.-access,-tools,-and-prerequisites)).
3. **Describe environments and configuration** — document environments in scope, key components and pipelines, configurable items, and authoritative configuration record locations (see [6.3](#6.3.-environment-and-configuration-overview)).
4. **Write deployment, release, and change procedures** — document normal deployment steps, patching and update steps, post-change verification, rollback trigger points, and related change or approval controls (see [6.4](#6.4.-deployment,-release,-and-change-procedures)).
5. **Define routine operational tasks** — list recurring maintenance activities, frequencies, expected health-check results, known cautions, and required operational records (see [6.5](#6.5.-routine-operational-tasks)).
6. **Document monitoring, alerting, and incident response** — state what to monitor, what normal looks like, how to respond to abnormal conditions, common issues with first-line corrective actions, escalation points, and vendor dependencies (see [6.6](#6.6.-monitoring,-alerting,-and-incident-response)).
7. **Record recovery references and operational records expectations** — note when rollback or recovery should be considered, operational prerequisites, reference to the Backup, Restore & Recovery Plan, and required logs, dashboards, and records (see [6.7](#6.7.-recovery-and-operational-records-references)).

## 6. Minimum Structure

### 6.1. Operational Context

Must include:

- system, application, or service name
- covered environments
- DevOps owner or document owner
- short statement of what the solution does in operational terms
- short statement of the live-service boundary this guide covers

This section orients the reader to the system being operated.

### 6.2. Access, Tools, and Prerequisites

Must include:

- required operational roles or privileges
- required tools, consoles, pipelines, scripts, or interfaces
- prerequisite conditions or dependencies
- secure handling notes for access methods

This section tells the receiving DevOps team what is needed before work begins.

### 6.3. Environment and Configuration Overview

Must include:

- environments in scope
- important components, services, or pipelines interacted with during operation
- key configurable items
- authoritative locations for configuration records where relevant

This section provides operational orientation without repeating full design detail.

### 6.4. Deployment, Release, and Change Procedures

Must include where relevant:

- normal deployment or release steps
- patching, update, or configuration-change steps
- verification steps after deployment or change
- rollback or recovery trigger points
- references to related change, release, or approval controls

This section makes controlled operational change and repeatable release activity possible in practice.

### 6.5. Routine Operational Tasks

Must include:

- recurring operational or maintenance activities
- task frequency where relevant
- expected results or health checks
- known cautions or dependencies
- any required operational records, tickets, logs, or evidence that the DevOps team must create or update as part of controlled live operation

This section defines the ongoing operational workload.

### 6.6. Monitoring, Alerting, and Incident Response

Must include:

- what should be monitored, alerted on, or checked
- what normal status looks like
- what to do when abnormal conditions are found
- common operational issues, likely causes, and first-line corrective actions
- escalation points when local resolution is not appropriate
- vendor or specialist escalation dependencies where local teams cannot fully resolve the issue

This section supports supportability, operational continuity, and effective incident response.

### 6.7. Recovery and Operational Records References

Must include:

- when rollback, restore, or recovery should be considered
- operational prerequisites the DevOps team must know
- reference to the authoritative Backup, Restore & Recovery Plan
- important logs, dashboards, tickets, and operational records the team must create, review, or update

This section makes recovery and evidence expectations visible without duplicating the full recovery plan.

## 7. Writing Rules

Include execution-level operational detail. Another competent DevOps team should be able to perform key deployment, operational, support, and recovery tasks reliably. Do not turn it into a full design document or a secret store.

Keep the following out of this artifact:

- business-case and authorization content
- detailed architecture rationale
- raw credentials or secrets
- the full recovery strategy
- project backlog or task planning

## 8. Traceability, Ownership, and Review

The implementation lead, DevOps lead, platform engineer, or technical delivery owner usually authors the guide with operational input.

It should be reviewed by the receiving DevOps or support team and the Service Owner before handover. For systems with meaningful operational impact, operational contributors should begin shaping this guidance during solution design.

Minimum traceability expectation:

- major operational tasks align with the deployed scope and environment
- monitoring, alerting, and incident-response steps link to owning teams and escalation paths
- evidence or records required for controlled live operation are explicit

Minimum ownership expectation:

- Support Owner ensures day-to-day usability.
- Service Owner confirms operational accountability.
- Delivery Owner confirms handover completeness before closure.

## 9. Maintenance Expectations

This is a living operational document. Update it when release steps, tools, access methods, monitoring, alerting, operational dependencies, or escalation paths change.

## 10. Validation Guide

- Can a DevOps team operate the system safely from this guide?
- Are deployment, maintenance, monitoring, incident-response, and troubleshooting steps practical?
- Does the guide make evidence, escalation, and vendor-dependency expectations explicit enough for controlled support?
- Are access, records, and recovery references clear?
- Does the guide avoid becoming a design document or a secret repository?

If weak, add missing operational steps, clarify expected results, and remove design-heavy or insecure content.

## 11. Done When

- All 7 sections (operational context through recovery references) are complete and consistent with what is actually deployed.
- A DevOps team member not on the delivery team can follow the deployment and monitoring steps without additional guidance.
- Access and tooling requirements are documented securely, without raw credentials or secrets.
- Escalation paths and recovery references are explicit and point to owning teams or authoritative plans.
- The guide has been reviewed by the receiving DevOps or support team and the Service Owner.

## 12. What Comes Next

1. Review with the receiving DevOps team before handover.
2. Reference this guide in the [Operational Readiness Confirmation Record](operational_readiness_confirmation_record_specification.md).
3. Confirm alignment with the [Operations & Support Model](operations_and_support_model_specification.md) and [Backup, Restore & Recovery Plan](backup_restore_and_recovery_plan_specification.md).
4. Keep current after go-live as operational changes occur.

## 13. Prompt Guide

**Starter prompt:**

```
Draft a DevOps Guide for this solution.
Write for the DevOps team that will run and support the system after handover.
Include operational context, access prerequisites, deployment and change procedures, routine operational tasks, monitoring and incident-response guidance, recovery references, and evidence expectations.
Keep it execution-focused and secure.
```

**Validation prompt:**

```
Review this DevOps Guide against the following questions:
- Can a DevOps team operate the system safely from this guide alone?
- Are deployment, maintenance, monitoring, incident-response, and troubleshooting steps practical and complete?
- Does the guide make evidence, escalation, and vendor-dependency expectations explicit enough for controlled support?
- Are access, records, and recovery references clear and securely documented?
- Does the guide avoid design-heavy or secret-storing content?
Flag any section that is missing, vague, or unsuitable for handover.
```
