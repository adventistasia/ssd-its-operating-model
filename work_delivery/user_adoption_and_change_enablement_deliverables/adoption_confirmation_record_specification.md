# Adoption Confirmation Record Specification

## 1. What This Artifact Is For

The Adoption Confirmation Record provides formal confirmation that impacted user groups were informed, required enablement activities occurred, key adoption risks were reviewed, and the Business Owner acknowledges user readiness.

It exists to keep readiness evidence visible rather than assumed. A useful record shows which groups were prepared, what evidence supports that conclusion, what risks remain, and who confirmed readiness.

The intended outcome is that user readiness is acknowledged on the basis of visible evidence, with remaining adoption risks and conditions made explicit before release or handover.

Intended readers include: Business Owner, Change or Communications Lead, Delivery Owner, and governance reviewers.

## 2. When to Use It

Use this artifact when the initiative needs formal confirmation that adoption preparation was completed before or shortly after go-live.

Use it near rollout or go-live, after communications and enablement activities have been delivered. It is most useful where user readiness must be evidenced and attributable, not just informally stated.

It should align with PMI stakeholder-readiness and acceptance discipline by linking user preparation to evidence and ownership. It should also align with ITIL organizational change management by making readiness acknowledgement explicit.

In the Work Delivery Framework lifecycle, this artifact is primarily a Stage 7 acceptance and closure input, supported by evidence collected during Stage 5 and Stage 6.

## 3. Stage Fit and Handoffs

| Stage | Role of this artifact |
| --- | --- |
| Stage 5–6 – Mobilization and Delivery | Evidence collected as communications and enablement are delivered |
| Stage 7 – Acceptance, Transition & Closure | Primary use: formal readiness confirmation as part of acceptance package |

**Upstream inputs:**

- [User Impact Assessment](user_impact_assessment_specification.md) — defines which user groups require preparation and what adoption risks apply
- [Change & Communication Plan](change_and_communication_plan_specification.md) — provides evidence of planned and delivered communications
- [Training & Enablement Materials Specification](training_and_enablement_materials_specification.md) — provides evidence of enablement delivery
- [Adoption Support Model](adoption_support_model_specification.md) — provides evidence of support arrangements

**Downstream outputs:**

- [Acceptance Record Specification](../solution_deliverables/acceptance_record_specification.md) — references adoption confirmation as part of solution acceptance
- [Formal Acceptance & Closure Record Specification](../governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md) — includes adoption confirmation as part of formal closure

## 4. Before You Start

Confirm the following before drafting:

- communications have been delivered
- enablement activities have been completed
- adoption evidence collected by user group
- named Business Owner and change lead
- readiness status known for each user group
- any deferred or conditional groups identified

## 5. How to Draft It

1. Complete the record identity section (§6.1).
2. Populate user group rows with readiness status and evidence references (§6.2).
3. Record the Business Owner acknowledgment (§6.3).
4. Review for unsupported readiness claims and make conditions explicit.

## 6. Minimum Structure

### 6.1. Record Identity

Must include:

- initiative or rollout name
- record version and date
- prepared by
- scope of user groups covered
- statement of whether the record covers full rollout readiness, phased readiness, or a limited audience subset

This section identifies what readiness claim the record is making.

### 6.2. Required Content for Each User-Group Row

Each row must include:

- user group
- communication completed
- enablement completed
- remaining risk or condition
- evidence reference
- readiness status where a group is deferred, conditionally ready, or not yet covered

Recommended table:

| User group | Communication completed | Enablement completed | Readiness status | Remaining risk or condition | Evidence reference |
| --- | --- | --- | --- | --- | --- |

This row structure makes the basis for readiness visible and reviewable.

### 6.3. Business Owner Readiness Acknowledgment

Must include:

- formal acknowledgment by the Business Owner or delegated authority
- date of acknowledgment
- any conditions or limitations attached to the acknowledgment

This section is the actual readiness decision.

## 7. Writing Rules

Keep it concise. Include enough detail to show what readiness actions occurred, what evidence exists, what risks remain, and who confirmed readiness.

Keep the following out of this artifact:

- the full training content
- campaign asset libraries
- detailed issue logs unless they materially affect readiness

## 8. Traceability, Ownership, and Review

The Change or Communications Lead or Business Owner representative usually prepares the record.

The Business Owner normally confirms the readiness acknowledgment and acts as the normal Acceptance Authority for adoption readiness unless a formal delegation is recorded.

The Delivery Owner is accountable for ensuring this readiness record is available as part of the Stage 7 acceptance package.

## 9. Maintenance Expectations

Update until readiness is confirmed. If readiness is conditional, keep the conditions visible or issue a superseding version when they are closed.

## 10. Done When

- User group rows are populated with evidence references and readiness status.
- Remaining risks or conditions are visible and owned.
- Partial, phased, or conditional readiness is explicit rather than implied.
- Business Owner acknowledgment is recorded with date.
- Record does not rely on unsupported readiness claims.

## 11. What Comes Next

1. Include as part of the Stage 7 acceptance package.
2. Reference in the [Acceptance Record](../solution_deliverables/acceptance_record_specification.md) and [Formal Acceptance & Closure Record](../governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md).
3. Track open conditions to closure and issue a superseding version when they are closed.
4. Confirm any deferred group coverage before full closure.

## 12. Prompt Guide

### 12.1. Starter Prompt

```
Draft an Adoption Confirmation Record for this initiative.
Summarize which user groups were informed, what enablement occurred, what risks or conditions remain, and the Business Owner's readiness acknowledgment.
Keep it concise and evidence-based.
```

### 12.2. Validation Prompt

```
Review this Adoption Confirmation Record.
Check that: user group rows are populated with evidence references and readiness status; remaining risks or conditions are visible and owned; partial, phased, or conditional readiness is explicit; the Business Owner acknowledgment is recorded with a date; and the record does not rely on unsupported readiness claims.
Identify any gaps and suggest where evidence references or conditional readiness need to be made clearer.
```
