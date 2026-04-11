---
lorespec: "0.1"
id: "2026041105"
date: "2026-04-11"
source: "codex"
topic: "Work Delivery Framework A02 resolved as a markdown-first operating model"
tags: [work-delivery-framework, ambiguity-resolution, operating-model, markdown-first, ai-agents, documentation]
classification:
  type: "operational"
  secondary_type: "framework-design"
  domains: [work_delivery_framework, documentation_governance, ai_agent_consumability]
  value: "high"
trails: [work-delivery-framework, ambiguity-resolution, specification-quality]
---

## Session Arc

### Started
The session resumed in the Work Delivery Framework ambiguity-resolution sequence after A01 had already been closed. The active item was A02, which asked what the framework actually is as a deliverable: policy, playbook, template set, workflow, knowledge base, or operating model. The user then clarified that the desired result is not advisory prose but a structured system that defines the operating model, workflow stages, artifact definitions, stage gates, blocker handling, and AI-consumable structure.

### Pivots
- The first pivot was from format choice to operating-model identity. The user's clarification made it explicit that the framework must control how work enters, moves, and stops, not merely explain best practices. (Transcript L4-L4)
- The second pivot was from a general structured artifact to a canonical publication model. When asked to choose the source-of-truth pattern, the user selected "markdown first," which settled the document architecture. (Transcript L7-L7)
- The final pivot was from decision-making to implementation state. The user confirmed that the plan was approved and that both the spec and the resolution plan had been updated, which closed the loop on A02 and left A03 as the next unresolved item. (Transcript L9-L9)

### Ended
The session ended with A02 resolved as a markdown-first operating model. The framework spec now carries the canonical operating-model definition, and the resolution plan marks A02 resolved while advancing the workflow to the next ambiguity, A03 governance and decision rights.

## ARTIFACT

### A1
- Artifact: `work_delivery_framework/work_delivery_framework_specification.md`
- Final state: Updated to define the framework as a full operating model for work definition and delivery readiness, and to declare the document itself as the canonical source of truth.
- Evolution: The document now requires machine-consumable YAML blocks for stages, artifacts, and gates, with stable IDs so AI agents can extract and apply the framework consistently.
- Source: "This framework is a full operating model" (Transcript L4-L4); "markdown first" (Transcript L7-L7); "spec and resolution plan was updated" (Transcript L9-L9)
- Why it matters: This removes the ambiguity around whether the framework is guidance or an enforceable system, and it gives the document a stable human-readable plus machine-readable form.

### A2
- Artifact: `work_delivery_framework/resolution_plan_work_delivery_framework_specification.md`
- Final state: Updated to mark A02 as resolved and to move the active sequencing position forward to A03.
- Evolution: The resolution plan now records the settled framework-form decision and preserves the ambiguity-first workflow that governs the remaining items.
- Source: "markdown first" (Transcript L7-L7); "spec and resolution plan was updated" (Transcript L9-L9)
- Why it matters: The plan stays aligned with the spec and continues to serve as the ordering mechanism for the remaining ambiguity work.

### A3
- Artifact: `session_digests/2026041105_work_delivery_framework_a02_resolved_as_a_markdown_first_operating_model.md`
- Final state: Created as the LoreSpec session digest for the A02 resolution session.
- Source: This extraction work and the current approved state reported by the user. (Transcript L9-L9)
- Why it matters: It preserves the decision trail and makes the resolved operating-model choice searchable later without relying on chat history.

## DECISION

### D1
- Decision: The Work Delivery Framework is a full operating model for work definition and delivery readiness, and its canonical publication model is Markdown-first with embedded machine-consumable YAML blocks.
- Issue: Whether the framework should be treated as guidance, a playbook, a template library, or an enforceable operating model with structured publication semantics.
- Positions:
  - Publish it as a loose guidance artifact or playbook.
  - Publish it as a full operating model with workflow stages, stage gates, artifact definitions, and AI-readable structure. (Chosen)
- Arguments:
  - The user explicitly required the framework to define request entry, stage sequence, required outputs, completeness, blocker handling, and AI-agent consumability. (Transcript L4-L4)
  - Markdown-first preserves readability for humans while still allowing stable extraction by machines when the document embeds structured YAML definitions. (Transcript L7-L7)
  - A single canonical spec prevents parallel "shadow" descriptions from drifting apart during iterative ambiguity resolution. (Transcript L8-L9)
- Warrant: If the framework must be both enforceable and AI-consumable, it needs a single authoritative document with stable structure rather than a loose collection of guidance texts.
- Qualifier: This settles framework form and publication model only; governance, stage definitions, and artifact inventories remain to be finalized in later ambiguities.
- Status: settled

## INSIGHT

### I1
- Insight: Markdown can serve as the canonical source of truth without sacrificing machine consumability if the framework embeds stable, fenced YAML objects for stages, artifacts, and gates.
- Domain: documentation-governance
- Confidence: high
- Source: "markdown first" (Transcript L7-L7); the assistant's proposed YAML-embedded model (Transcript L8-L8)

### I2
- Insight: The user's description of the framework as a "full operating model" turns the publication question into a control-system question, not a style preference.
- Domain: framework-design
- Confidence: high
- Source: "This framework is a full operating model" (Transcript L4-L4)

## PATTERN

### P1
- Pattern: Markdown-first operating model with structured YAML embeds.
- Scope: local
- Components:
  - Make one Markdown document the canonical source.
  - Encode stages, artifacts, and gates as fenced YAML objects with stable IDs.
  - Keep prose and structure in the same file so humans and AI agents read the same authority.
  - Treat the YAML blocks as extraction targets, not as a separate hidden system of record.
- When to use: When a framework must remain human-readable while also being precise enough for automated or AI-assisted interpretation.
- Source: "full operating model" (Transcript L4-L4) and "markdown first" (Transcript L7-L7)

## NEXT_STEP

### NS1
- What: Resolve A03, the governance, ownership, and decision-rights ambiguity.
- Why: The framework's form is now fixed, so the next unresolved question is who owns it, who enforces it, and who can stop work.
- Urgency: soon
- Source: The updated resolution sequence and the user's confirmation that the plan was approved and updated. (Transcript L9-L9)

## Connections

D1 --[led_to]--> A1
D1 --[led_to]--> A2
D1 --[led_to]--> NS1
P1 --[related_to]--> D1

## Trail Updates

- Extends `work-delivery-framework`.
- Extends `ambiguity-resolution`.
- Links to the prior scope-resolution digest `2026041104_work_delivery_framework_a01_scope_boundary.md` as the immediate predecessor in the same resolution sequence.
