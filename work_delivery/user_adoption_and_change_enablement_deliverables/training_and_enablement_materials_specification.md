# Training & Enablement Materials Specification

## 1. What This Artifact Is For

Training & Enablement Materials provide the practical guidance users need to perform expected behaviors correctly and consistently after the change.

They exist to translate solution behavior into usable guidance for real user groups. A useful training and enablement set helps users complete their tasks correctly, understand important cautions, and know where to get help when they are unsure.

The intended outcome is that affected users can perform the new or changed work correctly, consistently, and with enough confidence to reduce adoption friction and avoid preventable errors.

Intended readers include: impacted end users, trainers or facilitators, Change or Communications Lead, Business Owner, and support teams.

## 2. When to Use It

Use this artifact when the initiative changes user tasks, decision logic, system interaction, or compliance-relevant behavior enough that users need structured support.

Use it after user impacts and core behaviors are known but before adoption is expected. It is most useful where users need task-level support rather than only high-level awareness.

It should align with PMI stakeholder-readiness practice and with ITIL organizational change management and knowledge-sharing intent by making user guidance role-specific, practical, and supportable.

In the Work Delivery Framework lifecycle, these materials are usually elaborated in Stage 4, prepared and scheduled in Stage 5, and delivered and refined during Stage 6 based on readiness and feedback.

## 3. Stage Fit and Handoffs

| Stage | Role of this artifact |
| --- | --- |
| Stage 4 – Work Definition Details | Elaborated once user impacts and task behaviors are confirmed |
| Stage 5 – Delivery Mobilization | Prepared and scheduled for delivery |
| Stage 6 – Work Delivery | Delivered and refined based on readiness and feedback |

**Upstream inputs:**

- [User Impact Assessment](user_impact_assessment_specification.md) — identifies affected roles and adoption risks that shape content scope
- [Use Case Narratives Specification](../solution_deliverables/use_case_narratives_specification.md) — defines expected user task flows and behaviors
- [User Roles, Personas & Access Model Specification](../solution_deliverables/user_roles_personas_and_access_model_specification.md) — clarifies role scope and access context

**Downstream outputs:**

- [Adoption Confirmation Record](adoption_confirmation_record_specification.md) — receives evidence of enablement delivery

**Also relates to:**

- [Change & Communication Plan Specification](change_and_communication_plan_specification.md)
- [Adoption Support Model Specification](adoption_support_model_specification.md)

## 4. Before You Start

Confirm the following before drafting:

- completed User Impact Assessment identifying affected roles
- confirmed solution behavior and task flows from Use Case Narratives
- named training lead or change lead
- delivery format constraints identified (accessibility, language, time)
- scheduled enablement window confirmed

## 5. How to Draft It

1. Complete the material context header (§6.1).
2. Write task-specific content for each material set (§6.2).
3. Define delivery and format approach (§6.3).
4. Review for generic content, missing cautions, and unclear help paths.

## 6. Minimum Structure

### 6.1. Material Context

Must include:

- target audience or role
- enablement objective
- date or version
- owner

This section identifies who the material is for and what it is trying to enable.

### 6.2. Required Content for Each Material Set

Must include:

- tasks or behaviors the material supports
- instructions, examples, walkthroughs, or references suited to the role
- key cautions, common mistakes, or decision points
- where users get help if they are unsure

This section makes the material usable in practice.

### 6.3. Delivery and Format Notes

Should include:

- whether the material is self-service, facilitated, walkthrough-based, or quick-reference based
- any role-specific constraints affecting how the material should be used
- accessibility, language, timing, or format considerations where those factors affect effective adoption

This section helps teams choose the right enablement form, not just the right content.

## 7. Writing Rules

Include enough detail that the intended user can complete the relevant task correctly. Keep the content role-specific and task-focused. Do not turn it into a full system design or policy manual.

Keep the following out of this artifact:

- unnecessary technical design detail
- unrelated policy text
- content for roles not in scope

## 8. Traceability, Ownership, and Review

The training lead, change lead, or business subject matter expert usually prepares these materials with input from process owners and support teams.

The Delivery Owner is accountable for ensuring training and enablement outputs stay aligned with approved scope and rollout sequencing. The Business Owner or delegated Acceptance Authority should confirm that required user groups received fit-for-purpose enablement before final acceptance.

## 9. Maintenance Expectations

Update when user tasks, interfaces, rules, or support channels change materially. Retire outdated guides promptly where they could cause user error.

## 10. Done When

- Intended user can complete the task correctly using the material.
- Content is role-specific and task-focused.
- Cautions, common mistakes, and help paths are visible.
- Delivery format suits the target audience.
- Content does not drift into design or policy detail.

## 11. What Comes Next

1. Deliver materials per the [Change & Communication Plan](change_and_communication_plan_specification.md) schedule.
2. Reference delivery evidence in the [Adoption Confirmation Record](adoption_confirmation_record_specification.md).
3. Align help and escalation paths with the [Adoption Support Model](adoption_support_model_specification.md).
4. Retire and update materials promptly when tasks or interfaces change.

## 12. Prompt Guide

### 12.1. Starter Prompt

```
Draft Training & Enablement Materials for this initiative.
Write for the specific user role, explain the tasks they must perform, highlight important cautions, and show where they can get help if needed.
Keep the guidance role-specific and practical.
```

### 12.2. Validation Prompt

```
Review these Training & Enablement Materials.
Check that: the intended user can complete the task correctly using the material; content is tailored to a specific role or audience; cautions, common mistakes, and help paths are visible; the delivery format suits the real constraints of the target audience; and the material stays task-focused rather than drifting into design or policy documentation.
Identify gaps and suggest where content should be simplified or refocused on real tasks.
```
