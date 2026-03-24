# DevOps Guide Specification

## 1. Purpose and Intended Outcome

The DevOps Guide defines how the solution is deployed, configured, operated, monitored, supported, and recovered in day-to-day live service.

It exists to convert delivery and implementation knowledge into repeatable operational guidance that a DevOps team can use without relying on the original implementer. A useful guide supports handover, continuity, supportability, controlled operational change, safe release activity, and sustainable live-service ownership.

The intended outcome is that a competent DevOps team can run, support, maintain, and recover the deployed system or application consistently, safely, and independently after handover.

## 2. When It Is Required

This artifact is required when a solution will be handed to a DevOps, platform, operations, or support team and has repeatable deployment, configuration, maintenance, troubleshooting, monitoring, or recovery tasks.

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

## 4. Intended Readers and Users

- DevOps teams
- platform or site reliability teams where applicable
- support teams
- Service Owner and Support Owner

## 5. Intended Project Context

Use this artifact during detailed design, operational readiness, handover, and live-service transition. It is most useful where another team must safely deploy, update, operate, monitor, support, and recover the solution after delivery.

It should align with ITIL 4 Service Configuration Management, Monitoring and Event Management, Change Enablement, and Service Desk practices by making operational ownership, release activity, monitoring, and support interactions clear. It should also reflect NIST planning discipline by making operational prerequisites, roles, dependencies, and evidence expectations explicit.

## 6. How Much Detail to Include

Include execution-level operational detail. Another competent DevOps team should be able to perform key deployment, operational, support, and recovery tasks reliably. Do not turn it into a full design document or a secret store.

## 7. Required Content or Minimum Structure

### 7.1. Operational context

Must include:

- system, application, or service name
- covered environments
- DevOps owner or document owner
- short statement of what the solution does in operational terms
- short statement of the live-service boundary this guide covers

This section orients the reader to the system being operated.

### 7.2. Access, tools, and prerequisites

Must include:

- required operational roles or privileges
- required tools, consoles, pipelines, scripts, or interfaces
- prerequisite conditions or dependencies
- secure handling notes for access methods

This section tells the receiving DevOps team what is needed before work begins.

### 7.3. Environment and configuration overview

Must include:

- environments in scope
- important components, services, or pipelines interacted with during operation
- key configurable items
- authoritative locations for configuration records where relevant

This section provides operational orientation without repeating full design detail.

### 7.4. Deployment, release, and change procedures

Must include where relevant:

- normal deployment or release steps
- patching, update, or configuration-change steps
- verification steps after deployment or change
- rollback or recovery trigger points
- references to related change, release, or approval controls

This section makes controlled operational change and repeatable release activity possible in practice.

### 7.5. Routine operational tasks

Must include:

- recurring operational or maintenance activities
- task frequency where relevant
- expected results or health checks
- known cautions or dependencies
- any required operational records, tickets, logs, or evidence that the DevOps team must create or update as part of controlled live operation

This section defines the ongoing operational workload.

### 7.6. Monitoring, alerting, and incident response

Must include:

- what should be monitored, alerted on, or checked
- what normal status looks like
- what to do when abnormal conditions are found
- common operational issues, likely causes, and first-line corrective actions
- escalation points when local resolution is not appropriate
- vendor or specialist escalation dependencies where local teams cannot fully resolve the issue

This section supports supportability, operational continuity, and effective incident response.

### 7.7. Recovery and operational records references

Must include:

- when rollback, restore, or recovery should be considered
- operational prerequisites the DevOps team must know
- reference to the authoritative Backup, Restore & Recovery Plan
- important logs, dashboards, tickets, and operational records the team must create, review, or update

This section makes recovery and evidence expectations visible without duplicating the full recovery plan.

## 8. What to Keep Out

Keep the following out of this artifact:

- business-case and authorization content
- detailed architecture rationale
- raw credentials or secrets
- the full recovery strategy
- project backlog or task planning

## 9. Relationships to Other Artifacts

This artifact should align with the Technical Design Document, Solution Module Definitions, Operations & Support Model, Access Control guidance, and Backup, Restore & Recovery Plan.

## 10. Ownership, Review, and Acceptance Expectations

The implementation lead, DevOps lead, platform engineer, or technical delivery owner usually authors the guide with operational input.

It should be reviewed by the receiving DevOps or support team and the Service Owner before handover. For systems with meaningful operational impact, operational contributors should begin shaping this guidance during solution design.

## 11. Maintenance Expectations

This is a living operational document. Update it when release steps, tools, access methods, monitoring, alerting, operational dependencies, or escalation paths change.

## 12. Traceability and Ownership Minimum

Minimum traceability expectation:

- major operational tasks align with the deployed scope and environment
- monitoring, alerting, and incident-response steps link to owning teams and escalation paths
- evidence or records required for controlled live operation are explicit

Minimum ownership expectation:

- Support Owner ensures day-to-day usability.
- Service Owner confirms operational accountability.
- Delivery Owner confirms handover completeness before closure.

## 13. Validation Guide

- Can a DevOps team operate the system safely from this guide?
- Are deployment, maintenance, monitoring, incident-response, and troubleshooting steps practical?
- Does the guide make evidence, escalation, and vendor-dependency expectations explicit enough for controlled support?
- Are access, records, and recovery references clear?
- Does the guide avoid becoming a design document or a secret repository?

If weak, add missing operational steps, clarify expected results, and remove design-heavy or insecure content.

## 14. Prompt Guide for Drafting the Artifact

### 14.1. Starter prompt

> Draft a DevOps Guide for this solution.
> Write for the DevOps team that will run and support the system after handover.
> Include operational context, access prerequisites, deployment and change procedures, routine operational tasks, monitoring and incident-response guidance, recovery references, and evidence expectations.
> Keep it execution-focused and secure.
