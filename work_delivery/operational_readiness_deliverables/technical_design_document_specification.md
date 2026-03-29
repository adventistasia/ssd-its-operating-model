# Technical Design Document Specification

## 1. What This Artifact Is For

The Technical Design Document explains how the solution is structured, what it depends on, and what technical decisions affect deployment, operation, security, resilience, future support, and future change.

It exists to make the technical design understandable to people other than the original implementer.

**Who uses this artifact:**

| Reader | How used |
| --- | --- |
| Solution engineers and infrastructure engineers | Understand technical structure, interfaces, environments, and constraints |
| Delivery Owner | Confirm design is detailed enough for Stage 4 control and aligned to scope |
| IT Operations / Service Owner | Understand hosting, dependencies, and design choices affecting live ownership |
| Support teams | Understand design characteristics affecting monitoring, troubleshooting, and handover |
| Security reviewers | Review security-relevant choices and trust boundaries |
| Future maintainers | Understand significant decisions, assumptions, and dependencies before making change |

## 2. When to Use It

- **Required** for solutions with meaningful technical structure, integrations, infrastructure, security controls, or ongoing support implications.
- **Conditionally required** for smaller changes where technical complexity, shared dependency, or operational dependence is still material.
- **Not usually required** for trivial, low-risk, isolated changes with no design decisions, integration, or support impact.

The practical rule: if operations, support, security, or future maintainers would need a design-level explanation to understand what was built and why, this artifact should exist.

## 3. Stage Fit and Handoffs

- Stage 4: establish the delivery-ready technical design baseline.
- Stage 6: confirm the implemented technical state and highlight material variances.
- Stage 7: provide technical evidence support for readiness, acceptance, and closure.

Upstream sources:

- [Functional Capabilities Specification](../solution_deliverables/functional_capabilities_specification.md)
- [Solution Module Definition Specification](../solution_deliverables/solution_module_definition_specification.md)
- [Use Case Narratives Specification](../solution_deliverables/use_case_narratives_specification.md)

Downstream artifacts:

- [DevOps Guide Specification](devops_guide_specification.md)
- [Operations & Support Model Specification](operations_and_support_model_specification.md)
- [Backup, Restore & Recovery Plan Specification](backup_restore_and_recovery_plan_specification.md)
- [Operational Readiness Confirmation Record Specification](operational_readiness_confirmation_record_specification.md)

## 4. Before You Start

Make sure you have:

- approved scope baseline and module definitions
- list of known integrations, environments, and infrastructure dependencies
- relevant non-functional requirements or quality targets
- security and data handling requirements where applicable
- named technical lead, Delivery Owner, and reviewer
- operational stakeholders available for review where their domains are affected

If any of these are missing, treat the design as a working draft only.

## 5. How to Draft It

Follow these steps:

1. Define the scope and boundaries of the document — what it covers and what it does not.
2. Describe the architecture overview: major components, relationships, and trust boundaries.
3. Document the environment and hosting model.
4. Identify all integrations and external dependencies, including assumptions and risks.
5. Record significant data flow and configuration decisions.
6. Note security, resilience, and control characteristics that affect operations.
7. Record performance and non-functional assumptions where they shape the design.
8. Capture significant design decisions, constraints, and known limitations.
9. Add operational notes for characteristics that affect support, monitoring, or recovery.
10. Confirm the design is at design level — move procedures to the DevOps Guide.

## 6. Minimum Structure

### 6.1. Design scope and context

Include:

- solution or service name and scope covered
- version or status
- short technical purpose statement
- author or owner, reviewers, and related references

### 6.2. Architecture and structure overview

Include:

- major components or services and how they relate
- boundaries between environments, domains, or trust zones
- diagrams or references if used

### 6.3. Environment and hosting design

Include:

- environments in scope
- hosting or platform model
- infrastructure assumptions and deployment-relevant constraints

### 6.4. Integration and dependency design

Include:

- interfaces, integrations, or service interactions
- external systems or services depended on
- dependency assumptions and operationally significant dependency risks

### 6.5. Data and configuration considerations

Include where relevant:

- important data flows or storage decisions
- configuration assumptions and configuration-sensitive design choices

### 6.6. Security, resilience, and control considerations

Include where relevant:

- security-relevant design choices
- resilience or continuity considerations
- failure points or single points of dependency

### 6.7. Performance and non-functional considerations

Include where relevant:

- performance assumptions, scale or capacity expectations, availability or service expectations

### 6.8. Significant design decisions and constraints

Include:

- decisions future maintainers need to understand
- assumptions or constraints affecting future change
- vendor or platform dependencies and non-standard support arrangements

### 6.9. Operational considerations and support-sensitive characteristics

Include where relevant:

- design characteristics that materially affect support, monitoring, restore, or handover
- references to the [DevOps Guide Specification](devops_guide_specification.md) and related operational artifacts

### 6.10. Open issues and known limitations

Include where relevant:

- unresolved design items
- accepted technical limitations
- follow-up decisions needed before handover or closure

## 7. Writing Rules

Write the design clearly enough that another competent technical team could understand the solution without relying on the original implementer.

Keep the following out:

- runbooks or routine operating procedures
- detailed administration steps
- full support workflows
- project plans, sprint plans, and task assignments
- detailed test scripts
- security assessment detail that belongs in dedicated security artifacts

If it is too vague, it will not support handover, review, or later change. If it is too detailed, it will drift into operational procedure and duplicate other artifacts.

## 8. Traceability, Ownership, and Review

Minimum traceability expectation:

- technical components and design choices trace back to approved scope references
- material dependencies, assumptions, and support implications are visible
- material technical changes and variances are reflected in related operational-readiness artifacts

Minimum ownership expectation:

- Technical lead owns design accuracy.
- Delivery Owner ensures alignment to authorized scope and stage controls.
- Operations and support reviewers validate supportability implications where materially affected.

## 9. Maintenance Expectations

Update the document when architecture, environments, dependencies, interfaces, or material technical assumptions change.

During active delivery, keep it current enough to remain the usable design baseline. After go-live, update for major technical changes that materially affect understanding, support, resilience, or future design decisions.

Minor administrative edits or inconsequential wording changes do not require formal maintenance activity.

## 10. Validation Guide

- Does the document explain how the solution is built and what major technical decisions were made?
- Are architecture, environments, integrations, and interfaces described clearly enough for a reviewer, incoming support team, or future maintainer?
- Are operational characteristics, resilience design, and critical dependencies visible?
- Are major design decisions and their rationale explicit and traceable?
- Are known limitations and open technical issues stated?
- Does the document stay at design level rather than drifting into operational procedures or test scripts?

If weak, add missing design context, make assumptions and decisions traceable, and move operational or procedural content to the [DevOps Guide](devops_guide_specification.md).

## 11. Done When

This artifact is ready when it is:

- scoped, with clear technical boundaries and coverage
- understandable, with a readable explanation of components, environments, interfaces, and constraints
- support-aware, with operationally significant dependencies and design sensitivities visible
- maintainable, with major decisions, assumptions, and known limitations explicit enough for future change
- aligned to related artifacts and approved scope references
- free from procedural overload, with detailed procedures kept in the right downstream artifacts

## 12. What Comes Next

After this baseline is confirmed:

1. draft operational administration guidance in the [DevOps Guide Specification](devops_guide_specification.md)
2. define live-service ownership in the [Operations & Support Model Specification](operations_and_support_model_specification.md)
3. define the recovery path in the [Backup, Restore & Recovery Plan Specification](backup_restore_and_recovery_plan_specification.md)
4. confirm readiness in the [Operational Readiness Confirmation Record Specification](operational_readiness_confirmation_record_specification.md)

## 13. Prompt Guide

Starter prompt:

```text
Draft a Technical Design Document for this solution.
Explain design scope, architecture overview, environments, integrations, dependencies, data and configuration considerations, security and resilience, performance assumptions, major design decisions, operationally significant characteristics, and open issues.
Keep it concise, design-level, and suitable for review, support, handover, and future change.
Do not turn it into an administration guide, project plan, or test script repository.
```

Validation prompt:

```text
Check whether this Technical Design Document explains how the solution is built and what it depends on, makes key technical assumptions and control-relevant choices visible, includes enough detail for operations and future maintainers, and stays at design level rather than drifting into operational procedure.
```
