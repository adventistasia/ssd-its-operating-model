# Functional Capabilities Specification

## 1. Purpose and Intended Outcome

The Functional Capabilities artifact defines the approved business abilities the solution must provide. It is the functional scope baseline for the initiative.

It exists to make scope clear before detailed design, build, testing, and acceptance begin. A useful baseline helps business and delivery teams agree what the solution must be able to do without mixing in workflow detail, screen design, or implementation choices.

The intended outcome is that the initiative has a stable, outcome-aligned functional scope baseline that downstream design, build, testing, and acceptance work can trace back to.

This artifact defines what is in scope. It does not define the delivery unit or the detailed behavior to be tested for acceptance.

## 2. When It Is Required

This artifact is required when functional scope must be approved, managed, or accepted explicitly.

It is strongly recommended for any initiative with multiple stakeholders, formal acceptance, phased delivery, or non-trivial scope.

## 3. Intended Readers and Users

- Sponsor and Decision Authorities
- Business Owner / Process Owner
- Delivery Owner
- analysts and designers
- reviewers of downstream scope, testing, and acceptance artifacts

## 4. Intended Project Context

Use this artifact during definition and keep it as the approved functional baseline through delivery. It is most useful where business scope must remain stable as design and implementation detail evolve.

It should align with ISO/IEC/IEEE 29148-2018 requirements-engineering guidance by expressing clear, manageable, and reviewable requirements information items. It should also reflect PMI requirements-management discipline by preserving traceability from approved business outcomes into later delivery and acceptance artifacts.

## 5. How Much Detail to Include

Include enough detail for a reader to understand each approved business ability and why it matters. Do not include workflow steps, detailed business rules, technical design, or full acceptance criteria.

## 6. Required Content or Minimum Structure

This artifact should define both the baseline context and the capability entries that make up the approved scope.

### 6.1. Baseline context

Must include:

- initiative or solution name
- baseline version and status
- reference to the Initiative Definition Document
- short statement of the business outcome or scope area this baseline supports
- short statement of the approval boundary the baseline is intended to control

This section identifies the scope baseline and shows what approval context it belongs to.

### 6.2. Capability grouping approach

Should include:

- logical grouping of capabilities by business area when grouping improves readability
- short description of each group

This helps the reader understand how the scope is organized without changing the scope itself.

These groupings are for readability only. They do not replace the formal Solution Module structure used for delivery and acceptance grouping.

### 6.3. Required content for each capability entry

Each Functional Capability entry must include:

- stable Functional Capability ID
- capability statement written as one business ability
- business intent or value note

Each Functional Capability entry should include when useful:

- primary user role or beneficiary
- linked outcome, success measure, or scope reference
- acceptance-significant notes where a capability has material control, compliance, or operational importance
- short clarification note where ambiguity would otherwise remain

Each Functional Capability entry must not include:

- workflow sequencing
- detailed rule catalogs
- screen design
- technical implementation choices

The entry structure is the core information model of this artifact. It should allow downstream teams to derive modules, use cases, and validation without inventing new scope.

### 6.4. Capability writing rules

Must include rules stating that capability statements are:

- atomic
- non-overlapping
- expressed as business abilities
- bounded to approved scope

This section protects the baseline from becoming a process document or design artifact.

### 6.5. Baseline control rules

Must include:

- rule that downstream artifacts must remain consistent with the approved baseline
- rule for stable IDs and non-reuse of retired IDs
- statement that any new capability intent requires formal baseline revision
- statement that Solution Modules may group capabilities for delivery and acceptance but may not redefine capability intent

This section establishes how the baseline is governed.

### 6.6. Coverage and exclusion notes

Should include:

- known exclusions
- phased items
- dependencies that materially affect delivery of a capability
- explicit note of any approved business outcomes that are intentionally outside this baseline

This helps avoid false assumptions about completeness or timing.

### 6.7. Template guide

Recommended capability table columns:

| Functional Capability | Functional Capability statement | Business intent / value | Primary role | Outcome or measure supported | Notes |
| --- | --- | --- | --- | --- | --- |

Use short notes only. If a note starts to explain workflow, design, or detailed rules, move that content to a downstream artifact.

## 7. What to Keep Out

Keep the following out of this artifact:

- use case flows
- solution module structure
- detailed validation rules
- technical architecture
- UI or data design
- implementation backlog items

## 8. Relationships to Other Artifacts

This artifact should align with the Initiative Definition Document and should inform Solution Modules, Use Case Narratives, module-level acceptance planning, and the final Acceptance Record.

## 9. Ownership, Review, and Acceptance Expectations

The baseline is usually authored by a business analyst, product analyst, or delivery lead with Business Owner / Process Owner input.

It should be reviewed by the Business Owner / Process Owner, Delivery Owner, and any scope governance authority. Approval normally sits with the Business Owner / Process Owner or delegated scope authority.

## 10. Maintenance Expectations

This is a controlled baseline. Update it only when approved scope changes or when clarification is needed to remove ambiguity without changing intent. Preserve ID stability across versions.

## 11. Validation Guide

- Are the capability entries written as business abilities rather than process steps or design features?
- Is each capability understandable on its own?
- Are document-level and per-entry requirements both clear?
- Is the baseline governance rule explicit enough to prevent silent scope growth?
- Does the baseline make the approval boundary and known exclusions visible enough for later acceptance review?
- Could the capabilities be grouped into Solution Modules without inventing or splitting hidden scope?
- Could a human or AI drafter derive downstream artifacts without major guessing?

If weak, split combined capabilities, remove non-scope detail, and strengthen the baseline control rules.

## 12. Prompt Guide for Drafting the Artifact

### 12.1. Starter prompt

> Draft a Functional Capabilities artifact for this initiative.
> Define the approved business abilities the solution must provide, using stable Functional Capability references and short value statements.
> Keep the entries atomic, business-focused, and free of workflow, design, and implementation detail.

### 12.2. Section prompts

> Rewrite these proposed scope items as capability entries, each describing one approved business ability and why it matters.

> Create a capability table using the required fields in this specification and identify any entries that still contain workflow or design detail.

### 12.3. Validation prompts

> Check whether any capability entry introduces process sequence, technical design, or hidden new scope.

> Check whether every material outcome in the Initiative Definition is supported by one or more capability entries.
