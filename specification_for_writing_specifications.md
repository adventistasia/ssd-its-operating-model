# Specification for Writing Deliverable, Artifact, and Document Specifications

## 1. Purpose

This specification defines how to write clear, useful, and governable specifications for deliverables, artifacts, and documents.

It exists to ensure that specifications:

- clearly explain what an artifact is for
- define the minimum content and expectations for that artifact
- show how the artifact supports delivery, control, operations, or acceptance
- remain readable and practical for real project use
- reduce ambiguity, rework, and document sprawl

This is a guide for writing specifications. It does not itself define every artifact used in an initiative.

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

## 3. Intended Outcome

A good specification should make the target artifact easy to understand, easy to produce, and easy to review.

After reading a good specification, a practitioner should be able to answer:

- What is this artifact for?
- When is it needed?
- What must it contain?
- What should not be placed in it?
- How detailed should it be?
- Who uses it?
- How does it support delivery, control, operations, or acceptance?

## 4. Core Writing Principles

All specifications written using this guide should follow these principles.

### 4.1 Purpose before detail

Start by explaining why the artifact exists before describing its sections.

A specification should first answer:

- what problem the artifact solves
- what control, delivery, or operational need it serves
- why the artifact matters

### 4.2 Clear governance boundary

A specification must state what the artifact does and does not do.

This prevents overlap between artifacts and reduces confusion.

Examples:

- a specification may define approval-level content but not execution task planning
- a specification may define behavioral requirements but not technical architecture
- a specification may define acceptance evidence needs but not replace formal sign-off

### 4.3 Practical minimums

A specification should define the minimum content needed for the artifact to be useful and governable.

Do not overload the specification with optional detail unless that detail is necessary for clarity, control, risk reduction, or acceptance.

### 4.4 Plain language

Specifications should use simple language wherever possible.

They should be understandable by:

- business owners
- delivery staff
- reviewers
- future maintainers
- audit or oversight readers

Use technical terms only when they are necessary and define them when helpful.

### 4.5 Separation of summary and detail

A specification should help keep the target artifact readable.

If detailed material would make the target artifact hard to use, the specification should direct that detail into a separate supporting artifact and require a reference or link instead.

### 4.6 Traceability and control

A specification should make it possible to trace:

- what the artifact is supposed to define
- how it relates to other artifacts
- who owns or accepts it
- what role it plays in decision-making, delivery, operations, or acceptance

### 4.7 Supportability over authorship

A specification should encourage artifacts that others can understand, maintain, review, and use.

The artifact should not depend on the memory of the original author.

## 5. What a Specification Must Do

A good specification must:

- define the artifact’s purpose
- define when the artifact is required or recommended
- identify the intended readers and users
- define the right level of detail
- describe the minimum required content or structure
- clarify what does not belong in the artifact
- explain how the artifact relates to other artifacts
- define any important control, traceability, review, or acceptance expectations
- support consistency across initiatives

## 6. What a Specification Must Not Do

A good specification must not:

- duplicate the full content of related governance documents
- blur the boundary between authorization, design, execution, and acceptance
- require unnecessary detail for every initiative
- force one document to carry every type of information
- redefine roles or authority already defined elsewhere unless the specification’s purpose is to do so
- create hidden mandatory work through vague wording
- encourage documentation for its own sake

## 7. Recommended Structure for a Specification

The sections below are the recommended default structure for writing a specification for a deliverable, artifact, or document.

Not every specification needs every section, but any section removed should be a conscious decision.

### 7.1 Purpose

State why the artifact exists and what need it serves.

This section should make the artifact understandable in plain language.

### 7.2 Governance Position or Boundary

State where the artifact fits in the overall delivery and control model.

Clarify:

- what this artifact supports
- what it does not replace
- what it must align with
- what decisions or controls remain outside it

### 7.3 When It Is Required

State when the artifact is:

- required
- conditionally required
- recommended
- optional

Where helpful, describe the kinds of initiatives or risk conditions that make the artifact necessary.

### 7.4 Intended Readers and Users

Identify who needs to read, use, review, maintain, approve, or rely on the artifact.

This helps define tone, content depth, and structure.

### 7.5 Intended Outcome or Use

Explain what the artifact should enable once completed.

Examples:

- clearer approval decisions
- better scope control
- clearer design handoff
- stronger operational readiness
- more defensible acceptance decisions

### 7.6 Level of Detail

Define how much detail belongs in the artifact.

This section should prevent two common failures:

- artifacts that are too vague to be useful
- artifacts that become overloaded with implementation detail

Where appropriate, include guidance such as:

- approval-level detail
- design-level detail
- execution-level detail
- operational summary only

### 7.7 Required Content or Minimum Structure

List the sections, content elements, or information categories the artifact must contain.

Use direct wording such as:

- Must include
- Should include
- May include
- Must not include

This is the main control section of the specification.

### 7.8 Content Boundary

Explain what should be kept out of the artifact.

This is especially important when nearby artifacts could easily overlap.

Examples:

- detailed test scripts belong elsewhere
- runbooks belong elsewhere
- task plans belong elsewhere
- build configuration belongs elsewhere

### 7.9 Relationships to Other Artifacts

Explain how this artifact connects to upstream and downstream artifacts.

Examples:

- what should exist before this artifact is written
- what artifacts this one informs
- what it should reference instead of repeating
- how it supports evidence, acceptance, or operations

### 7.10 Ownership, Review, and Acceptance Expectations

Where relevant, identify:

- who usually owns creation of the artifact
- who reviews it
- who relies on it
- whether it has a named Acceptance Authority or approval need

Not every specification needs formal acceptance rules, but governance-relevant artifacts usually need clear review expectations.

### 7.11 Maintenance Expectations

If the artifact is expected to change over time, the specification should state:

- whether it is a living document
- what should be kept current
- when it should be updated
- when a new version is needed

### 7.12 Quality Checklist

Include a short self-check to test whether the artifact is complete, usable, and aligned with its intended purpose.

### 7.13 Prompt Guide for Drafting the Artifact

Where useful, include a short prompt guide that helps practitioners draft the target artifact from the specification.

This section should not replace the specification itself. It should translate the specification into practical drafting prompts.

The prompt guide may include:

- a starter prompt for drafting the first version of the artifact
- prompts for drafting individual sections
- prompts for checking completeness, clarity, and alignment
- prompts for improving readability and removing overlap with related artifacts

The prompt guide should be practical, simple, and consistent with the content boundary defined by the specification.

## 8. Recommended Writing Pattern

When drafting a specification, write in the following order:

1. Define the purpose of the target artifact.
2. Define its governance boundary.
3. Define when it is required.
4. Define who uses it.
5. Define the correct level of detail.
6. Define the minimum content.
7. Define what does not belong in it.
8. Define how it relates to other artifacts.
9. Define any maintenance, review, or acceptance expectations.
10. Add a short quality checklist.
11. Add a prompt guide that helps practitioners draft the target artifact from the specification.

This order usually produces clearer specifications than starting with section headings only.

## 9. Writing Rules for Good Specifications

### 9.1 Write for decisions and action

A specification should help people create a useful artifact, not just describe an ideal document.

### 9.2 Prefer minimum enforceable clarity

Say what must be present, but avoid unnecessary prescription where professional judgment is acceptable.

### 9.3 Use stable headings where consistency matters

Where multiple initiatives will use the same kind of artifact, stable section names improve reuse, review, and training.

### 9.4 Distinguish mandatory from optional

Use consistent wording so readers can tell the difference between:

- required content
- recommended content
- optional additions

### 9.5 Avoid hidden scope expansion

Do not quietly introduce new deliverables, approval gates, or responsibilities through supporting notes or examples.

If the specification adds a real obligation, state it clearly.

### 9.6 Avoid role ambiguity

If the artifact depends on ownership, review, acceptance, or update responsibility, say so clearly.

### 9.7 Keep examples illustrative, not controlling

Examples should help understanding, but they should not accidentally become mandatory unless stated as a rule.

## 10. Default Content Pattern for Most Specifications

For most deliverable, artifact, or document specifications, the following pattern is recommended.

### 10.1 Document Identity

May include:

- specification title
- version
- status
- last updated date
- owner

### 10.2 Purpose

Explain why the target artifact exists.

### 10.3 Governance Boundary

Explain what the target artifact does and does not do.

### 10.4 Applicability

Explain when the target artifact is required, recommended, or optional.

### 10.5 Intended Readers

Explain who will use, review, or rely on the artifact.

### 10.6 Required Content

Define the minimum content or section structure.

### 10.7 Excluded Content

Define what should be documented elsewhere.

### 10.8 Related Artifacts

Show the main upstream, downstream, or companion artifacts.

### 10.9 Review and Acceptance Expectations

State who normally reviews, approves, or accepts the artifact if relevant.

### 10.10 Maintenance Expectations

State whether the target artifact is static or living.

### 10.11 Quality Check

Provide a short checklist for completeness and usability.

### 10.12 Prompt Guide for Drafting the Artifact

Provide practical prompts that help a practitioner draft the target artifact using the specification.

This may include:

- a full-document drafting prompt
- section-by-section prompts
- review prompts for completeness, clarity, and boundary control

## 11. Specification Quality Criteria

A specification is considered strong when it is:

### 11.1 Clear

A reader can easily understand the artifact’s purpose and required content.

### 11.2 Bounded

The specification clearly states what belongs in the artifact and what does not.

### 11.3 Usable

A practitioner can draft the artifact without guessing what the document is supposed to do.

### 11.4 Aligned

The artifact’s role is consistent with surrounding governance, delivery, and acceptance controls.

### 11.5 Proportionate

The level of detail matches the need, risk, and lifecycle stage.

### 11.6 Maintainable

The artifact can be updated and understood over time.

### 11.7 Auditable

The artifact’s purpose, ownership, and use in decision-making or acceptance can be explained later.

## 12. Common Failure Patterns to Avoid

Do not write specifications that:

- describe the artifact too vaguely to be useful
- mix purpose, design, execution, and acceptance without clear boundaries
- copy large amounts of content from related artifacts
- force detailed content into a summary document
- omit ownership, review, or maintenance expectations where these matter
- make examples look like mandatory sections without saying so
- create artifacts that cannot be kept current in practice

## 13. Recommended Prompt Questions for Drafting a Specification

Use these questions before writing a new specification:

1. What exact problem does this artifact solve?
2. What decision, control, delivery, or operational need does it support?
3. At what stage is the artifact needed?
4. Who will read it, use it, review it, or rely on it?
5. What is the minimum information that must be in it?
6. What detail would overload the artifact and should go elsewhere?
7. What related artifacts already exist around it?
8. Does this artifact need named ownership, review, or acceptance?
9. Is this artifact expected to change over time?
10. How will someone know the artifact is complete and usable?

## 14. Recommended Prompt Template for Writing a New Specification

Use or adapt the following prompt when drafting a new specification:

> Write a specification for the [artifact name].
>
> The specification should explain:
>
> - the purpose of the artifact
> - where it fits in the delivery and governance model
> - when it is required or recommended
> - who uses or reads it
> - the correct level of detail
> - the minimum required content and structure
> - what must not be included
> - how it relates to other artifacts
> - any ownership, review, update, or acceptance expectations
> - a short quality checklist
>
> Use plain language. Keep the specification practical and bounded. Do not turn the artifact into a catch-all document.

## 15. Minimal Template for a Specification

Use this as a starting outline when writing a new deliverable, artifact, or document specification.

1. Purpose
2. Governance Position / Boundary
3. When Required
4. Intended Readers and Users
5. Intended Outcome or Use
6. Level of Detail
7. Required Content / Minimum Structure
8. Content Boundary
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
> Keep the level of detail appropriate to the artifact’s purpose.
> Do not add content that the specification says should be handled in other artifacts.

**Section drafting prompts**

Add short prompts for drafting major sections of the target artifact, especially where practitioners may need help starting.

Examples:

> Draft the Purpose section for this artifact in simple language.

> Draft the Required Content section for this artifact using the minimum structure defined in the specification.

> Draft this artifact so it is clear, bounded, and easy for reviewers to use.

**Validation prompts**

Add prompts that help review the draft against the specification.

Examples:

> Check whether this draft includes all required sections and content defined by the specification.

> Check whether this draft includes content that should be placed in another artifact instead.

> Check whether the level of detail is appropriate for the artifact’s intended use.

> Rewrite this draft to improve clarity, remove duplication, and keep the document within its defined boundary.

## Appendix A — Specification Self-Check

Use the questions below to review whether a specification is complete and usable.

### Purpose and boundary

1. Does the specification clearly explain why the target artifact exists?
2. Does it clearly state what the artifact does not do?
3. Does it avoid overlapping unnecessarily with related artifacts?

### Usability

4. Could a practitioner draft the artifact from this specification without major guessing?
5. Is the required content stated clearly?
6. Are required, recommended, and optional elements clearly distinguished?

### Proportion and clarity

7. Does the specification define the right level of detail?
8. Does it keep summary content separate from detailed supporting content?
9. Is the language plain enough for mixed audiences?

### Control and lifecycle

10. Does the specification explain how the artifact relates to other artifacts?
11. Does it define ownership, review, or acceptance expectations where needed?
12. Does it state whether the artifact is static or should be kept current over time?

### Quality

13. Would the resulting artifact be understandable, reviewable, and maintainable by someone other than the original author?
14. Would the resulting artifact support traceability, handover, and future review?
15. Does the specification avoid making the artifact broader or heavier than it needs to be?

