# Use Case Narratives Specification

## 1. Purpose and Intended Outcome

Use Case Narratives describe how users achieve defined outcomes using the solution. They turn approved Functional Capabilities into reviewable, testable, and acceptance-ready behavior.

This artifact exists to reduce ambiguity about how the solution should behave from the user's point of view. A useful use case set shows who is acting, what triggers the action, what outcome is intended, what rules matter, what exceptions are important, and what observable conditions prove the behavior is correct.

The intended outcome is that user-visible behavior and expected results are explicit enough to guide design, validation, and acceptance without guesswork.

Where Solution Modules are being used as delivery and acceptance units, the Use Case Narratives define the behavior that must be validated for each module.

## 2. When It Is Required

This artifact is required when behavioral clarity is needed to design, validate, or accept the solution.

It is especially important for role-based workflows, approvals, exception handling, sensitive actions, and any scope where misunderstanding user behavior would create delivery or acceptance risk.

## 3. Intended Readers and Users

- business reviewers
- analysts and designers
- developers and test teams
- Acceptance Authorities
- security or control reviewers where sensitive behavior is involved

## 4. Intended Project Context

Use this artifact after the Functional Capabilities artifact and Solution Modules are defined. It is most useful when the team needs business-behavior detail that remains traceable to approved scope.

It should align with ISO/IEC/IEEE 29148 requirements-elaboration principles by turning approved scope into clearer behavioral detail without changing the baseline. It should also align with ITIL 4 service validation and testing intent by making expected behavior explicit, reviewable, and testable.

The use case set should make it clear what behavior must work for a Solution Module to be considered delivered and ready for acceptance.

## 5. How Much Detail to Include

Include enough detail that a business reviewer, tester, or AI drafter can understand and validate the behavior without inventing missing steps or rules. Keep the description at business-behavior level. Do not turn the artifact into a UI specification, API specification, or full test script.

The level of detail should be sufficient to support module-level walkthroughs, testing, and acceptance evidence.

## 6. Required Content or Minimum Structure

This artifact should define both the required content for each use case and the rules that keep the set traceable and bounded.

### 6.1. Use case set context

Must include:

- reference to the Initiative Definition Document
- reference to the Functional Capabilities artifact and Solution Modules
- version or status of the use case set

Should include:

- short statement of how the use case set supports module-level validation and acceptance

This section identifies what approved baseline the behavior descriptions belong to.

### 6.2. Required content for each use case

Each use case must include:

- Use Case ID
- use case name
- related Module ID
- related Functional Capabilities
- primary actor
- supporting actors or systems where relevant
- trigger
- intended outcome
- preconditions
- postconditions or resulting state where that matters to validation, auditability, or downstream processing
- main flow
- alternate and exception paths where relevant
- business rules and validations
- access expectations where relevant
- auditability requirements where relevant
- acceptance criteria

Each use case should be self-contained enough that a reviewer can understand the expected behavior without reading multiple other documents first.

### 6.3. Guidance for each required section

The use case entry should describe the following in practical terms:

- `Trigger`: what starts the use case
- `Intended outcome`: what successful completion means for the user or business process
- `Main flow`: the high-level business steps and decision points
- `Alternate and exception paths`: important variations, failures, rejections, or error conditions
- `Business rules and validations`: the checks or conditions that materially affect correct behavior
- `Access expectations`: which role may perform the action and any separation-of-duties or sensitivity constraints
- `Auditability requirements`: what must be traceable and why
- `Postconditions or resulting state`: what should be true after completion if the use case succeeds or fails materially
- `Acceptance criteria`: observable results that prove the use case works correctly

This section keeps the required structure usable rather than heading-only.

### 6.4. Traceability rules

Must include rules stating that:

- every use case must map to one defined Solution Module
- every use case must reference one or more approved Functional Capabilities
- no use case may introduce new scope outside the approved baseline
- module-level validation evidence must be traceable to the use cases used to define the behavior

This section protects scope and supports later evidence tracing.

### 6.5. Coverage expectations

Must include:

- expectation that all in-scope Functional Capabilities are covered by one or more use cases where behavior needs to be defined
- expectation that overlap and duplication between use cases should be controlled
- expectation that each module has enough use case coverage to support module-level acceptance

This section helps the use case set function as a complete behavior model instead of a partial sample.

### 6.6. Template guide

Recommended use case headings:

| Field | What it should contain |
| --- | --- |
| Use Case ID | Stable ID such as `UC-###` |
| Use Case name | Clear verb-led title |
| Module ID | One related Solution Module |
| Functional Capabilities | Approved Functional Capabilities only |
| Main flow | High-level business steps and decisions |
| Acceptance criteria | Observable outcomes, not vague intentions |

If the artifact becomes heavily tabular, keep the flow, exceptions, and rules readable and do not collapse everything into one line per use case.

## 7. What to Keep Out

Keep the following out of this artifact:

- technical implementation design
- detailed screen layouts
- API or database specifications
- full test scripts
- new business scope not traceable to approved Functional Capabilities

## 8. Relationships to Other Artifacts

This artifact should align with the Functional Capabilities artifact, Solution Modules, User Roles, Personas & Access Model, Access Control & Authorization Model, Audit & Monitoring Design Summary, module-level validation evidence, and final acceptance evidence.

## 9. Ownership, Review, and Acceptance Expectations

Use Case Narratives are usually authored by analysts or functional leads with business owner input.

They should be reviewed by the Business Owner / Process Owner, Delivery Owner, test lead, and security reviewers where access or sensitive behavior is material.

Use Case Narratives normally support module-level validation and feed the broader Solution Deliverables Acceptance Record rather than functioning as stand-alone acceptance records.

## 10. Maintenance Expectations

Keep the use case set current while behavior is still being elaborated and whenever approved behavior changes. Update when business rules, roles, or acceptance conditions change materially.

## 11. Validation Guide

- Does every use case trace back to approved modules and capabilities?
- Is each use case complete enough to understand expected behavior without major guessing?
- Are alternate paths, rules, and sensitive behaviors visible where they matter?
- Are the resulting state and downstream effects clear where acceptance or control depends on them?
- Are acceptance criteria observable and testable?
- Is the use case set sufficient to support module-level testing and acceptance without inventing missing behavior?
- Does the artifact stay at business-behavior level rather than drifting into design?

If weak, tighten traceability, complete the missing sections, and remove technical detail.

## 12. Prompt Guide for Drafting the Artifact

### 12.1. Starter prompt

> Draft a Use Case Narrative for this solution behavior.
> Include the required fields from this specification, keep the behavior traceable to the approved Module and Functional Capabilities, describe the main and alternate paths in business language, and make the acceptance criteria observable and testable.
> Do not introduce new scope or technical design detail.

### 12.2. Section prompts

> Draft the main flow and alternate paths so a business reviewer can understand the behavior and a tester can validate it.

> Draft the access, audit, and acceptance sections so sensitive or controlled behavior is explicit and reviewable.

### 12.3. Validation prompts

> Check whether this use case introduces behavior outside the approved Functional Capabilities.

> Check whether the use case is complete enough for a reviewer or AI drafter to use without inventing missing rules or outcomes.
