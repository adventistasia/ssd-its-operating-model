# User Roles, Personas & Access Model Specification

## 1. What This Artifact Is For

This artifact defines who uses the solution, what each role is trying to achieve, what user context matters, and what access boundaries apply.

This artifact answers three linked questions:

**Who is acting in the solution?**

**What do they need to do and why does it matter?**

**What are they allowed, not allowed, or required to do?**

The three parts are related but not the same:

- `Role`: a stable category of user based on responsibilities, decisions, and access needs
- `Persona`: optional real-world context that helps explain goals, behaviors, pain points, or constraints within a role
- `Access model`: the allowed actions, restrictions, conditions, and control notes that apply to roles

Use personas only when they help readers understand real-world context. Personas must not add new scope or replace role and access definitions.

## 2. When to Use It

Use this artifact when:

- the solution has more than one meaningful user group
- different roles have different tasks, decisions, or approval authority
- user context affects design, training, adoption, or support
- sensitive actions, separation of duties, or audit concerns matter
- use cases need a stable actor model and access assumptions

This artifact is usually drafted in Stage 4 before or alongside modules and use cases.

## 3. Stage Fit and Handoffs

- Stage 4: define actor, role, and access boundaries for delivery-ready behavior design.
- Stage 6: use this model to validate live-role behavior and access expectations.
- Stage 7: use this model as part of the evidence basis for acceptance and operational handover.

Upstream source:

- [Functional Capabilities Specification](functional_capabilities_specification.md)

Downstream artifacts:

- [Solution Modules Specification](solution_modules_specification.md)
- [Use Case Narratives Specification](use_case_narratives_specification.md)
- [Access Control and Authorization Model Specification](../security_privacy_and_compliance_deliverables/access_control_and_authorization_model_specification.md)
- [Training and Enablement Materials Specification](../user_adoption_and_change_enablement_deliverables/training_and_enablement_materials_specification.md)

## 4. Before You Start

Make sure you have:

- the approved scope baseline
- a list of likely actors, user groups, and supporting users
- existing evidence about user needs, frustrations, channels, devices, or working conditions where available
- known approval, access, sensitivity, or segregation concerns
- known resources, records, data types, or functions that need access control
- named owner and reviewer

If evidence is weak, keep personas light and treat assumptions as assumptions rather than facts.

## 5. How to Draft It

Follow these steps:

1. List the user roles, not individual people.
2. Define each role by business responsibility, decision authority, and access need, not by job title alone.
3. Record each role's main goals and core actions in the solution.
4. Define the access boundary for each role in terms of resources, actions, visibility, restrictions, and approval-sensitive work.
5. Note stewardship, approval, review, supervisory, or exception-handling responsibility where relevant.
6. Add personas only if different user contexts within a role materially affect use cases, design choices, training, support, or adoption.
7. Build the access model from the resources and actions that need control, not from the org chart alone.
8. Apply least privilege, default deny, and separation-of-duties thinking. Add conditions or attributes where role alone is too coarse.
9. Map the roles to the related capabilities, modules, and use cases.

Useful tests:

- If two roles do the same thing with the same boundary, combine them unless there is a control reason to keep them separate.
- If a persona starts to create new requirements, remove it or escalate the missing requirement through governance.
- If access is written only as broad statements such as "has normal access," rewrite it as role plus action plus resource plus restriction.
- If a permission exists only "just in case," remove it unless there is a named reason and owner.

## 6. Minimum Structure

### 6.1. Document header and scope note

Include:

- initiative or solution name
- version and status
- owner and reviewer
- short note on why the role, persona, and access model matters for this initiative
- short note on the scope covered by the model

### 6.2. Role catalog

Use a table like this:

| Role | Business purpose | Goals or user needs | Main actions | Decision or approval authority | Access boundary | Data sensitivity or control notes | Related IDs |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Staff member | Raises and tracks requests. | Needs to submit and monitor requests so work can be resolved. | Submit request, view own request | No approval authority | Can act only on own requests | Can view personal request data only | `FC-001`, `SM-001`, `UC-001` |

Role entries should be stable enough that downstream use cases can reuse them without reinterpretation.

### 6.3. Relationship and control notes

Add short notes for:

- reviewer or approval chains
- separation-of-duties rules
- privileged or supervisory roles
- delegated authority or temporary authority rules
- visibility rules between roles
- handoff points between internal users, external users, and supporting teams

This section makes important role relationships visible without turning the document into an org chart.

### 6.4. Optional personas

If personas are used, keep them short, evidence-based, and tied to a role.

Each persona should include:

- persona name
- linked role
- evidence basis or source note if known
- real-world context
- top goals or user needs
- behaviors or preferences that materially affect the solution
- pain points or frustrations
- constraints that matter, such as device, connectivity, language, accessibility, digital skill, time pressure, or work environment
- enablement or support note if useful

Avoid decorative biography. Include only details that change design, communication, support, or use-case thinking.

Example personas:

```text
Persona name: Maria
Linked role: Staff member
Evidence basis or source note: Assumed from branch-office feedback about mobile-first users in low-connectivity settings
Real-world context: Works from a field location and often completes requests on a phone with unstable connectivity
Top goals or user needs:
- Submit requests quickly without losing progress
- Understand whether the request was received
Behaviors or preferences that materially affect the solution:
- Uses short sessions between other tasks
- Prefers simple steps and clear confirmation
Pain points or frustrations:
- Form data is lost when the connection drops
- Long instructions are hard to follow on a small screen
Constraints:
- Mobile device only
- Low bandwidth
- Limited time per session
Enablement or support note:
- Provide simple submission guidance and clear save or confirmation messages
```

```text
Persona name: Daniel
Linked role: Staff member
Evidence basis or source note: Assumed from first-time users with low digital confidence
Real-world context: Uses the solution occasionally and is not confident with administrative systems
Top goals or user needs:
- Complete the task correctly on the first try
- Know what to do next when validation fails
Behaviors or preferences that materially affect the solution:
- Reads prompts carefully before acting
- Needs plain-language labels and errors
Pain points or frustrations:
- Unfamiliar terms slow him down
- Too many choices at once create hesitation
Constraints:
- Low digital skill
- Second-language English
Enablement or support note:
- Use plain-language prompts and clear correction guidance in related use cases and training
```

```text
Persona name: Leah
Linked role: Supervisor
Evidence basis or source note: Assumed from high-volume reviewers who manage approvals during peak periods
Real-world context: Reviews a large number of requests under time pressure and needs to make consistent decisions
Top goals or user needs:
- Process work quickly without missing control checks
- See which items need attention first
Behaviors or preferences that materially affect the solution:
- Relies on queue views, status clarity, and decision support cues
- Prefers exceptions to be obvious
Pain points or frustrations:
- Incomplete submissions create rework
- Unclear status labels slow review
Constraints:
- High workload
- Limited time for follow-up
Enablement or support note:
- Make review criteria, statuses, and exception handling explicit in use cases and support material
```

### 6.5. Access model

Use a table like this:

| Role | Resource or function | Allowed actions | Restricted actions | Conditions or limits | Approval or review basis | Audit notes | Related IDs |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Staff member | Own service requests | Create, view | Approve, reassign, view other users' requests | Authenticated user; own records only | Standard user access | Submission and status changes logged | `UC-001` |

The access model should:

- deny access by default unless an allowed action is explicitly stated
- express permissions as role plus action plus resource
- show where role hierarchy, ownership, time, location, training, case assignment, or other attributes change the rule
- call out privileged actions, temporary elevation, or break-glass access where relevant

### 6.6. Access governance notes

Add short notes for:

- how access is approved or granted at a business level
- what needs periodic review
- what events should trigger access change or removal
- how non-human, service, or shared access is treated if it exists

Keep this section governance-focused and light. Do not turn it into platform configuration detail.

## 7. Writing Rules

This artifact should define role boundaries, user context, and access expectations clearly enough that downstream artifacts stay consistent.

Use these rules:

- Roles are categories of users, not named people.
- Roles should be based on responsibilities and meaningful access differences.
- Personas should be based on evidence where possible and should focus on goals, behaviors, motivations, frustrations, and constraints that matter to solution delivery.
- Demographic detail should be included only when it materially affects the solution.
- Access should be defined in terms of permitted and restricted actions on resources or functions.
- Start with least privilege and default deny.
- Use separation-of-duties and privileged-access notes where control risk makes them relevant.
- If RBAC is not enough, add the condition or attribute that changes the access rule rather than forcing everything into one role label.

Keep the following out:

- raw account inventories
- group or directory implementation detail
- secrets or credential procedures
- full identity-platform design
- training plans
- personas written as fictional marketing profiles with no delivery value

For detailed authorization logic, use the formal access-control spec in the security domain.

## 8. Traceability, Ownership, and Review

Minimum traceability expectation:

- each role should map to related `FC-###`, `SM-###`, and `UC-###` references where relevant
- role and access terms should match the same terms used in modules and use cases

Minimum ownership expectation:

- Delivery Owner ensures this artifact stays aligned to approved scope.
- Solution lead or analyst owns drafting quality and cross-artifact consistency.
- Security reviewer validates control-sensitive role boundaries where needed.

## 9. Done When

This artifact is ready when:

- the important roles are clear and distinct
- each role has a visible purpose, goals, and main actions
- personas, if used, add useful context without changing scope
- access boundaries and control-sensitive responsibilities are visible
- privileged, supervisory, or separated duties are called out where they matter
- downstream use cases can use the same actor model and access assumptions without guessing

## 10. What Comes Next

Use this artifact to support:

1. [Solution Modules](solution_modules_specification.md)
2. [Use Case Narratives](use_case_narratives_specification.md)
3. security, training, adoption, and support artifacts where role boundaries matter
4. the detailed [Access Control & Authorization Model Specification](../security_privacy_and_compliance_deliverables/access_control_and_authorization_model_specification.md) when deeper security design is required

## 11. Prompt Guide

Starter prompt:

```text
Draft a User Roles, Personas & Access Model for Stage 4.
List the user roles, their business purpose, goals, main actions, authority, access boundary, and control notes.
Where helpful, add short evidence-based personas that clarify behavior, constraints, or support needs without adding scope.
Include an access table that states role, resource or function, allowed actions, restricted actions, conditions or limits, approval basis, and audit notes.
Use least privilege and default deny thinking.
```

Validation prompts:

```text
Check whether any role is unclear, overlaps another role without reason, or conflicts with the approved scope and planned use cases.
```

```text
Check whether any persona is decorative rather than useful, or whether any access rule is too vague because it does not name the role, resource, action, and restriction clearly enough.
```
