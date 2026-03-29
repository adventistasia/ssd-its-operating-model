# Non-Functional Requirements Specification

## 1. What This Artifact Is For

The **Non-Functional Requirements Specification** defines the cross-cutting qualities the solution must exhibit to be acceptable in production. While Functional Capabilities describe what the solution must do, this artifact describes **how well** it must do it.

It answers questions such as:

* **How fast must the solution respond or process?**
* **How reliable and available must it be?**
* **How will it scale with demand?**
* **What usability, accessibility, or regulatory standards apply?**
* **What security, privacy, and auditability qualities are required?**

Documenting these expectations early helps teams make design decisions, plan testing, and agree on acceptance criteria that reflect real-world demands rather than implicit or conflicting assumptions. Intended readers include delivery owners, outcome owners, solution leads, technical designers, testers, and IT operations.

## 2. When to Use It

Use this specification during **Work Definition Details (Stage 4)** whenever the solution's success depends on qualities beyond basic correctness. It is especially useful when:

* Performance, throughput, latency, or responsiveness matter for user satisfaction or operational viability.
* Reliability, availability, failover, or disaster recovery capabilities will influence design or cost.
* Usability, accessibility, or ergonomic factors affect adoption and compliance.
* Compliance with specific industry, regulatory, or corporate standards is required.
* The solution must scale beyond current volumes, users, or locations.
* Changes to non-functional qualities could introduce business risk or require explicit funding.

For very small, non-critical initiatives, these qualities may be captured within other artifacts such as use cases or module definitions. For anything with multiple users, integrations, or service-level commitments, a dedicated specification clarifies expectations and prevents unstated assumptions from driving late-stage disputes.

## 3. Stage Fit and Handoffs

* **Work Definition Details (Stage 4):** Draft quality attributes based on the Problem & Outcome Validation Brief, Functional Capabilities, and known operational expectations. Review them with the Outcome Owner, Delivery Owner, Solution Lead, and operational stakeholders.
* **Delivery Mobilization (Stage 5):** Refine and baseline the attributes as part of mobilization planning, linking them to test planning and budgeting.
* **Work Delivery (Stage 6):** Use the attributes to guide performance, reliability, usability, and compliance testing. Record evidence and deviations in the Validation & Evidence Matrix.
* **Acceptance, Transition & Closure (Stage 7):** Refer to the attributes when determining whether delivered behavior meets the agreed acceptance quality.

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
* A named owner and reviewer with authority to set or negotiate quality targets.

If any of these are missing, treat the draft as a working draft and label it as such.

## 5. How to Draft It

1. **Identify applicable quality attributes.** Common categories include performance, reliability, scalability, usability, accessibility, maintainability, portability, security, privacy, auditability, interoperability, and regulatory compliance. Select only those that are material to the initiative.
2. **Define target levels.** For each attribute, state the target or range — for example, response time under 2 seconds for 95% of interactions, availability 99.9%, time to restore under 4 hours, WCAG 2.1 AA compliance. Include the rationale and highlight trade-offs if targets may conflict.
3. **Assign stable identifiers.** Give each requirement a unique `QA-###` ID to aid traceability and cross-referencing in the Decision Record Log and Validation & Evidence Matrix.
4. **Specify measurement and monitoring.** Describe how each attribute will be measured — for example, synthetic testing, load tests, accessibility audits, security scanning — and what monitoring and alerting will be required in operations.
5. **Link to modules and use cases.** Where different modules or use cases have different quality expectations, state those differences or note which parts of the solution are most affected by each attribute.
6. **Note constraints and assumptions.** Record any constraints, dependencies, or assumptions that affect the ability to meet the target — for example, third-party SLAs, network latency, or deployment environments.
7. **Review and agree.** Validate the targets with stakeholders, ensuring they are realistic, measurable, and aligned with budget and delivery expectations.

## 6. Minimum Structure

### 6.1. Document header

Include initiative name, version, status, owner, reviewer, and date. Summarize the purpose of the specification.

### 6.2. Attribute summary table

Provide a concise table listing each quality attribute and its target. Use `QA-###` IDs for traceability:

| QA-### | Attribute / Category | Target / Threshold | Applies to (FC/SM/UC) | Measurement & monitoring | Notes |
| --- | --- | --- | --- | --- | --- |
| `QA-001` | Performance – response time | 95% of user requests < 2 s | `FC-002`, `SM-003` | Load test results; real-time monitoring | Applies to request submission and search flows |
| `QA-002` | Availability | 99.9% uptime per calendar month | All modules | Availability monitoring dashboard | Excluding planned maintenance |
| `QA-003` | Accessibility | WCAG 2.1 AA compliance | All user-facing screens | Accessibility audit report | Required for compliance |

### 6.3. Attribute details

Provide additional detail for each attribute where needed, including rationale, specific scenarios, scope of applicability, dependencies, and trade-offs.

### 6.4. Measurement and monitoring expectations

Describe the tools, metrics, dashboards, or processes required to measure and monitor each attribute in production. Note any responsibilities or ownership for monitoring and responding to quality breaches.

### 6.5. Assumptions and constraints

List any assumptions, dependencies, or constraints affecting the ability to meet the targets, such as infrastructure limitations, third-party SLAs, or phased roll-out scenarios.

## 7. Writing Rules

Match target levels to real operational and business needs — avoid aspirational statements that cannot be tested. Where targets conflict or trade-offs exist, make the trade-off visible rather than hiding it. State rationale so reviewers and designers can understand why each target was set.

Keep the following out:

* detailed test scripts or test case design
* platform configuration or infrastructure provisioning detail
* operational runbooks that belong in the Operations & Support Model
* security controls or data handling rules that belong in security and privacy specifications

## 8. Traceability, Ownership, and Review

This artifact traces back to the Problem & Outcome Validation Brief and the Functional Capabilities Specification.

It feeds forward to the Technical Design Document, DevOps Guide, Validation & Evidence Matrix, and Acceptance Record.

Ownership expectations:

* Delivery Owner is accountable for ensuring quality targets are agreed and maintained within scope.
* Solution Lead owns drafting quality and cross-artifact consistency.
* Outcome Owner confirms business-facing qualities reflect real business expectations.
* IT Operations or Service Owner confirms operational qualities are feasible and supportable.
* Reviewer validates that targets are measurable and linked to evidence.

## 9. Done When

* Material quality attributes are identified and documented for the solution.
* Each attribute has a defined target, `QA-###` ID, measurement method, and rationale.
* Differences in quality expectations across modules or use cases are made visible.
* Constraints, dependencies, and assumptions affecting quality are documented.
* The specification is reviewed and agreed by the Delivery Owner, Solution Lead, Outcome Owner, and relevant operational stakeholders.

## 10. What Comes Next

1. Use quality targets to guide the [Technical Design Document](../operational_readiness_deliverables/technical_design_document_specification.md).
2. Feed `QA-###` IDs into the [Validation & Evidence Matrix](../governance_and_control_deliverables/validation_and_evidence_matrix_specification.md) for test planning and evidence tracking.
3. Establish monitoring and alerting expectations in the [DevOps Guide](../operational_readiness_deliverables/devops_guide_specification.md).
4. Reference quality targets when completing the [Acceptance Record](acceptance_record_specification.md) to confirm delivered behavior meets agreed acceptance quality.

## 11. Prompt Guide

Starter prompt:

```text
Draft a Non-Functional Requirements Specification for Work Definition Details (Stage 4).
Include the material quality attributes for this initiative, the target levels for each, how they will be measured, and any assumptions or constraints.
Assign a QA-### ID to each attribute and link them to relevant FC, SM, or UC IDs where applicable.
```

Validation prompt:

```text
Check whether the Non-Functional Requirements Specification lists all relevant non-functional qualities, defines measurable targets with QA-### IDs, explains how each will be measured and monitored, and records assumptions and constraints.
```
