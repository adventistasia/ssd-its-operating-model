# ITS Operating Model – Start Here

This repository holds the ITS Operating Model, the Work Delivery Framework, and the supporting specifications used to plan, authorize, and close IT work.

---

## Which artifact do I write first?

**Start with the Initiative Definition Document.**

The [Initiative Definition Document specification](work%20delivery/governance_and_control_deliverables/initiative_definition_document_specification.md) is the primary governance baseline for any initiative. Write it before writing any design, planning, or domain artifact.

It records:
- what the initiative is and why it exists
- what outcomes it is expected to achieve
- who owns it and who will accept the result
- what deliverables are required and who is accountable for each

Everything else—solution design, data, security, operational readiness—is elaborated after this baseline exists.

> If you are working on solution design specifically, use the [Deliverable Specifications Index](work%20delivery/deliverable_specifications_index.md) for the recommended reading and drafting order.

---

## What is the minimum acceptable spec for small work?

Apply the lightest level of detail that still makes the work understandable, controllable, and supportable.

| Initiative profile | Minimum acceptable |
|---|---|
| Low complexity / low risk | One concise Initiative Definition Document, possibly combined with a Project Charter in a single controlled document |
| Medium complexity / cross-team | Separate Initiative Definition Document and Project Charter; core domain artifacts for in-scope areas with named owners and acceptance evidence |
| High complexity / high risk / regulated | Full domain-specific artifacts, traceability, and formal review and evidence |

For small work, a single combined document is acceptable **if**:
- the outcome, scope, and ownership are explicit
- required deliverables are listed with Acceptance Authorities named
- the decision to proceed is recorded

Do not skip the decision record, ownership, or acceptance—even for small initiatives.

> See [Work Delivery Framework §3 – Applicability and Scaling](work%20delivery/work_delivery_framework.md) and [Standard Deliverables Guide §5 – Minimum Viable Deliverable Depth](work%20delivery/standard_deliverables_guide.md) for full guidance.

---

## What are the required review gates before build and before deploy?

### Before build: Work Authorization (Stage 3)

No delivery work may start without explicit Work Authorization.

The gate requires:
- an approved Initiative Definition Document
- a signed-off Project Charter confirming scope, ownership, and accountability
- a funding confirmation or explicit funding condition
- a decision record from the Decision Authority (approve / defer / reject / approve with conditions)

> See [Work Delivery Framework §11 – Stage 3 Work Authorization](work%20delivery/work_delivery_framework.md).

### Before deploy: Acceptance, Transition & Closure (Stage 7)

Work is not complete until it is formally accepted.

The gate requires:
- acceptance records from the named Acceptance Authorities for each in-scope domain
- operational handover confirmation where operational ownership is impacted
- a closure record confirming final status, any remaining conditions, and assigned follow-up actions

> See [Work Delivery Framework §15 – Stage 7 Acceptance, Transition & Closure](work%20delivery/work_delivery_framework.md).

---

## Where to go next

| I want to… | Start here |
|---|---|
| Understand the full staged delivery process | [Work Delivery Framework](work%20delivery/work_delivery_framework.md) |
| Find the right deliverable spec | [Deliverable Specifications Index](work%20delivery/deliverable_specifications_index.md) |
| Browse all standard deliverables by domain | [Standard Deliverables Guide](work%20delivery/standard_deliverables_guide.md) |
| Write a well-structured specification | [Specification Writing Guide](specification_writing_guide.md) |
| Use AI to draft a deliverable | [AI-Assisted Authoring Standard](work%20delivery/ai_assisted_authoring_standard.md) |
| Understand the broader operating model | [ITS Operating Model](its_operating_model.md) |
