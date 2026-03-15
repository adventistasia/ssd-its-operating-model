# Solution Modules Specification

## 1. Purpose and Intended Outcome

Solution Modules organize approved functional scope and related use case behavior into coherent delivery and acceptance groupings. They show how approved Functional Capabilities are bundled into manageable units for elaboration, validation, deployment, and acceptance.

This artifact exists to support controlled delivery without redefining scope. A useful Solution Modules artifact helps teams see how the approved Functional Capabilities and related Use Case Narratives are grouped, what each grouping enables, and how those groupings support validation evidence and formal acceptance.

For initiatives using modular delivery, each Solution Module is the primary unit of solution delivery, behavior validation, and business acceptance.

The intended outcome is that approved Functional Capabilities are organized into manageable units that support controlled elaboration, validation, deployment sequencing, and acceptance without changing scope intent.

## 2. When It Is Required

This artifact is required when approved scope is large or structured enough that the initiative needs explicit delivery and acceptance groupings.

It is recommended for most multi-capability initiatives and especially useful for phased delivery or module-level validation.

## 3. Intended Readers and Users

- Delivery Owner and implementation leads
- analysts and designers
- test and validation leads
- Business Owner / Process Owner
- release and operations stakeholders

## 4. Intended Project Context

Use this artifact after the Functional Capabilities artifact is approved and before detailed behavioral definition is complete. It is most useful where the team needs clear units of delivery and evidence without changing approved business scope.

It should align with PMI scope-structuring and work decomposition practice by grouping approved scope into manageable units without changing the authorized baseline. It should also align with ITIL 4 release and service validation thinking by creating meaningful units of delivery and acceptance.

The module structure should make it clear what can be delivered, tested, evidenced, and accepted together as one controlled unit.

## 5. How Much Detail to Include

Include enough detail to explain what each module is for, which approved Functional Capabilities it contains, which Use Case Narratives define its behavior, and how it supports delivery and acceptance. Do not turn it into a work breakdown structure, sprint plan, or technical architecture document.

## 6. Required Content or Minimum Structure

This artifact should define both the overall module set and the required content for each module entry.

### 6.1. Module set context

Must include:

- initiative or solution name
- version and status
- reference to the approved Functional Capabilities artifact
- reference to the related Use Case Narratives set or drafting approach
- short explanation of how modules are being used in this initiative

The explanation of module use must state whether Solution Modules are the primary delivery and acceptance units for the initiative.

This section tells the reader how to interpret the module set.

### 6.2. Module summary view

Must include a summary of all modules. Recommended columns are:

| Module ID | Module name | Purpose | Included Functional Capabilities | Planned Use Case IDs | Primary users or roles | Acceptance or validation note |
| --- | --- | --- | --- | --- | --- | --- |

This summary gives a fast view of how approved scope is grouped.

### 6.3. Required content for each module entry

Each module entry must include:

- stable Module ID
- module name
- module purpose
- included Functional Capabilities
- planned or related Use Case IDs
- short statement of the behavior or outcome area covered

Each module entry should include when relevant:

- primary user groups or roles
- dependencies on other modules or external systems
- release or phase note
- validation or acceptance focus note when the module is used as a distinct evidence grouping
- named Acceptance Authority where module-level acceptance is being tracked

Each module entry must not include:

- new capabilities not present in the approved baseline
- detailed use case flows
- technical design implementation detail
- task assignments or sprint-level planning

This entry structure makes the module usable for downstream elaboration and evidence planning.

### 6.4. Module boundary rules

Must include:

- what kinds of behavior are included in a module
- how exclusions or out-of-bound behavior should be expressed
- rule that modules organize approved scope and do not authorize new scope
- rule that related Use Case Narratives must stay within the module's approved capability boundary

This section prevents modules from becoming hidden change requests.

### 6.5. Functional Capability-to-module mapping

Must include a mapping that shows how approved Functional Capabilities are assigned to one or more modules.

Recommended columns:

| Functional Capability | Functional Capability statement | Assigned Module ID | Notes |
| --- | --- | --- | --- |

This section supports coverage review and prevents orphan capabilities.

### 6.6. Module-level validation expectations

Must include:

- how modules support testing, deployment, or acceptance grouping
- statement that module validation must be traceable back to approved Functional Capabilities and related use cases
- statement on how cross-module behavior or shared dependencies will be handled when evidence cannot be isolated to one module
- statement that a module is accepted when its included Functional Capabilities are implemented and its related use cases meet the agreed validation and acceptance criteria

This section explains why the module structure matters operationally.

## 7. What to Keep Out

Keep the following out of this artifact:

- new business scope
- detailed use case narratives
- sprint or task plans
- detailed technical design
- raw evidence logs

## 8. Relationships to Other Artifacts

This artifact depends on the Functional Capabilities artifact and the related Use Case Narratives. It should inform validation structure, deployment planning, and acceptance evidence.

## 9. Ownership, Review, and Acceptance Expectations

The artifact is usually prepared by the Delivery Owner, business analyst, or solution lead with business owner input.

It should be reviewed by the Business Owner / Process Owner, Delivery Owner, and leads responsible for testing, release, or elaboration.

Where modular delivery is being used, the module definition should be strong enough that reviewers can see what behavior will be delivered and accepted together. Module acceptance evidence should normally be recorded in the broader Solution Deliverables Acceptance Record rather than in this artifact itself.

## 10. Maintenance Expectations

Maintain the module structure while the initiative is being elaborated and delivered. Update when approved scope changes, module boundaries shift materially, or coverage gaps are found.

## 11. Validation Guide

- Does each module group approved Functional Capabilities in a coherent way?
- Can a reviewer see that modules organize scope rather than change it?
- Are all approved Functional Capabilities assigned to one or more modules?
- Are the related use cases visible enough to show what behavior will be tested and accepted with the module?
- Is it clear how cross-module behavior will be validated without creating ownership ambiguity?
- Is the per-module information specific enough to guide use cases and evidence planning?
- Does the artifact avoid drifting into task planning or design?

If weak, clarify module purpose, add the missing mapping, and remove content that belongs in use cases or delivery plans.

## 12. Prompt Guide for Drafting the Artifact

### 12.1. Starter prompt

> Draft a Solution Modules artifact that groups the approved Functional Capabilities into coherent delivery and acceptance units.
> For each module, include its purpose, included Functional Capabilities, primary users or roles, and any dependencies that matter for delivery and validation.
> Do not invent new scope or turn the modules into task plans.

### 12.2. Section prompts

> Create a module summary table using the required fields in this specification and show how the modules help controlled delivery and acceptance.

> Build a Functional Capability-to-module mapping and identify any approved Functional Capabilities that are currently unassigned or ambiguously assigned.

### 12.3. Validation prompts

> Check whether any module entry implies new business scope not present in the Functional Capabilities artifact.

> Check whether the module set is clear enough to support use case drafting and module-level validation.
