# User Impact Assessment Specification

## 1. What This Artifact Is For

The User Impact Assessment identifies which user groups are affected by the initiative, what changes in their behavior or process, and what adoption risks must be managed.

It exists to make user change visible before communications, training, and support plans are finalized. A useful assessment tells the organization who is affected, how their work changes, where the change is most difficult, and which groups need focused support.

The intended outcome is that user impacts and adoption risks are understood early enough to shape targeted communications, training, support, and readiness decisions.

Intended readers include: Business Owner, Change or Communications Lead, Delivery Owner, training and support leads, and process owners.

## 2. When to Use It

Use this artifact when the initiative changes user behavior, responsibilities, approvals, process steps, tools, or communication needs.

Use it during planning and elaboration, before launch communications and training are finalized. It is most useful where adoption success depends on understanding different levels of user impact rather than treating all audiences the same.

It should align with PMI stakeholder engagement and communications practice by identifying affected groups and the significance of change for each. It should also align with ITIL organizational change management intent by making readiness and resistance factors visible early.

In the Work Delivery Framework lifecycle, this artifact is commonly identified in Stage 2 when user impact shapes authorization discussions, elaborated in Stage 4, and used in Stage 5 and Stage 6 to drive communication, enablement, and support priorities.

## 3. Stage Fit and Handoffs

| Stage | Role of this artifact |
| --- | --- |
| Stage 2 – Work Definition | Identified when user impact shapes authorization discussions |
| Stage 4 – Work Definition Details | Elaborated with full group-level impact detail |
| Stage 5–6 – Mobilization and Delivery | Drives communication, enablement, and support priorities |

**Upstream inputs:**

- [Initiative Definition Document Specification](../governance_and_control_deliverables/initiative_definition_document_specification.md) — provides approved scope and initiative context
- [User Roles, Personas & Access Model Specification](../solution_deliverables/user_roles_personas_and_access_model_specification.md) — identifies user types and role structure
- [Use Case Narratives Specification](../solution_deliverables/use_case_narratives_specification.md) — describes expected user behavior and task flows

**Downstream outputs:**

- [Change & Communication Plan](change_and_communication_plan_specification.md) — uses impact assessment to target audiences and messages
- [Training & Enablement Materials Specification](training_and_enablement_materials_specification.md) — uses impact assessment to scope content by role
- [Adoption Support Model Specification](adoption_support_model_specification.md) — uses impact assessment to define support priorities
- [Adoption Confirmation Record Specification](adoption_confirmation_record_specification.md) — references high-impact groups when confirming readiness

## 4. Before You Start

Confirm the following before drafting:

- approved initiative scope
- completed or draft Use Case Narratives or user role model
- known rollout approach
- named Business Owner and change lead
- understanding of user groups and their current working practices

## 5. How to Draft It

1. Complete the assessment context header (§6.1).
2. Describe each impacted user group (§6.2).
3. Identify high-priority groups needing focused attention (§6.3).
4. Populate the summary table (§6.4).

## 6. Minimum Structure

### 6.1. Assessment Context

Must include:

- initiative or rollout name
- scope of the assessment
- date or version
- owner

This section identifies what change scenario the assessment covers.

### 6.2. Required Content for Each Impacted User Group

Each impacted group entry must include:

- user group or role
- current-state behavior summary
- future-state behavior summary
- nature and scale of change
- main adoption risks or resistance factors
- business criticality or consequence if the group does not adopt correctly where that matters

This section is the core impact model of the artifact.

### 6.3. High-Priority Impact Notes

Should include:

- groups needing focused enablement
- groups needing focused communication or support
- constraints such as low digital confidence, low bandwidth, high volume, or time-critical work

This section helps downstream readiness planning become targeted rather than generic.

### 6.4. Template Guide

Recommended columns:

| User group | Current state | Future state | Scale of change | Main risks or resistance | Support need |
| --- | --- | --- | --- | --- | --- |

Use short entries that focus on behavior and operating impact, not general opinions.

## 7. Writing Rules

Include enough detail to show who is affected, what changes for them, and where adoption risk exists. Do not turn it into a full communication plan or training catalog.

Keep the following out of this artifact:

- detailed communication calendars
- full training content
- technical design detail

## 8. Traceability, Ownership, and Review

The change lead, business analyst, or Business Owner usually coordinates this artifact.

Review should include process owners and teams representing affected users.

The Delivery Owner is accountable for ensuring this assessment is reflected in delivery planning and mobilization decisions. The Business Owner, as the usual Acceptance Authority for adoption outcomes, should confirm that high-impact groups are addressed before final acceptance.

## 9. Maintenance Expectations

Update when user groups change, solution behavior changes materially, or new adoption risks are discovered.

## 10. Done When

- Affected user groups are identified with current and future state described.
- Scale of change and main adoption risks are visible per group.
- High-priority groups needing focused support are identified.
- The summary table is populated.
- Downstream communication and training decisions can be based on the assessment.

## 11. What Comes Next

1. Use as input to the [Change & Communication Plan](change_and_communication_plan_specification.md).
2. Use to scope [Training & Enablement Materials](training_and_enablement_materials_specification.md).
3. Reference when defining the [Adoption Support Model](adoption_support_model_specification.md).
4. Confirm high-impact groups are addressed before the [Adoption Confirmation Record](adoption_confirmation_record_specification.md) is prepared.

## 12. Prompt Guide

### 12.1. Starter Prompt

```
Draft a User Impact Assessment for this initiative.
Identify the affected user groups, how their behavior or responsibilities will change, the scale of change, and the main adoption risks or resistance factors.
Keep it focused on practical user impact and readiness.
```

### 12.2. Validation Prompt

```
Review this User Impact Assessment.
Check that: affected user groups are identified with current and future state described; scale of change and adoption risks are visible per group; high-priority groups needing focused support are called out; the summary table is populated; and downstream communication and training decisions can be based on this assessment.
Identify any gaps and suggest where group-level impacts should be sharpened or where assessment has drifted into mitigation planning.
```
