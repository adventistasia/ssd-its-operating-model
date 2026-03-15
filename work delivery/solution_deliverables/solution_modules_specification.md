# Solution Modules Specification

## 1. Purpose and Intended Outcome

Solution Modules organize approved functional scope into coherent delivery and acceptance groupings. They show how approved capabilities are bundled into manageable units for elaboration, validation, deployment, and acceptance.

This artifact exists to support controlled delivery without redefining scope. A useful Solution Modules artifact helps teams see how the approved capabilities are grouped, what each grouping enables, and how those groupings support later use cases and evidence.

The intended outcome is that approved capabilities are organized into manageable units that support controlled elaboration, validation, deployment sequencing, and acceptance without changing scope intent.

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

## 5. How Much Detail to Include

Include enough detail to explain what each module is for, which approved capabilities it contains, and how it supports delivery and acceptance. Do not turn it into a work breakdown structure, sprint plan, or technical architecture document.

## 6. Required Content or Minimum Structure

This artifact should define both the overall module set and the required content for each module entry.

### 6.1. Module set context

Must include:

- initiative or solution name
- version and status
- reference to the approved Functional Capabilities artifact
- short explanation of how modules are being used in this initiative

This section tells the reader how to interpret the module set.

### 6.2. Module summary view

Must include a summary of all modules. Recommended columns are:

| Module ID | Module name | Purpose | Included Capability IDs | Primary users or roles | Acceptance or validation note |
| --- | --- | --- | --- | --- | --- |

This summary gives a fast view of how approved scope is grouped.

### 6.3. Required content for each module entry

Each module entry must include:

- stable Module ID
- module name
- module purpose
- included Capability IDs
- short statement of the behavior or outcome area covered

Each module entry should include when relevant:

- primary user groups or roles
- dependencies on other modules or external systems
- planned use case references
- release or phase note
- validation or acceptance focus note when the module is used as a distinct evidence grouping

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

This section prevents modules from becoming hidden change requests.

### 6.5. Capability-to-module mapping

Must include a mapping that shows how approved capabilities are assigned to one or more modules.

Recommended columns:

| Capability ID | Capability statement | Assigned Module ID | Notes |
| --- | --- | --- | --- |

This section supports coverage review and prevents orphan capabilities.

### 6.6. Module-level validation expectations

Must include:

- how modules support testing, deployment, or acceptance grouping
- statement that module validation must be traceable back to approved capabilities and related use cases
- statement on how cross-module behavior or shared dependencies will be handled when evidence cannot be isolated to one module

This section explains why the module structure matters operationally.

## 7. What to Keep Out

Keep the following out of this artifact:

- new business scope
- detailed use case narratives
- sprint or task plans
- detailed technical design
- raw evidence logs

## 8. Relationships to Other Artifacts

This artifact depends on the Functional Capabilities artifact and should inform Use Case Narratives, validation structure, deployment planning, and acceptance evidence.

## 9. Ownership, Review, and Acceptance Expectations

The artifact is usually prepared by the Delivery Owner, business analyst, or solution lead with business owner input.

It should be reviewed by the Business Owner / Process Owner, Delivery Owner, and leads responsible for testing, release, or elaboration. It usually supports acceptance rather than functioning as a separate acceptance record.

## 10. Maintenance Expectations

Maintain the module structure while the initiative is being elaborated and delivered. Update when approved scope changes, module boundaries shift materially, or coverage gaps are found.

## 11. Validation Guide

- Does each module group approved capabilities in a coherent way?
- Can a reviewer see that modules organize scope rather than change it?
- Are all approved capabilities assigned to one or more modules?
- Is it clear how cross-module behavior will be validated without creating ownership ambiguity?
- Is the per-module information specific enough to guide use cases and evidence planning?
- Does the artifact avoid drifting into task planning or design?

If weak, clarify module purpose, add the missing mapping, and remove content that belongs in use cases or delivery plans.

## 12. Prompt Guide for Drafting the Artifact

### 12.1. Starter prompt

> Draft a Solution Modules artifact that groups the approved Functional Capabilities into coherent delivery and acceptance units.
> For each module, include its purpose, included Capability IDs, primary users or roles, and any dependencies that matter for delivery and validation.
> Do not invent new scope or turn the modules into task plans.

### 12.2. Section prompts

> Create a module summary table using the required fields in this specification and show how the modules help controlled delivery and acceptance.

> Build a capability-to-module mapping and identify any approved capabilities that are currently unassigned or ambiguously assigned.

### 12.3. Validation prompts

> Check whether any module entry implies new business scope not present in the Functional Capabilities artifact.

> Check whether the module set is clear enough to support use case drafting and module-level validation.
