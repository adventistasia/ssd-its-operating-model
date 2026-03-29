# Integration & External Dependency Specification

## 1. What This Artifact Is For

The **Integration & External Dependency Specification** documents the interfaces and dependencies the solution relies on to deliver its capabilities. It provides a clear, operational view of each integration, the contract it must meet, and how failure modes are handled.

It answers questions like:

* **What external systems or services does this solution depend on?**
* **What is exchanged — data, events, calls — and how often?**
* **Who owns each dependency and how are failures detected and managed?**
* **What fallback or degradation paths exist if the dependency is unavailable?**

By making integrations explicit, this specification reduces the risk of hidden dependencies, unmanaged failure modes, or unclear operational ownership. It complements the Technical Design Document by focusing on operational and contractual aspects rather than low-level architecture. Intended readers include delivery owners, solution leads, technical designers, IT operations, security reviewers, and dependency owners.

## 2. When to Use It

Use this specification when the solution relies on **more than one external integration or material dependency**, including:

* Calls to third-party APIs or services
* Batch or streaming data feeds
* Messaging or event subscriptions
* Shared databases or storage managed outside the initiative's control
* Legacy systems owned by other teams or vendors

It is most valuable when:

* Integration contracts affect system correctness or compliance.
* Dependencies carry their own SLAs, performance, or availability constraints.
* Failure handling, retries, or fallback behavior could materially affect user outcomes.
* Operational ownership must span multiple teams or vendors.

Draft this specification in **Work Definition Details (Stage 4)** alongside the Technical Design Document, then refine it in Delivery Mobilization (Stage 5) and Work Delivery (Stage 6) as details are clarified and tested.

## 3. Stage Fit and Handoffs

* **Work Definition Details (Stage 4):** Identify all significant integrations and dependencies. Document their purpose, contract summary, data exchanged, timing, error handling, and operational responsibilities. Assign `INT-###` identifiers.
* **Delivery Mobilization (Stage 5):** Refine the specification with input from dependency owners, security and compliance teams, and operations. Confirm SLAs, fallback strategies, and monitoring needs.
* **Work Delivery (Stage 6):** Validate integrations in testing. Update the specification with operational considerations discovered during delivery. Link integration tests and evidence in the Validation & Evidence Matrix.
* **Acceptance, Transition & Closure (Stage 7):** Use the specification to support operational handover and acceptance. Ensure service owners and support teams understand the dependencies and their responsibilities.

Upstream sources:

* [Non-Functional Requirements Specification](non_functional_requirements_specification.md)
* [Solution Module Definition Specification](solution_module_definition_specification.md)
* [Technical Design Document Specification](../operational_readiness_deliverables/technical_design_document_specification.md)

Downstream artifacts:

* [DevOps Guide Specification](../operational_readiness_deliverables/devops_guide_specification.md)
* [Operations & Support Model Specification](../operational_readiness_deliverables/operations_and_support_model_specification.md)
* [Backup, Restore & Recovery Plan Specification](../operational_readiness_deliverables/backup_restore_and_recovery_plan_specification.md)
* [Validation & Evidence Matrix Specification](../governance_and_control_deliverables/validation_and_evidence_matrix_specification.md)

## 4. Before You Start

Make sure you have:

* A list of all external systems, services, or dependencies identified during design.
* Preliminary interface documentation, SLAs, or contracts for these dependencies.
* Named owners or contacts for each dependency, internal or external.
* Knowledge of security, compliance, or data privacy constraints associated with the integration.
* A named owner and reviewer for the specification.

If any of these are missing, treat the draft as a working draft and label it as such.

## 5. How to Draft It

1. **Create an integration list.** Identify each dependency by name and assign a unique `INT-###` identifier. Include systems, services, feeds, or interfaces external to the solution team's control.
2. **Describe the purpose.** State why the dependency is needed and what capability it supports.
3. **Summarize the contract.** For each dependency, capture: data exchanged (requests, responses, messages, files); protocols or interfaces used (REST, SOAP, GraphQL, FTP, message bus, database link); frequency or timing (synchronous, asynchronous, batch, scheduled); and authentication and authorization requirements.
4. **Document operational behavior.** Describe expected response times or throughput; failure modes (timeouts, error responses, partial failures); retry and fallback strategies (number of retries, exponential backoff, circuit breaker, manual failover); and degradation or graceful shutdown behavior.
5. **Identify ownership and SLAs.** Record who owns the dependency, any service-level agreements, support contacts, and escalation paths.
6. **Define monitoring and alerts.** Note how the integration will be monitored — health checks, error rate thresholds, dashboards — and who is responsible for responding to alerts.
7. **Capture security and compliance considerations.** Document any data sensitivity classifications, encryption requirements, audit logging needs, or regulatory obligations.
8. **Note testing and validation.** Describe how the integration will be tested — mock environments, contract testing, end-to-end tests — and what evidence will be captured.
9. **Record assumptions and dependencies.** Note assumptions about dependency availability, planned decommissioning, or future changes that could affect the integration.

## 6. Minimum Structure

### 6.1. Document header

Include initiative name, version, status, owner, reviewer, and date. Summarize the purpose of the specification.

### 6.2. Integration and dependency summary table

Provide an overview of each integration using `INT-###` identifiers:

| INT-### | Name / System | Purpose | Data exchanged | Protocol / interface | Frequency / timing | Owner | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `INT-001` | Payment API | Validate and process payments | JSON over HTTPS | REST | Synchronous | Vendor X | Requires API key; SLA 99.9% |
| `INT-002` | HR system feed | Import employee data nightly | CSV via SFTP | SFTP | Nightly batch | HR IT team | Subject to HR data privacy policy |

### 6.3. Detailed integration entries

For each item in the summary table, provide:

* **Description and purpose**
* **Data exchanged**
* **Interface details** — protocol, endpoints, authentication
* **Timing and frequency**
* **Operational behavior** — normal operation, error handling, retry, fallback
* **Ownership and SLAs**
* **Monitoring and alerting**
* **Security and compliance**
* **Testing and validation**
* **Assumptions and dependencies**

### 6.4. Overall considerations

Summarize any cross-integration concerns such as combined failure impacts, sequencing constraints, shared SLA requirements, or aggregated data sensitivity issues.

## 7. Writing Rules

Each integration entry should be specific about the contract and failure behavior — avoid vague statements such as "the system handles errors gracefully." State the failure mode, the fallback path, and who is responsible for resolution.

Keep the following out:

* internal code design or platform implementation detail
* full runbooks that belong in the Operations & Support Model or DevOps Guide
* data schema definitions or field-level mapping tables that belong in technical design documents
* security platform configuration that belongs in the access control or security specification

## 8. Traceability, Ownership, and Review

This artifact traces back to Non-Functional Requirements and Solution Module Definitions.

It feeds forward to the DevOps Guide, Operations & Support Model, Backup/Restore & Recovery Plan, and Validation & Evidence Matrix.

Ownership expectations:

* Delivery Owner is accountable for ensuring all material integrations are identified and documented.
* Solution Lead owns drafting quality, completeness, and cross-artifact consistency.
* IT Operations or Service Owner confirms operational feasibility, monitoring needs, and support responsibilities.
* External dependency owners confirm accuracy of described contracts and SLAs.
* Security reviewer validates data sensitivity classifications, encryption requirements, and compliance obligations.

## 9. Done When

* All significant external integrations and dependencies are identified with `INT-###` IDs and documented.
* Each integration entry describes the data exchanged, interface details, timing, operational behavior, error handling, fallback, ownership, monitoring, and security considerations.
* SLAs, support contacts, and escalation paths are visible for each dependency.
* Testing and validation plans are stated or linked.
* The specification is reviewed and agreed by the Delivery Owner, Solution Lead, IT Operations, and any external dependency owners.

## 10. What Comes Next

1. Feed integration contracts and monitoring needs into the [DevOps Guide](../operational_readiness_deliverables/devops_guide_specification.md) for deployment and monitoring design.
2. Use operational ownership and failure-handling entries to inform the [Operations & Support Model](../operational_readiness_deliverables/operations_and_support_model_specification.md).
3. Reference `INT-###` IDs in the [Validation & Evidence Matrix](../governance_and_control_deliverables/validation_and_evidence_matrix_specification.md) for integration testing evidence.
4. Include integration risk and recovery considerations in the [Backup, Restore & Recovery Plan](../operational_readiness_deliverables/backup_restore_and_recovery_plan_specification.md).

## 11. Prompt Guide

Starter prompt:

```text
Draft an Integration & External Dependency Specification for Work Definition Details (Stage 4).
List each significant integration or external dependency with a unique INT-### identifier, describe its purpose, data exchanged, interface details, timing, operational behavior, failure handling, ownership, monitoring, and security considerations.
Use a table for the summary and detailed entries for each integration.
```

Validation prompt:

```text
Check whether the Integration & External Dependency Specification identifies all material dependencies with INT-### IDs, documents their operational contracts, and addresses failure handling, fallback, ownership, monitoring, and security considerations.
```
