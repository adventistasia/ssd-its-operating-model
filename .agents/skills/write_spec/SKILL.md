---
name: write_spec
description: >
  Build clear IT initiative, solution, or operational specifications that make intent, scope, accountability, and traceability explicit.
  Use when a user asks to draft, review, extend, or rework a specification for any delivery artifact (charter, capability brief, solution design, support model, compliance record, etc.) so the content is clear before work starts, visible while work is in progress, and accountable in ownership and decisions.
---

# Write spec skill

## Gather context
- Before drafting, open and review `specification_writing_guide.md` so you align with its section guidance and examples.
- Capture the artifact name plus its role (governance, delivery, implementation, operations, or compliance) and the audience who will sign, consume, or act on it.
- Clarify why it exists: what trigger, capability gap, business outcome, or risk it resolves; link to the supporting initiative or operating model artifact (e.g., reference `its_operating_model.md` or `its_work_management_model.md`).
- Ask for measurable success criteria, acceptance tests, or definition of done, and record any timelines or milestones that constrain the work.
- Document the authoring owner(s) and supporting SMEs who will keep the spec current.

## Draft the structure
Use the sections in `specification_writing_guide.md` as the base template, but keep them practical:
1. **Purpose & value** (intent, why now, and how it supports delivery/governance).
2. **Problem/opportunity statement** (current state, gaps, or requests) plus desired outcomes.
3. **Scope boundaries** (what is included, what is excluded, dependencies, handoffs, and affected capabilities).
4. **Governance, decisions, and approvals** (list decision points, required approvals, and owners; explicitly call out pending decisions that block progress).
5. **Roles, responsibilities, and accountability** (who leads, who supports, and who owns support/maintenance).
6. **Success criteria & acceptance** (metrics, KPIs, compliance checks, or quality gates).
7. **Assumptions, risks, and constraints** (including policy, compliance, technology, or capacity constraints).
8. **Traceability references** (link to higher-level initiatives, policies, and artifacts; note iterations and change history).
9. **Support & sustainment** (handover plan, documentation, runbook, and owner for ongoing operations).

## Emphasize governance and traceability
- Record every decision with the owner’s name and decision date; use bullet lists or tables to keep this visible.
- Track traceability by linking each section back to a requirement, policy, or capability, especially when describing acceptance criteria or controls.
- Preserve scope boundaries by noting what was deliberately excluded and why; this prevents scope creep.
- If the spec changes, log the change rationale, author, and effective date so a reviewer can follow the evolution.

## Engage the user iteratively
- When details are missing (e.g., scope, dependencies, success metrics), ask clarifying questions such as “Who signs off on the completion?”, “Which policies or compliance regimes must we satisfy?”, or “What downstream teams rely on this output?”
- Share the draft structure before fully writing to ensure the owner agrees on terminology and priorities.
- After drafting, walk through the spec with stakeholders to confirm the decision log, owners, and acceptance criteria are accurate.

## References
- Use `specification_writing_guide.md` for canonical sections and examples.
- Consult `its_operating_model.md` and `its_work_management_model.md` for governance expectations, work visibility requirements, and accountability structures.
