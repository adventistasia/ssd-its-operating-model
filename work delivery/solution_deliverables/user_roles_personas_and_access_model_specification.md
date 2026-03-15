# User Roles, Personas & Access Model Specification

## 1. Purpose and Intended Outcome

This artifact defines the categories of users who interact with the solution, the responsibilities and goals associated with those roles, and the access boundaries that govern what each role is allowed or expected to do.

Optional personas add practical human context where role names alone are not enough to support clear use cases, access review, training, or adoption planning.

The artifact exists to make user assumptions explicit before build and acceptance. A useful role and access model gives the project a stable actor model, a clear view of role boundaries, and a practical basis for access, behavior, and enablement decisions.

The intended outcome is that user roles, access expectations, and relevant personas are clear enough to support consistent design, access control, testing, training, and acceptance decisions.

## 2. When It Is Required

This artifact is required when the solution has multiple meaningful user groups, differentiated access, privileged actions, approval authority, or sensitive data exposure.

It is strongly recommended for any solution that depends on role boundaries, separation of duties, or privacy and audit controls.

## 3. Intended Readers and Users

- Business Owner / Process Owner
- analysts and designers
- security and privacy reviewers
- Delivery Owner
- test, training, and change enablement leads

## 4. Intended Project Context

Use this artifact before detailed behavior and access implementation are finalized. It is most useful where different actors have distinct responsibilities, authority, or sensitivity exposure that must stay consistent across scope, use cases, and operational controls.

It should align with NIST SP 800-53 access-control expectations, NIST SP 800-63 digital identity guidance where assurance matters, and CIS Control 6 on access control management. When personas are used, it should also support practical change and enablement work without changing formal scope.

## 5. How Much Detail to Include

Include enough detail to make role purpose, access boundaries, and sensitive interactions understandable. Do not turn the artifact into a full identity architecture, account register, or HR organization chart.

## 6. Required Content or Minimum Structure

This artifact should define the overall user model, the required content for each role, and optional persona content where it adds real value.

### 6.1. User model context

Must include:

- solution or initiative name
- short explanation of why the role and access model matters for this initiative
- reference to approved scope or behavior artifacts

This section helps readers understand how the role model should be used.

### 6.2. Required content for each role entry

Each role entry must include:

- role name
- role purpose or description
- primary goals
- key actions or responsibilities in the solution
- access boundary
- role authority or business ownership note where the role carries approval, stewardship, or control responsibility
- data sensitivity or control notes where relevant

Each role entry should include when useful:

- typical decisions made by the role
- business outcomes the role supports
- links to related capabilities or use cases

This section defines the minimum information needed for a role to be useful in drafting and review.

### 6.3. Role relationships and control assumptions

Must include where relevant:

- reviewer or approval chains
- separation-of-duties assumptions
- visibility rules between roles
- any role interactions that materially affect behavior or access control
- identification of privileged, supervisory, or exception-handling roles that need higher scrutiny

This section is important whenever relationships between roles affect the correctness or control of the solution.

### 6.4. Role-to-solution mapping

Should include:

- mapping of roles to capabilities, modules, or use cases where that helps downstream consistency

Recommended columns:

| Role | Related capability, module, or use case | Nature of involvement | Notes |
| --- | --- | --- | --- |

This section helps keep downstream artifacts aligned to the same actor model.

### 6.5. Optional persona entries

If personas are used, each persona should include:

- persona name
- linked role
- real-world context
- key goals
- pain points or constraints
- enablement or support implications where useful

Personas must not add new scope or override the formal role boundary. They exist to improve clarity, not to create new requirements silently.

### 6.6. Access modeling cautions

Must state that the artifact:

- defines role boundaries and expectations
- does not replace the formal Access Control & Authorization Model when detailed authorization logic is required
- should not contain raw account lists or credential detail

This section keeps the artifact bounded.

## 7. What to Keep Out

Keep the following out of this artifact:

- raw account inventories
- directory group implementation detail
- secrets or credential-handling procedures
- full identity-platform design
- training plans or campaign content

## 8. Relationships to Other Artifacts

This artifact should align with the Functional Capabilities, Use Case Narratives, Access Control & Authorization Model, Security & Privacy Risk Assessment, Training & Enablement Materials, and Adoption Support Model.

Where detailed authorization logic, provisioning rules, or technical enforcement are required, the formal Access Control & Authorization Model remains the authoritative control artifact.

## 9. Ownership, Review, and Acceptance Expectations

The artifact is usually authored by analysts or solution leads with business and security input.

It should be reviewed by the Business Owner / Process Owner, Delivery Owner, and Security / Data Protection Officer where relevant. Change and training leads should review persona content where it affects adoption planning.

## 10. Maintenance Expectations

Update when role responsibilities, approval boundaries, privileged actions, or sensitivity assumptions change materially. Keep persona content current only while it remains useful and representative.

## 11. Validation Guide

- Are the role entries distinct and practically useful?
- Are access boundaries and sensitive interactions explicit where needed?
- Are role relationships captured where they materially affect behavior or control?
- Are approval, stewardship, or privileged-role responsibilities visible where they affect governance or separation of duties?
- If personas are used, do they improve clarity without adding hidden scope?
- Could downstream artifacts use this model without inventing missing actor detail?

If weak, sharpen the role distinctions, add control-relevant notes, and separate persona context from formal role boundaries.

## 12. Prompt Guide for Drafting the Artifact

### 12.1. Starter prompt

> Draft a User Roles, Personas & Access Model for this solution.
> For each role, include its purpose, goals, key actions, access boundary, and any sensitivity or control notes.
> Add role relationships where they affect approvals, visibility, or separation of duties.
> Use personas only when they improve practical clarity and do not add scope.

### 12.2. Section prompts

> Draft the role catalog so each role is distinct, behavior-oriented, and usable for downstream use cases and access review.

> Draft the role relationships section so reviewer chains, visibility rules, and separation-of-duties assumptions are explicit.

### 12.3. Validation prompts

> Check whether the role model is consistent with the approved scope and planned use cases.

> Check whether any persona content introduces hidden scope, role overlap, or unsupported assumptions.
