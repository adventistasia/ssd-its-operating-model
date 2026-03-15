# Specification Writing Guide

## 1. Purpose

This specification defines how to write clear, useful, and governable specifications for deliverables, artifacts, and documents.

It exists to ensure that specifications:

- clearly explain why an artifact exists
- define the minimum content and expectations for that artifact
- show how the artifact supports delivery, control, operations, or acceptance
- remain readable and practical for real project use
- reduce ambiguity, rework, and document sprawl

This is a guide for writing specifications. It does not itself define every artifact used in an initiative.

The specification should also be written so that an LLM can use it as a reliable drafting guide for producing useful, practical artifacts for the intended project context and intended audience.

## 2. What This Guide Is For

Use this guide when creating or revising a specification for any planned delivery artifact, including:

- governance documents
- delivery artifacts
- design artifacts
- operational artifacts
- security or compliance artifacts
- data and records artifacts
- user adoption and change artifacts

Examples include:

- Initiative Definition specifications
- Project Charter specifications
- Functional Capabilities specifications
- Use Case Narrative specifications
- Operations and Support Model specifications
- Security assessment specifications
- acceptance record specifications

## 3. Instructions for Agents

Use this section when an agent is asked to produce a specification for a specific deliverable, artifact, or document.

### 3.1 Primary instruction

Treat this guide as the governing pattern for how the specification should be written.

Do not produce a generic template. Produce a specification that is practical for the named artifact, intended project context, and intended audience.

### 3.2 What the agent should do

When asked to draft a specification, the agent should:

1. Identify the target artifact clearly.
2. Identify or infer the intended audience for that artifact.
3. Identify or infer the project or delivery context the artifact is meant to support.
4. Use the recommended structure in Section 5 unless there is a good reason to adapt it.
5. Apply the writing principles in Section 4 while drafting.
6. Use the validation approach in Section 6 to review the specification before finalizing it.
7. Use Sections 7 to 9 when help is needed with drafting questions, prompt formulation, or the starting template.

### 3.3 What the agent should include

Unless there is a strong reason not to, the agent should include the sections listed in Section 5.

If a section is removed or adapted, the agent should do so deliberately and keep the resulting specification usable for both human and agent drafting.

### 3.4 How the agent should write required content

When writing required content, the agent should follow:

- Section 4 for writing principles
- Section 5.7 for required content structure
- Section 5.12 for validation guidance inside the produced specification
- Section 5.13 for prompt guidance inside the produced specification

In practice, this means:

- explain each major content item in short, usable terms
- distinguish required content from optional content clearly
- use meaningful sub-sections instead of flat lists when the artifact naturally has major parts
- make the content specific to the target artifact rather than generic

### 3.5 How the agent should handle boundaries

The agent should explicitly control scope by using:

- Section 4.4 for boundary thinking
- Section 5.8 for the `What to Keep Out` section
- Section 6.3 during validation

The agent should name the kinds of content that belong elsewhere when that helps avoid overlap or document sprawl.

### 3.6 How the agent should handle prompts and validation

The agent should make the resulting specification usable for future drafting and review by following:

- Section 5.12 for the validation guide inside the produced specification
- Section 5.13 for the prompt guide inside the produced specification
- Section 6 for validation of the finished specification
- Section 7 for drafting questions
- Section 8 for the recommended prompt template
- Section 9 for the minimal template and suggested prompt guide format

### 3.7 How the agent should validate its own output

Before finalizing the specification, the agent should use Section 6 to assess the draft and improve any weak areas.

The agent should present the specification only after it is satisfied that:

- the specification is practical for the target artifact
- the audience and context are clear
- the content and boundaries are usable
- the produced specification can guide a human or agent drafter without major guessing

## 4. Writing Principles for Good Specifications

Use the principles below when writing any deliverable, artifact, or document specification.

They are intended to keep the specification practical, easy to apply, and usable by both human practitioners and AI agents.

### 4.1 Start with purpose, intended outcome, and real use

Explain why the artifact exists and what intended outcome a useful finished artifact should achieve before describing its structure.

Make clear what problem it solves, what successful use of the artifact should enable, and how it supports review, delivery, operation, handover, acceptance, or control.

### 4.2 Make context and audience visible

Show who the artifact is for, what kind of initiative or situation it supports, and what would make it genuinely useful in practice.

This helps prevent generic output.

### 4.3 Use plain language and practical detail guidance

Use direct wording that tells the drafter what is needed in practice.

Avoid abstract labels or shorthand that sound formal but do not clearly guide drafting.

### 4.4 Keep the artifact bounded

Say clearly what belongs in the artifact and what should be kept out.

If detailed material belongs in another artifact, direct the drafter to reference it rather than duplicate it.

`What to Keep Out` is usually the clearest section title for this.

### 4.5 Define usefulness, not just completeness

Do not only say what sections must exist. Explain what each section is there to achieve.

Where helpful, say what a good section allows a reader, reviewer, operator, or decision-maker to understand or do.

### 4.6 Prefer minimum useful structure

Define the minimum content needed for the artifact to be useful and governable.

When the target artifact naturally has major parts, organize required content into meaningful sub-sections rather than one long flat list.

### 4.7 Distinguish required from optional

Use consistent wording so readers can tell the difference between:

- required content
- optional content
- illustrative examples

If the specification adds a real obligation, state it clearly.

### 4.8 Make review, maintenance, and traceability practical

Say who needs the artifact to be usable, what changes should trigger review or update, and how the artifact relates to other artifacts, decisions, or acceptance.

The resulting artifact should be understandable and maintainable by someone other than the original author.

### 4.9 Add practical cautions and prompt guidance where useful

Include short cautions where an artifact has common drafting failure modes.

Prompt guides should help a human or AI drafter produce a practical artifact, not just a complete-looking one.

Where useful, include:

- required inputs
- section prompts
- validation prompts

### 4.10 Recommend section numbering for usability

Where a specification has multiple major sections or sub-sections, number them so they are easy to identify, reference, review, and discuss.

Use numbering consistently in the visible headings, especially for:

- major sections
- sub-sections under a major section
- prompt guide sub-sections
- validation or checklist sub-sections where reviewers may need to cite a specific item

For example:

- `## 1. Purpose and Intended Outcome`
- `## 7. Required Content or Minimum Structure`
- `### 7.1. Baseline context`
- `### 12.2. Section prompts`

This improves traceability in review comments, governance discussions, change requests, and AI-assisted drafting.

## 5. Recommended Structure for a Specification

The sections below are the recommended default structure for writing a specification for a deliverable, artifact, or document.

Not every specification needs every section, but any section removed should be a conscious decision.

### 5.1 Document Identity

Include this section when version control, ownership, or publication status needs to be visible.

It may include:

- specification title
- version
- status
- last updated date
- owner

### 5.2 Purpose and Intended Outcome

State why the artifact exists, what need it serves, and what intended outcome the completed artifact should achieve or enable.

This section should make the artifact understandable in plain language.

Where useful, distinguish between:

- the purpose of the artifact
- the intended outcome the artifact helps produce, protect, confirm, or sustain

It should also make the intent of the specification obvious enough that an LLM can use it to produce a practical artifact rather than a generic template.

### 5.3 When It Is Required

State when the artifact is:

- required
- conditionally required
- recommended
- optional

Where helpful, describe the kinds of initiatives or risk conditions that make the artifact necessary.

### 5.4 Intended Readers and Users

Identify who needs to read, use, review, maintain, approve, or rely on the artifact.

This helps define tone, content depth, and structure.

### 5.5 Intended Project Context

State the kinds of initiatives, situations, or delivery conditions this artifact is meant to support.

This section should help the drafter understand the practical setting for the artifact.

It may include:

- the types of projects or initiatives where the artifact is most useful
- the kinds of risks, controls, or delivery conditions that shape the artifact
- whether the artifact is mainly for approval, delivery, operations, support, acceptance, or handover
- any context that helps prevent the artifact from becoming generic or misapplied

### 5.6 How Much Detail to Include

Explain how detailed the artifact should be in plain language.

This section should prevent two common failures:

- artifacts that are too vague to be useful
- artifacts that become overloaded with implementation detail

Prefer direct wording such as:

- enough detail to support approval decisions
- enough detail to explain the design clearly
- enough detail for someone else to carry out the work
- a short operating summary with links to detailed procedures elsewhere

Avoid vague shorthand such as:

- approval-level
- design-level
- control-design level
- execution-level

### 5.7 Required Content or Minimum Structure

This section is the main drafting control of the specification.

Define the minimum useful information model for the artifact, not only its headings.

List the sections, content elements, records, fields, or information categories the artifact must contain.

Do not stop at naming the headings only.

For each required section, content item, or information category, explain in short, usable terms:

- what it must include
- what it is for
- what it should help the reader understand, decide, do, validate, or accept

When the artifact naturally has major parts, structure this section in a way that reflects those parts rather than using one flat list.

Where practical, number the section and its sub-sections so reviewers and drafters can refer to them unambiguously.

When the artifact is entry-based, record-based, log-based, or table-based, define the required fields for each entry or row, not only the overall document sections.

When useful, distinguish clearly between:

- document-level required content
- per-entry or per-record required content
- required content
- recommended content
- optional content
- prohibited content

For example, a strong specification may:

- break the required content into meaningful sub-sections
- say what each sub-section must include
- add a short explanation of why that sub-section matters
- define stable IDs, mappings, or traceability fields where control depends on them
- define controlled values for statuses, decisions, classifications, or outcomes where ambiguity would create governance risk
- provide a recommended table structure or short template guide when the artifact is naturally tabular or form-like
- add short cautions where a section commonly becomes overloaded or is often misused

Use direct wording such as:

- Must include
- Should include
- May include
- Must not include

Avoid writing this section as:

- headings only
- a generic blank template with no guidance
- a long flat list when the artifact naturally has major parts

This section should be detailed enough that:

- a human drafter could produce the artifact with minimal guessing
- a reviewer could assess completeness and usefulness section by section
- an AI agent could generate a practical first draft without inventing major structure, fields, or control content

### 5.8 What to Keep Out

Explain what should be kept out of the artifact.

This section should focus on preventing overlap and document sprawl, not on repeating obvious statements about governance.

Examples:

- detailed test scripts belong elsewhere
- runbooks belong elsewhere
- task plans belong elsewhere
- build configuration belongs elsewhere

### 5.9 Relationships to Other Artifacts

Explain how this artifact connects to upstream and downstream artifacts.

Examples:

- what should exist before this artifact is written
- what artifacts this one informs
- what it should reference instead of repeating
- how it supports evidence, acceptance, or operations

### 5.10 Ownership, Review, and Acceptance Expectations

Where relevant, identify:

- who usually owns creation of the artifact
- who reviews it
- who relies on it
- whether it has a named Acceptance Authority or approval need

Not every specification needs formal acceptance rules, but governance-relevant artifacts usually need clear review expectations.

### 5.11 Maintenance Expectations

If the artifact is expected to change over time, the specification should state:

- whether it is a living document
- what should be kept current
- when it should be updated
- when a new version is needed

### 5.12 Validation Guide for the Produced Specification

Include a short validation guide that can be used to assess whether the produced specification is complete, usable, and aligned with its intended purpose.

This section should be usable by:

- a human reviewer checking the written specification
- an AI agent validating the written specification before it is used for drafting

The validation guide should help answer:

- does the specification clearly explain why the target artifact exists
- is the intended audience and project context clear
- is required content clear and usable
- is the artifact boundary clear
- is the amount of detail appropriate
- could a human or AI drafter use the specification without major guessing

Where useful, the validation guide should also say how to improve the specification if a weak area is found.

### 5.13 Prompt Guide for Drafting the Artifact

Where useful, include a short prompt guide that helps practitioners draft the target artifact from the specification.

This section should not replace the specification itself. It should translate the specification into practical drafting prompts.

The prompt guide may include:

- a starter prompt for drafting the first version of the artifact
- prompts for drafting individual sections
- prompts for checking completeness, clarity, and alignment
- prompts for improving readability and removing overlap with related artifacts

The prompt guide should be practical, simple, and consistent with the artifact boundary defined by the specification.

The prompt guide should reinforce the artifact's purpose, intended project context, and intended audience so that AI-assisted drafting stays useful and grounded.

## 6. Specification Validation Guide

Use this section to assess whether a written specification is strong enough to guide a human or AI drafter.

The goal is not only to judge quality, but also to identify how to improve a weak or incomplete specification.

When using this section for validation:

- assess the specification against each validation area
- note whether the specification is strong, adequate, weak, or missing in that area
- give specific rewrite guidance for any weak or missing area
- prefer practical improvement advice over generic criticism

Common failure patterns to watch for during validation include:

- describing the artifact too vaguely to be useful
- mixing purpose, design, execution, and acceptance without clear boundaries
- copying large amounts of content from related artifacts
- forcing detailed content into a summary document
- omitting ownership, review, or maintenance expectations where these matter
- making examples look mandatory when they are only illustrative
- creating artifacts that cannot be kept current in practice
- duplicating the full content of related governance documents
- requiring unnecessary detail for every initiative
- forcing one document to carry every type of information
- redefining roles or authority unnecessarily
- creating hidden mandatory work through vague wording
- encouraging documentation for its own sake

### 6.1 Purpose and usefulness

Check whether the specification clearly explains why the target artifact exists, what intended outcome it supports, and what useful work it is meant to support.

Signs the specification is strong:

- the purpose is easy to understand
- the intended outcome is easy to understand
- the intended use of the artifact is obvious
- the document explains what a useful finished artifact helps people do

If weak, improve it by:

- rewriting the purpose in plain language
- stating the intended outcome in plain language
- stating what problem the artifact solves
- explaining what decisions, work, review, handover, or acceptance the artifact should support

Common failure patterns in this area:

- the purpose is generic and could apply to almost any artifact
- the intended outcome is missing or implied only indirectly
- the purpose describes the document form but not its practical use
- the purpose does not help a drafter understand what a good finished artifact should achieve

### 6.2 Context and audience fit

Check whether the specification makes the intended audience and intended project context visible enough to guide drafting.

Signs the specification is strong:

- the main readers and users are named
- the kinds of initiatives or situations the artifact is meant for are clear
- the specification gives enough context to prevent generic output

If weak, improve it by:

- naming the intended readers and users more clearly
- adding the project or delivery context the artifact is meant to support
- stating what would make the artifact practically useful for that audience

Common failure patterns in this area:

- the specification does not say who the artifact is really for
- the context is so broad that the resulting artifact will likely be generic
- the intended audience is named, but their needs are not reflected in the specification

### 6.3 Content and boundary clarity

Check whether the specification clearly states what the artifact must contain and what should be kept out.

Signs the specification is strong:

- required content is explicit
- optional content is clearly distinguished
- the artifact boundary is clear
- the specification helps prevent overlap with nearby artifacts

If weak, improve it by:

- rewriting required content as clear content items or sections
- separating required content from optional content
- adding a `What to Keep Out` section with concrete exclusions
- clarifying where related detail should live instead

Common failure patterns in this area:

- required content is too vague
- optional content is mixed into required content
- the boundary is unclear, so the artifact risks becoming a catch-all document
- overlap with related artifacts is not controlled

### 6.4 Practical drafting guidance

Check whether a drafter could produce the artifact without major guessing.

Signs the specification is strong:

- the amount of detail is explained in plain language
- the content structure is easy to follow
- the document explains what a good section should achieve

If weak, improve it by:

- replacing abstract labels with practical detail guidance
- organizing content into meaningful sections or sub-sections
- explaining what each major section is for, not just what it is called

Common failure patterns in this area:

- the specification uses abstract labels instead of practical guidance
- the content structure is a flat list that gives little help to the drafter
- the specification says what sections exist but not what they are meant to achieve

### 6.5 Alignment and traceability

Check whether the specification explains how the artifact relates to other artifacts, ownership, review, and acceptance.

Signs the specification is strong:

- related upstream and downstream artifacts are identified
- ownership and review expectations are clear
- acceptance or approval expectations are clear where relevant
- the artifact's role in delivery, control, operations, or acceptance is understandable

If weak, improve it by:

- adding the key related artifacts
- naming who owns, reviews, or relies on the artifact
- clarifying whether the artifact supports approval, delivery, handover, operations, or acceptance

Common failure patterns in this area:

- ownership or review responsibility is unclear
- the artifact's place in the wider delivery model is vague
- the relationship to supporting or upstream artifacts is missing

### 6.6 Maintainability and lifecycle fit

Check whether the specification explains how the artifact should stay usable over time.

Signs the specification is strong:

- it is clear whether the artifact is static or living
- update triggers are named
- the risk of outdated content is visible where relevant

If weak, improve it by:

- stating whether the artifact should be maintained over time
- listing the kinds of changes that should trigger update or review
- explaining why stale content would create confusion, delivery risk, or operational risk

Common failure patterns in this area:

- the document sounds complete at one point in time but gives no update expectation
- change triggers are missing
- the consequences of outdated content are not visible

### 6.7 Prompt and AI drafting usability

Check whether the specification can be used directly by an AI agent to draft a useful artifact.

Signs the specification is strong:

- the prompt guide is specific enough to produce non-generic output
- required inputs are clear
- the prompts reinforce purpose, audience, and context
- validation prompts help improve a weak draft

If weak, improve it by:

- adding required inputs
- rewriting the starter prompt so it targets the real audience and use
- adding section prompts for difficult parts
- adding validation prompts that check specificity, boundary control, and practical usefulness

Common failure patterns in this area:

- the prompt is too generic and likely to produce generic output
- the prompt does not reinforce the intended audience or project context
- the prompt guide helps start drafting but not improve a weak draft

### 6.8 Validation outcome

After reviewing the specification, produce a short overall judgment using language such as:

- ready to use
- usable with minor revision
- needs revision before use
- not strong enough to guide drafting

Then give the most important improvement actions first.

A useful validation response should:

- identify the weakest areas
- explain why they matter
- suggest concrete rewrite actions
- help the next drafter improve the specification quickly

## 7. Recommended Prompt Questions for Drafting a Specification

Use these questions before writing a new specification:

1. What exact problem does this artifact solve?
2. When is the artifact needed?
3. Who will read it, use it, review it, or rely on it?
4. What project context or delivery situation is this artifact meant for?
5. What intended outcome should a good finished artifact help achieve, protect, confirm, or sustain?
6. What is the minimum information that must be in it?
7. What detail would overload the artifact and should go elsewhere?
8. What related artifacts already exist around it?
9. Does this artifact need named ownership, review, or acceptance?
10. Is this artifact expected to change over time?
11. How will someone know the artifact is complete and usable?

## 8. Recommended Prompt Template for Writing a New Specification

Use or adapt the following prompt when drafting a new specification:

> Write a specification for the [artifact name].
>
> The specification should explain:
>
> - why the artifact exists
> - what intended outcome the finished artifact should achieve or enable
> - when it is required or recommended
> - who uses or reads it
> - what project context or delivery situation it is meant for
> - how much detail belongs in it
> - the minimum required content and structure
> - what must not be included
> - how it relates to other artifacts
> - any ownership, review, update, or acceptance expectations
> - a short quality checklist
>
> Use plain language. Keep the specification practical and bounded. Make the intent and audience obvious enough that an LLM can use the specification to draft a useful artifact for a real project. Do not turn the artifact into a catch-all document.

## 9. Minimal Template for a Specification

Use this as a starting outline when writing a new deliverable, artifact, or document specification.

1. Document Identity (if needed)
2. Purpose and Intended Outcome
3. When It Is Required
4. Intended Readers and Users
5. Intended Project Context
6. How Much Detail to Include
7. Required Content or Minimum Structure
8. What to Keep Out
9. Relationships to Other Artifacts
10. Ownership, Review, and Acceptance Expectations
11. Maintenance Expectations
12. Quality Checklist
13. Prompt Guide for Drafting the Artifact

---

### Suggested Prompt Guide Format

Where a specification includes a Prompt Guide for Drafting the Artifact, the following pattern is recommended.

**Starter prompt**

> Draft a [artifact name] based on this specification.
> Use plain language.
> Include all required sections.
> Keep the amount of detail appropriate to the artifact's purpose.
> Make the intended outcome explicit so the draft is useful, not just complete.
> Make the draft fit the intended project context and intended audience.
> Do not add content that the specification says should be handled in other artifacts.

**Section drafting prompts**

Add short prompts for drafting major sections of the target artifact, especially where practitioners may need help starting.

Examples:

> Draft the Purpose and Intended Outcome section for this artifact in simple language.

> Draft the Required Content section for this artifact using the minimum structure defined in the specification.

> Draft this artifact so it is clear, bounded, and easy for reviewers to use.

**Validation prompts**

Add prompts that help review the draft against the specification.

Examples:

> Check whether this draft includes all required sections and content defined by the specification.

> Check whether this draft includes content that should be placed in another artifact instead.

> Check whether the amount of detail is appropriate for the artifact's intended use.

> Check whether the draft makes the intended outcome explicit and keeps each major section aligned to that outcome.

> Rewrite this draft to improve clarity, remove duplication, and keep the document within its defined boundary.

## Appendix A - Specification Self-Check

Use the questions below to review whether a specification is complete and usable.

### Purpose and boundary

1. Does the specification clearly explain why the target artifact exists?
2. Does it clearly explain what intended outcome the artifact should help achieve or enable?
3. Does it clearly state what should be kept out of the artifact?
4. Does it avoid overlapping unnecessarily with related artifacts?

### Usability

5. Could a practitioner draft the artifact from this specification without major guessing?
6. Is the required content stated clearly?
7. Are required, recommended, and optional elements clearly distinguished?
8. Is the intended project context clear enough to guide useful drafting?

### Proportion and clarity

9. Does the specification explain how much detail is needed in plain language?
10. Does it keep summary content separate from detailed supporting content?
11. Is the language plain enough for mixed audiences?

### Control and lifecycle

12. Does the specification explain how the artifact relates to other artifacts?
13. Does it define ownership, review, or acceptance expectations where needed?
14. Does it state whether the artifact is static or should be kept current over time?

### Quality

15. Would the resulting artifact be understandable, reviewable, and maintainable by someone other than the original author?
16. Would the resulting artifact support traceability, handover, and future review?
17. Does the specification avoid making the artifact broader or heavier than it needs to be?
18. Would an LLM using this specification likely produce an artifact that is practical for the intended project and audience rather than generic?
