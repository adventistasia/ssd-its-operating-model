# Business Rules Catalog Specification

## 1. What This Artifact Is For

The **Business Rules Catalog** is a centralized record of the rules, validations, policies, and approval conditions that govern solution behavior across modules and use cases. It provides a single place to document and trace the rules that determine correct behavior, decision logic, and exception handling.

It answers questions like:

* **What rules must be applied for this solution to operate correctly and compliantly?**
* **Why does each rule exist and what policy or rationale supports it?**
* **Where does each rule apply — which module, use case, or process step?**
* **What is the impact of the rule on decisions and outcomes?**

Having a catalog prevents rule duplication, fragmentation, and inconsistency. It helps solution designers, developers, testers, and auditors see which rules matter, why they exist, and how they affect behavior. Intended readers include delivery owners, solution leads, developers, testers, compliance reviewers, and auditors.

## 2. When to Use It

Use this artifact in **Work Definition Details (Stage 4)** when the solution contains numerous validations, approval conditions, or decision logic that cut across multiple modules or use cases. It is especially useful when:

* Policy or regulatory rules must be applied consistently throughout the solution.
* Approvals or exception handling depend on clear and repeatable rules.
* Multiple modules share the same validation logic.
* Complex branching or conditional flows need to be traceable.
* Auditability requires that rules and their rationales be documented explicitly.

For simple systems with minimal rules, it may be sufficient to document rules directly in use case narratives or module definitions. As the number or complexity of rules grows, a separate catalog improves clarity and traceability.

## 3. Stage Fit and Handoffs

* **Work Definition Details (Stage 4):** Draft the catalog alongside Solution Module Definitions and Use Case Narratives. Identify rules, rationale, affected modules and use cases, and validation implications.
* **Delivery Mobilization (Stage 5):** Review the catalog with policy owners, compliance officers, or subject matter experts. Refine as needed and baseline the rules.
* **Work Delivery (Stage 6):** Use the catalog to guide development and testing. Link rules to test cases and evidence in the Validation & Evidence Matrix.
* **Acceptance, Transition & Closure (Stage 7):** Reference the catalog during acceptance to confirm that mandatory rules have been implemented and validated.

Upstream sources:

* [Functional Capabilities Specification](functional_capabilities_specification.md)
* Policy and regulatory documents relevant to the initiative
* SME input and governance policies

Downstream artifacts:

* [Solution Module Definition Specification](solution_module_definition_specification.md)
* [Use Case Narratives Specification](use_case_narratives_specification.md)
* [Validation & Evidence Matrix Specification](../governance_and_control_deliverables/validation_and_evidence_matrix_specification.md)

## 4. Before You Start

Make sure you have:

* A list of modules and use cases where rules will apply.
* Access to relevant policies, legal requirements, or regulatory obligations.
* Subject matter experts who can explain the rationale behind each rule.
* Agreement on identification conventions — use `BR-###` identifiers for stable traceability.
* A named owner and reviewer for the catalog.

If any of these are missing, treat the catalog as a working draft and label it as such.

## 5. How to Draft It

1. **Identify rules.** Gather all business rules, approval conditions, validations, and exception criteria from Functional Capabilities, Use Case Narratives, policy documents, and SME interviews.
2. **Assign a stable identifier.** Give each rule a unique `BR-###` ID to facilitate traceability and change control.
3. **Write the rule statement.** Describe the rule in clear, concise language. Include any conditions or thresholds that trigger the rule.
4. **Record the rationale.** Explain why the rule exists. Reference policies, legal requirements, business rationale, or risk controls.
5. **List affected modules and use cases.** Identify where the rule applies. Link to the relevant `SM-###` and `UC-###` IDs.
6. **Describe decision impact.** State how the rule influences decisions, outcomes, or system behavior — for example, reject a request, require approval, or apply a threshold.
7. **Define validation and evidence needs.** Note how the rule will be tested or validated and what evidence will demonstrate compliance.
8. **Add notes or remarks.** Include any additional comments, open questions, or known exceptions.

## 6. Minimum Structure

Use a table like this:

| Rule ID | Rule statement | Rationale / Policy basis | Affected modules / use cases | Decision impact | Validation & evidence | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| `BR-001` | Approver must be a manager in the requestor's department. | Company Policy XYZ | `SM-002`, `UC-008` | Requests from other departments require re-assignment to correct approver. | UAT; audit log | Exceptions only for emergency scenarios |
| `BR-002` | Requests over $5,000 require finance approval. | Finance Policy 12-B | `SM-001`, `UC-003` | Adds finance approval step. | Functional test; evidence of approval captured | Threshold indexed annually |

## 7. Writing Rules

Each rule statement should be unambiguous and state both the condition and the required outcome or constraint clearly. Rationale entries should point to the policy, legal requirement, or control objective that requires the rule — not just say "required by policy."

Keep the following out:

* detailed process or workflow descriptions that belong in use case narratives
* test scripts or test cases
* UI design or screen behavior descriptions
* implementation or platform configuration detail

## 8. Traceability, Ownership, and Review

This artifact traces back to Functional Capabilities and the policy or regulatory documents that govern the initiative.

It feeds forward to Solution Module Definitions, Use Case Narratives, and the Validation & Evidence Matrix.

Ownership expectations:

* Delivery Owner is accountable for catalog completeness and stage-control use.
* Solution Lead owns rule quality, clarity, and cross-artifact consistency.
* Compliance or policy owner reviews rules that originate from corporate or regulatory obligations.
* Reviewer confirms that all material decision logic is represented and traceable.

## 9. Done When

* Each rule has a unique `BR-###` ID and a clear statement.
* The rationale and policy basis for each rule are recorded.
* Affected modules and use cases are listed for each rule.
* The decision impact and validation needs are documented.
* The catalog is reviewed and approved by the Delivery Owner and relevant policy or compliance authorities.

## 10. What Comes Next

1. Use catalog entries to complete and cross-reference [Solution Module Definitions](solution_module_definition_specification.md) and [Use Case Narratives](use_case_narratives_specification.md).
2. Reference `BR-###` IDs in test planning and link evidence in the [Validation & Evidence Matrix](../governance_and_control_deliverables/validation_and_evidence_matrix_specification.md).
3. Keep the catalog current during delivery as rules are clarified or policy guidance changes.
4. Include catalog reference in acceptance and closure records where compliance or audit traceability is required.

## 11. Prompt Guide

Starter prompt:

```text
Create a Business Rules Catalog for Work Definition Details (Stage 4).
List each rule with a unique BR-### ID, the rule statement, rationale or policy basis, affected modules and use cases (SM-### and UC-### IDs), and the expected decision impact and validation method.
Use a table format for clarity.
```

Validation prompt:

```text
Check whether the Business Rules Catalog identifies all relevant rules, assigns unique BR-### IDs, states the rationale and policy basis, lists affected modules and use cases, and defines validation and evidence needs.
```
