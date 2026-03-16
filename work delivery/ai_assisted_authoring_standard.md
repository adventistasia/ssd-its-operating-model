# AI-Assisted Authoring Standard

## 1. Purpose

Define the default prompting, review, and revision protocol for AI-assisted deliverable drafting across the repository.

## 2. Standard Prompt Order

Use this order in prompts:

1. objective and artifact type
2. stage and required depth
3. in-scope and out-of-scope boundaries
4. required IDs, references, and source context
5. required structure/specification
6. review and acceptance criteria

## 3. Standard Review Loop

1. reviewer comments on gaps and required changes
2. revision request states what must change and what must not change
3. AI revises
4. AI provides concise change summary
5. owner confirms accepted / revise again / escalate

## 4. Mandatory Guardrails

- AI must not authorize, accept, or close governed work.
- AI must not expand authorized scope without explicit instruction.
- AI must not invent evidence or completion status.
- Stable IDs and references must be preserved through revisions.

## 5. Required Inputs Before Controlled Drafting

- stage context
- scope boundary
- owner/reviewer
- intended decision or acceptance use
- applicable specification or required structure

If missing, output should be labeled **working draft** and treated as non-authoritative.
