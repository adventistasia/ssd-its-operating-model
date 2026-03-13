# Use Case Narrative Specification

## 1. Purpose

A Use Case Narrative describes how a user (actor) achieves a specific outcome using the solution.

Use Case Narratives:

- turn approved Functional Capabilities into clear, testable behavior
- define what “correct behavior” looks like for users and reviewers
- support acceptance planning and evidence later in delivery

Use cases explain behavior in business language. They are not technical design documents.

## 2. Role in the Project Delivery Framework

Use Case Narratives are part of the **Solution Deliverables** domain.

They are normally produced in **Stage 4 — Delivery Elaboration**, after scope is authorized and the team is structuring the approved scope.

They support:

- Stage 4: detailing what will be built (without changing scope)
- Stage 6: validating behavior and collecting evidence
- Stage 7: confirming acceptance against what was defined

Use cases may be drafted early to improve clarity, but they must remain consistent with the authorized scope baseline.

## 3. Alignment to the Solution Documentation Process

Use Case Narratives sit in **Step 2 — Structure Authorized Scope**.

Rules from the Solution Documentation Process apply:

- each use case must reference a **Solution Module ID (SM-###)**
- each use case must reference one or more **Capability IDs (FC-###)**
- no behavior is allowed without traceability to approved Capability IDs
- if new capability intent is discovered, update the Functional Capabilities baseline through governance before continuing

## 4. Inputs and Preconditions

You should not write use cases until these inputs exist:

- Initiative Definition (baseline intent and scope)
- Approved Functional Capabilities with stable **FC-###** IDs
- Solution Modules with stable **SM-###** IDs
- User Roles (and personas if used)
- Named Acceptance Authority and acceptance focus for the Solution Deliverables domain

## 5. What a Use Case Narrative Is

A Use Case Narrative is a structured description of:

- who is acting
- what triggers the action
- what outcome they need
- what steps happen at a high level
- what rules and checks must be applied
- what access and audit expectations exist
- what must be true to accept it as working

A use case should be small enough to test, but complete enough to remove ambiguity.

## 6. Use Case Narrative Required Contents

Each Use Case Narrative must include the sections below.

### 6.1 Identification

- **Use Case ID:** UC-###
- **Use Case Name:** clear verb phrase (e.g., “Submit Request”, “Approve Application”)
- **Solution Module ID:** SM-###
- **Capability IDs:** FC-###, FC-### (must exist in the Functional Capabilities baseline)

### 6.2 Actors

- **Primary actor:** the main user role performing the action
- **Supporting actors (if any):** other roles or systems involved

### 6.3 Trigger

- what starts the use case (event, request, schedule, or condition)

### 6.4 Intended Outcome

- what “done” means for the user (business result, not technical result)

### 6.5 Preconditions

- what must already be true before the use case can start (e.g., “user is authenticated”, “record exists”)

### 6.6 High-Level Workflow

- step-by-step outline at a business level
- include key decisions (approve/reject, valid/invalid, complete/incomplete)
- include important alternate paths (happy path + common variations)
- include failure cases and what the expected handling should be

### 6.7  Business Rules and Validations

- the checks that must be applied (eligibility rules, required fields, limits, state rules)
- the outcomes when a rule fails (clear user-facing result)

### 6.8 Access Expectations

- which roles can perform the use case
- any separation-of-duties constraints (if relevant)
- any sensitive data handling notes (if relevant)

### 6.9 Auditability Requirements

- what actions must be logged
- what must be traceable (who, what, when)

### 6.10 Acceptance Criteria

Acceptance criteria must be specific enough to test.

Include:

- observable conditions that prove the use case works
- expected results for key alternate paths
- required evidence notes (if helpful)

## 7. Writing Rules

Use Case Narratives must:

- stay aligned to the Initiative Definition and authorized scope
- stay traceable to approved FC-### IDs and one SM-### ID
- avoid technical implementation details (APIs, tables, frameworks, code)
- use simple business language
- describe behavior that can be tested and accepted
- include at least one alternate path when risk or rules make it necessary

Use Case Narratives must not:

- introduce new capability intent not present in Functional Capabilities
- change the meaning of an approved capability
- become a detailed UI specification (screens can be mentioned only when necessary for clarity)

## 8. Traceability and Change Control

### 8.1 Traceability Rules

Every use case must support traceability:

- FC-### → SM-### → UC-###

Later evidence should be traceable:

- UC-### → test evidence → deployment evidence → acceptance

### 8.2 Control Rule (Scope Protection)

If writing a use case reveals missing capability intent (new behavior), stop and:

- update Functional Capabilities through the normal agreement and governance path, then
- update Solution Modules and Use Cases to match the approved baseline

No delivery work should proceed on unapproved scope.

### 8.3 ID and Version Discipline

- UC IDs are stable once assigned
- do not reuse retired UC IDs
- record version metadata (date, author, change summary)

## 9. Quality Checks (Validation Criteria)

A set of use cases is acceptable when:

- every UC references a valid SM-### and valid FC-### IDs
- all in-scope capabilities are covered by one or more UCs (no “orphan” FCs)
- no UC introduces scope outside the authorized baseline
- actors and access expectations match the User Roles model
- business rules are clear and testable
- auditability expectations are stated for sensitive or high-risk actions
- acceptance criteria are specific and measurable
- duplication and overlap are controlled (clear boundaries between UCs)

## 10. Prompt Suggestions

Use the prompts below to draft and validate use cases quickly.

### 10.1 Prompt: Draft initial use case list (by module)

“Create an initial list of Use Cases for this project.

Inputs:

- Initiative Definition (problem, outcome, scope)
- Solution Modules (SM-### with descriptions)
- Functional Capabilities (FC-###)
- User Roles

Rules:

- Each use case must map to exactly one Solution Module (SM-###).
- Each use case must list the Capability IDs (FC-###) it implements.
- Do not introduce any new scope.

Output:

- A table with: UC-###, Use Case Name, SM-###, Actor, Included FC-### IDs, brief outcome.”

### 10.2 Prompt: Draft a full Use Case Narrative

“Draft a Use Case Narrative using this structure:

- Use Case ID (UC-###)
- Name
- Solution Module ID (SM-###)
- Capability IDs (FC-###)
- Primary actor
- Supporting actors
- Trigger
- Intended outcome
- Preconditions
- High-level workflow (steps + key decisions)
- Business rules and validations
- Access expectations
- Auditability requirements
- Acceptance criteria

Rules:

- Keep language simple.
- Describe behavior, not design.
- Do not add capabilities beyond the listed FC-###.

Use these inputs:
[PASTE the SM description]
[PASTE relevant FC statements]
[PASTE relevant user roles]”

### 10.3 Prompt: Add alternate paths and error handling

“Review this Use Case Narrative and add:

- common alternate paths
- failure cases (validation failures, missing data, permissions)
- what the user sees or what outcome happens

Rules:

- Do not add new scope.
- Keep it testable.

Output:

- Updated workflow + acceptance criteria changes.”

### 10.4 Prompt: Derive acceptance criteria that can be tested

“Convert this use case into clear acceptance criteria.

Rules:

- Each criterion must be observable and testable.
- Cover the main path and the important alternate paths.
- Do not add new scope.

Output:

- A numbered list of acceptance criteria.”

### 10.5 Prompt: Validate traceability and scope compliance

“Validate these Use Case Narratives for traceability and scope compliance.

Inputs:

- Functional Capabilities list (FC-###)
- Solution Modules list (SM-###)
- Use Cases (UC-###)

Checks:

1. Every UC references exactly one SM and at least one FC.
2. All referenced FC IDs exist in the baseline.
3. No UC introduces behavior not covered by its FC IDs.
4. Identify missing coverage: FC IDs with no UC.
5. Identify overlap: UCs that duplicate the same behavior.

Output:

- Issues found
- Specific fixes (which UC/FC to adjust)
- A simple coverage matrix (FC → UCs).”

### 10.6 Prompt: Validate access and auditability

“Validate each use case for access and auditability.

Inputs:

- User Roles
- Use Case Narratives

Checks:

- Actor role is correct and consistent
- Access expectations match role boundaries
- Sensitive actions have audit logging requirements (who/what/when)
- Separation-of-duties is respected where needed

Output:

- Issues + recommended corrections per UC.”

### 10.7 Prompt: Plain-language quality review

“Rewrite any confusing parts of these use cases in simpler language.

Rules:

- Keep intent unchanged.
- Do not add scope.
- Keep steps at a business level.

Output:

- Revised sections only, with a short note of what changed.”

