# Quality Attributes / Non-Functional Requirements Specification

## 1. What This Artifact Is For

The **Quality Attributes / Non-Functional Requirements (NFR) Specification** defines the cross-cutting qualities that the solution must exhibit in order to be considered acceptable in production. While Functional Capabilities describe what the solution must do, quality attributes describe **how well** it must do it.

This artifact answers questions such as:

* **How fast must the solution respond or process?**
* **How reliable and available must it be?**
* **How will it scale with demand?**
* **What usability, accessibility or regulatory standards apply?**
* **What security, privacy and auditability qualities are required?**

Documenting these expectations early helps teams make design decisions, plan testing, and agree on acceptance criteria that reflect real-world demands instead of implicit or conflicting assumptions.

## 2. When to Use It

Use this specification during **Stage 4** (Work Definition Details) whenever the solution's success depends on qualities beyond basic correctness. It is especially useful when:

* Performance, throughput, latency or responsiveness matter for user satisfaction or operational viability.
* Reliability, availability, failover or disaster recovery capabilities will influence design or cost.
* Usability, accessibility, or ergonomic factors affect adoption and compliance.
* Compliance with specific industry, regulatory or corporate standards is required.
* The solution must scale beyond current volumes, users or locations.
* Changes to non-functional qualities could introduce business risk or require explicit funding.

For very small, non-critical initiatives, these qualities may be captured within other artifacts (for example in use cases or module definitions). For anything with multiple users, integrations, or service-level commitments, a dedicated specification clarifies expectations.

## 3. Stage Fit and Handoffs

* **Stage 4:** Draft the quality attributes based on the Problem & Outcome Validation Brief, Functional Capabilities, and known operational expectations. Review them with the Outcome Owner, Delivery Owner, Solution Lead and operational stakeholders.
* **Stage 5:** Refine and baseline the attributes as part of mobilization planning, linking them to test planning and budgeting.
* **Stage 6:** Use the attributes to guide performance, reliability, usability and compliance testing. Record evidence and deviations in the Validation & Evidence Matrix.
* **Stage 7:** Refer to the attributes when determining whether delivered behaviour meets the agreed acceptance quality.

Upstream sources:

* [Problem & Outcome Validation Brief Specification](problem_and_outcome_validation_brief_specification.md)
* [Functional Capabilities Specification](functional_capabilities_specification.md)
* [Solution Modules Specification](solution_modules_specification.md)
* [Use Case Narratives Specification](use_case_narratives_specification.md)

Downstream artifacts:

* [Technical Design Document Specification](../operational_readiness_deliverables/technical_design_document_specification.md)
* [DevOps Guide Specification](../operational_readiness_deliverables/devops_guide_specification.md)
* [Validation & Evidence Matrix Specification](../governance_and_control_deliverables/validation_and_evidence_matrix_specification.md)
* [Acceptance Record Specification](acceptance_record_specification.md)

## 4. Before You Start

Make sure you have:

* A clear understanding of the problem and intended outcomes (see the Problem & Outcome Validation Brief).
* The approved Functional Capabilities and high-level scope.
* Awareness of any corporate or regulatory standards that apply.
* Preliminary operational input on expected service-level targets or supportability constraints.
* Named owner and reviewer with authority to set or negotiate quality targets.

## 5. How to Draft It

1. **Identify applicable quality attributes.** Common categories include performance, reliability, scalability, usability, accessibility, maintainability, portability, security, privacy, auditability, interoperability and regulatory compliance. Select only those that are material to the initiative.
2. **Define target levels.** For each attribute, state the target or range (for example, response time < 2 seconds for 95% of interactions, availability 99.9%, time to restore < 4 hours, WCAG 2.1 AA compliance, etc.). Include the rationale for each target and highlight trade-offs if targets may conflict.
3. **Assign stable identifiers.** Give each requirement a unique `QA-###` ID to aid traceability and cross-referencing in the Decision Record Log and Validation & Evidence Matrix.
4. **Specify measurement and monitoring.** Describe how each attribute will be measured (e.g. synthetic testing, load tests, accessibility audits, security scanning), what metrics or KPIs will be collected, and what monitoring and alerting will be required in operations.
5. **Link to modules and use cases.** Where different modules or use cases have different quality expectations, state those differences or note which parts of the solution are most affected by each attribute.
6. **Note constraints and assumptions.** Record any constraints, dependencies or assumptions that affect the ability to meet the target (for example, third-party SLAs, network latency, deployment environments).
7. **Review and agree.** Validate the targets with stakeholders, ensuring they are realistic, measurable and aligned with budget and delivery expectations.

## 6. Minimum Structure

### 6.1. Document header

Include initiative name, version, status, owner, reviewer and date. Summarize the purpose of the specification.

### 6.2. Attribute summary table

Provide a concise table listing each quality attribute and its target. Use `QA-###` IDs for traceability:

| QA-### | Attribute / Category | Target / Threshold | Applies to (FC/SM/UC) | Measurement & Monitoring | Notes |
| --- | --- | --- | --- | --- | --- |
| QA-001 | Performance – response time | 95% of user requests < 2 s | FC-002, SM-003 | Load test results; real-time monitoring | Applies to request submission and search flows |
| QA-002 | Availability | 99.9% uptime per calendar month | All modules | Availability monitoring dashboard | Excluding planned maintenance |
| QA-003 | Accessibility | WCAG 2.1 AA compliance | All user-facing screens | Accessibility audit report | Required for compliance |

### 6.3. Attribute details

Provide additional detail for each attribute where needed, including rationale, specific scenarios, scope of applicability, dependencies and trade-offs.

### 6.4. Measurement and monitoring expectations

Describe the tools, metrics, dashboards or processes required to measure and monitor each attribute in production. Note any responsibilities or ownership for monitoring and responding to quality breaches.

### 6.5. Assumptions and constraints

List any assumptions, dependencies or constraints affecting the ability to meet the targets, such as infrastructure limitations, third-party SLAs, or phased roll-out scenarios.

## 7. Acceptance Criteria

* Material quality attributes are identified and documented for the solution.
* Each attribute has a defined target, `QA-###` ID, measurement method and rationale.
* Differences in quality expectations across modules or use cases are made visible.
* Constraints, dependencies and assumptions affecting quality are documented.
* The specification is reviewed and agreed by the Delivery Owner, Solution Lead, Outcome Owner and relevant operational stakeholders.

## 8. Recommended Acceptance Evidence

* Approved Quality Attributes / NFR Specification signed by the Delivery Owner and Outcome Owner or delegate.
* Linked test plans or results showing that quality targets were considered during Stage 6.
* Monitoring and alerting configuration in the DevOps or operations environment.

## 9. Recommended Acceptance Authority

* Outcome Owner for business-facing qualities.
* IT Operations / Service Owner for operational qualities.

## 10. Prompt Guide

Starter prompt:

```text
Draft a Quality Attributes / Non-Functional Requirements Specification for Stage 4.
Include the material quality attributes for this initiative, the target levels for each, how they will be measured, and any assumptions or constraints.
Assign a QA-### ID to each attribute and link them to relevant FC, SM or UC IDs where applicable.
```

Validation prompt:

```text
Check whether the Quality Attributes specification lists all relevant non-functional qualities, defines measurable targets with QA-### IDs, explains how each will be measured and monitored, and records assumptions and constraints.
```
