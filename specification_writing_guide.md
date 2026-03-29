# Specification Writing Guide

## 1. Purpose

This guide defines how to write and maintain deliverable specifications for planned ITS work.

A good specification tells a new person:

- what the artifact is for
- when they need it
- what must go in it
- how to draft it without guesswork
- when it is done

Use this guide when creating or revising a specification for any planned delivery artifact — governance documents, solution deliverables, operational artifacts, security or compliance records, data artifacts, or user adoption materials.

This guide also governs how AI agents should use specifications as drafting inputs. A specification written to this standard should produce a practical, bounded artifact — not a generic template.

---

## 2. Writing Principles

### 2.1 Start with purpose and real use

Explain why the artifact exists before describing its structure. State what problem it solves and what it enables — review, delivery, operation, acceptance, or control.

### 2.2 Use plain language

Use direct wording that tells the drafter what is needed in practice. Avoid abstract labels that sound formal but do not clearly guide drafting.

### 2.3 Keep Each Artifact Focused

Say what belongs in the artifact and what should go elsewhere. Each artifact should serve one clear purpose. If detail belongs in another artifact, direct the drafter to reference it rather than duplicate it.

### 2.4 Define usefulness, not just completeness

Do not only say what sections must exist. Explain what each section is there to achieve. Where useful, say what a good section allows a reviewer, operator, or decision-maker to do.

### 2.5 Use minimum useful structure

Define the minimum content needed for the artifact to be useful and governable. Organize required content into meaningful sections rather than one long flat list.

### 2.6 Distinguish required from optional

Use consistent wording so readers can tell the difference between required content, optional content, and illustrative examples.

Use: **Must include**, **Should include**, **May include**, **Must not include**.

### 2.7 Make traceability practical

Say who owns the artifact, what changes trigger review or update, and how it relates to upstream and downstream artifacts.

### 2.8 Number sections for usability

Use visible section numbering in specifications, especially for major sections and sub-sections. This supports review comments, governance discussions, and AI-assisted drafting.

---

## 3. When to Use Which Pattern

There are two patterns: the **light pattern** and the **extended pattern**. Most specifications use the light pattern. Choose based on the properties of the artifact, not by default.

### Choosing a Pattern

Use the **light pattern** when the artifact is:

- produced once (or updated infrequently) during delivery
- primarily used to enable a decision, build a solution, or record an outcome
- unlikely to need formal version control or ongoing update obligations after it is accepted

Use the **extended pattern** when the artifact is one or more of the following:

- a **living document** that must be kept current over the life of an initiative or service (add Maintenance Expectations)
- a **formal governance baseline** that an approver will sign off on and later compare against delivery outcomes (add Validation Guide)
- a **complex operational or technical control document** where "done when" bullets alone are not sufficient to assess readiness

---

## 4. Standard Light Pattern — Section-by-Section Guide

Every light-pattern specification uses these 11 sections in this order.

### Section 1 — What this artifact is for

State in plain language: what the artifact is, why it exists, and what question it answers. Include the intended audience as a short sentence if it is not obvious from context. Keep this to one or two short paragraphs.

### Section 2 — When to use it

State when the artifact is required, conditionally required, or optional. Include scaling guidance: when a lighter version is appropriate, and when a fuller version is needed. Name the initiative types or risk conditions that make it necessary.

### Section 3 — Stage fit and handoffs

Name the upstream sources this artifact draws from, and the downstream artifacts it feeds. Use relative markdown links where practical. This replaces the old "Relationships to Other Artifacts" section.

### Section 4 — Before you start

List the minimum inputs needed before drafting begins. If a key input is missing, the output should be treated as a working draft. Common inputs include: approved scope, named owner, confirmed stage, approved requirements or constraints.

### Section 5 — How to draft it

Numbered steps. Keep to 5–8 steps. Each step should be a concrete action, not an abstract instruction.

### Section 6 — Minimum structure

The required sections, fields, tables, and entries the artifact must contain. For each major section, state what it must include and why it matters. Where the artifact is table-based or record-based, define the required fields per row or entry. Keep example tables where they exist.

### Section 7 — Writing rules

Content quality rules for this specific artifact, followed by "Keep the following out:" bullets that name what belongs elsewhere.

### Section 8 — Traceability, ownership, and review

Name: who owns creation of the artifact, what upstream artifact it traces back to, what downstream artifact it feeds forward to, who reviews it. This replaces the old "Ownership, Review, and Acceptance Expectations" and "Relationships to Other Artifacts" sections.

### Section 9 — Done when

Short bullet list of minimum readiness conditions. The artifact is ready to use when all of these are true. For most artifacts, 4–6 bullets are enough.

### Section 10 — What comes next

Numbered list of next actions or linked artifacts. Usually 3–5 items.

### Section 11 — Prompt guide

Two code blocks:

1. **Starter prompt** — a ready-to-use prompt for drafting the artifact from the specification
2. **Validation prompt** — a prompt for checking whether a draft meets the specification

---

## 5. Extended Pattern Additions

Start with all 11 standard sections. Then add the following where warranted.

### Maintenance expectations — living documents only

Add this section after section 8 when the artifact is expected to change over time. State:

- whether it is a living document
- what should be kept current
- what changes trigger an update or new version

Do not add this section to static records, one-time approvals, or point-in-time evidence artifacts.

### Validation guide — complex governance baselines only

Add this section when "Done When" is not enough to assess a complex governance baseline. Use it for:

- Initiative Definition Document
- Project Charter
- Formal Acceptance and Closure Record
- Operations and Support Model
- Operational Readiness Confirmation Record

When used, the validation guide should help a reviewer assess whether the artifact is complete, decision-ready, and consistent with its approved scope. Structure it as a numbered checklist with short explanations, not as a generic quality rubric.

---

## 6. Writing Style Rules

- Use title-case for section headings within numbered sections (e.g., "What This Artifact Is For", "Stage Fit and Handoffs", "Done When").
- Use "Must include:" not "Required:".
- Use relative markdown links between specifications.
- Preserve stable IDs (FC-###, SM-###, UC-###, BR-###, etc.) wherever they appear.
- Keep example tables and their column structures.
- Keep numbered steps in "How to draft it".
- Keep code-block prompt guides.
- Do not pad specifications with unnecessary content.
- Do not repeat content that is fully covered by a linked upstream specification.
- Do not rename files.

---

## 7. Traceability Rules

Every specification must show the work chain: from upstream authorization to downstream acceptance.

Maintain this path where relevant:

> Work Assessment → Initiative Definition or Work Brief → Functional Capabilities → Solution design and operational artifacts → Delivery evidence → Acceptance, handover, and closure records

Key rules:

- Downstream content must not contradict the approved upstream baseline without making the change explicit.
- Where a stable ID exists (FC-###, SM-###, etc.), preserve it and show the traceability link.
- Link to the authoritative source document rather than copying its content.
- Use relative markdown links to link between specifications and supporting artifacts.

---

## 8. Scope and Detail Rules

Match the amount of detail to the artifact's actual purpose.

| Artifact type | Target detail level |
|---|---|
| Stage 1 screening artifact | Enough to decide whether to proceed — no design |
| Stage 2 decision-ready document | Enough to authorize — no implementation detail |
| Stage 3 authorization record | Explicit decision, basis, conditions — not a design |
| Stage 4 elaboration artifact | Enough to build, configure, or implement correctly |
| Stage 5–6 delivery artifact | Enough to demonstrate what was done and why |
| Stage 7 closure record | Enough to confirm acceptance, handover, and remaining conditions |

Do not force full initiative document packs when a Work Brief is sufficient.

Do not under-specify work that is broad, risky, cross-team, compliance-sensitive, security-sensitive, data-sensitive, or operationally significant.

Common scoping failures to avoid:

- Forcing detailed design into a Stage 2 definition document
- Carrying operational runbooks inside a design summary
- Duplicating content that belongs in a linked artifact
- Making examples look mandatory
- Creating hidden mandatory work through vague wording

---

## 9. AI-Assisted Drafting Notes

When an AI agent uses a specification to draft an artifact, it must:

- Stay inside the scope boundary defined by the specification
- Treat missing key inputs as a signal to produce a working draft, not a complete one
- Label the draft clearly when key inputs are absent
- Not invent evidence, approvals, decisions, or completion status
- Not authorize work, approve scope changes, assign owners, or mark deliverables accepted
- Not silently expand scope through elaboration or design detail

A specification written to this standard should give an AI agent enough structure to produce a practical, bounded first draft without major guessing.

If the specification is unclear about a boundary, the agent should flag the ambiguity rather than resolve it silently.

---

## 10. Practical Review Test

Before finalizing a specification, check:

1. Can a new person read this and understand whether they need the artifact?
2. Can they tell when it is required versus optional?
3. Can they identify what must go in it and what must stay out?
4. Can they draft it without guessing about structure or content?
5. Can they tell when it is done?
6. Does it link to the right upstream and downstream artifacts?
7. Are owners and reviewers named where needed?
8. Could an AI agent use this to produce a useful, bounded first draft?

If any answer is "no" or "not clearly," revise that section before using the specification.

---

## Appendix A — Section folding reference

When revising a heavy-pattern specification to the light pattern, fold sections as follows:

| Old section | Fold into |
|---|---|
| Intended Readers and Users | Section 1 (short paragraph) or Section 2 |
| Intended Project Context | Section 2 (When to use it) |
| How Much Detail to Include | Section 7 (Writing rules, as leading guidance) |
| Relationships to Other Artifacts | Section 3 (Stage fit and handoffs) |
| Ownership, Review, and Acceptance Expectations | Section 8 (Traceability, ownership, and review) |
| Lifecycle and Change Control | Maintenance Expectations (extended pattern only) or remove |
| Required Content or Minimum Structure | Section 6 (Minimum structure) |
| Validation Guide | Section 9 (Done when) for most; keep as Validation Guide only for complex governance baselines |
| Prompt Guide for Drafting the Artifact | Section 11 (Prompt guide) |
