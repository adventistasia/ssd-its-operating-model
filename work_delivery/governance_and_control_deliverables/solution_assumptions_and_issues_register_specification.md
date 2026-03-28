# Solution Assumptions & Issues Register Specification

## 1. What This Artifact Is For

The **Solution Assumptions & Issues Register** is a living log of unresolved design assumptions, open questions, issues and risks that emerge during solution definition and delivery. It provides transparency into uncertainties and design dependencies and helps ensure that they are tracked to resolution rather than buried in scattered notes.

It answers questions such as:

* **What assumptions are we relying on for this solution to work?**
* **What design issues, open questions or risks still need resolution?**
* **How might unresolved items affect scope, cost, quality or timeline?**
* **Who owns each assumption or issue and when will it be resolved?**

The register complements the [Decision Record Log](decision_record_log_specification.md) by making assumptions and issues visible before they become decisions. When assumptions are confirmed or issues are resolved, the outcomes should be captured as decisions in the Decision Record Log.

## 2. When to Use It

Use this register from **Stage 2** through **Stage 7**. It is most helpful when:

* There are multiple unknowns, dependencies or unanswered questions that could affect design or acceptance.
* Design assumptions could significantly change cost, timeline, quality or scope if invalidated.
* There is a risk that unresolved issues will be forgotten or rediscovered late in delivery.

It should be maintained throughout the initiative and reviewed regularly. Items that turn into decisions should cross-reference the Decision Record Log.

## 3. Stage Fit and Handoffs

* **Stage 2 – Work Definition:** use the register to capture early assumptions and open questions that need to be addressed before Functional Capabilities are approved.
* **Stage 4 – Work Definition Details:** create or update the register as design questions, assumptions and issues are identified. Review it during module definition and use case drafting.
* **Stage 5 – Delivery Mobilization:** update the register during mobilization planning and risk assessment. Assign owners and target resolution dates.
* **Stage 6 – Work Delivery:** track resolution of assumptions and issues during delivery. As items are resolved, record the outcome and reference the Decision Record Log if a decision was made.
* **Stage 7 – Acceptance, Transition & Closure:** use the register to highlight any remaining assumptions or unresolved issues that affect acceptance or require post-acceptance management.

Upstream sources:

* [Solution Module Definition Specification](../solution_deliverables/solution_module_definition_specification.md)
* [Use Case Narratives Specification](../solution_deliverables/use_case_narratives_specification.md)
* [Quality Attributes / Non-Functional Requirements Specification](../solution_deliverables/quality_attributes_specification.md)
* Team workshops, risk assessments and design reviews

Downstream artifacts:

* [Decision Record Log Specification](decision_record_log_specification.md)
* [Acceptance Record Specification](../solution_deliverables/acceptance_record_specification.md)

## 4. Before You Start

Make sure you have:

* A mechanism for capturing assumptions, questions and issues as they arise (workshops, comments, etc.).
* A naming convention for items — use `AI-###` identifiers (Assumption/Issue) for stable traceability.
* Agreement on how often the register will be reviewed and updated.
* Named owner and reviewer for the register.

## 5. How to Draft It

1. **Create an entry for each assumption or issue.** Include the type (assumption, issue, open question, risk), a description and context.
2. **Identify the impact.** Describe how the assumption or issue could affect scope, cost, timeline, quality, compliance or operations if not addressed.
3. **Link to related artifacts.** Reference the `FC-###`, `SM-###` or `UC-###` that the assumption or issue touches. If it relates to a rule (`BR-###`), integration (`INT-###`), or a quality attribute (`QA-###`), note that too.
4. **Assign an owner.** Specify who is responsible for resolving the assumption or issue.
5. **Set a target resolution date or stage.** Provide an expected timeframe for resolution.
6. **Track status.** Define status values such as Open, Under Investigation, Resolved, Deferred, or Closed. Update status as work progresses.
7. **Record the resolution.** When resolved, summarize the outcome, decisions made, implications for scope or design, and reference the Decision Record Log entry if appropriate.

## 6. Minimum Structure

Use a table like this:

| Item ID | Type (Assumption/Issue/Risk) | Description | Impact | Related artifacts | Owner | Status | Target resolution | Resolution summary / Decision reference |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| AI-001 | Assumption | API provider will deliver v2 endpoints by Q3 | Could delay integration if API is late | SM-003, UC-010 | Delivery owner | Open | Stage 5 | |
| AI-002 | Issue | Unclear whether finance approval is needed for small purchases | Could change approval flow in UC-003 | BR-002, UC-003 | SME for Finance | Under investigation | Stage 4 | |

## 7. Acceptance Criteria

* All material assumptions and issues identified during design and delivery are logged.
* Each entry describes the potential impact and references related artifacts.
* Owners and target resolution timelines are defined.
* Status updates and resolution summaries are maintained.
* Decisions arising from resolved items are captured in the Decision Record Log.

## 8. Recommended Acceptance Evidence

* Completed register showing all open and resolved items, with resolution summaries and references to the Decision Record Log.
* Endorsement from the Delivery Owner that all critical assumptions and issues have been managed appropriately.

## 9. Recommended Acceptance Authority

* Delivery Owner for completeness and management oversight.
* Outcome Owner or sponsor where assumptions or issues materially affect business outcomes.

## 10. Prompt Guide

Starter prompt:

```text
Create a Solution Assumptions & Issues Register.
List all assumptions, open questions, issues and risks identified during solution design. Include the type, description, potential impact, related artifacts (FC-###, SM-###, UC-###, BR-###, INT-###, QA-###), owner, status and target resolution.
Use a table format with AI-### identifiers and leave the resolution summary blank until resolution.
```

Validation prompt:

```text
Check whether all assumptions and issues are logged with clear descriptions, impacts, related artifacts, owners, statuses and target resolution dates, and that resolved items reference decisions or outcomes in the Decision Record Log.
```
