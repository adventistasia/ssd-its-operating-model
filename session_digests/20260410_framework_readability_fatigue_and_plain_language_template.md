---
lorespec: "0.1"
id: "framework-readability-fatigue-and-plain-language-template"
date: "2026-04-10"
source: "codex"
topic: "Improved the work delivery framework reading experience by separating quick-use guidance from deeper reference material"
tags: [framework, readability, drafting, templates, work-delivery]
classification:
  type: "drafting"
  secondary_type: "operational"
  domains: [work_delivery, document_design, governance]
  value: "high"
trails: [framework-usability, work-delivery-framework-simplification]
---

## Session Arc

### Started
The session began with a reflective question about how a human reader might feel reading through the work delivery framework artifacts.

### Pivots
- The discussion shifted from emotional reaction to design diagnosis when the user asked what could reduce reader fatigue without defeating the framework's purpose.
- The diagnosis narrowed when the user identified the main failure mode as people starting but getting lost midway.
- The session became design-oriented when the user confirmed the main audience was delivery owners who work with artifacts regularly.
- The conversation moved from concept to implementation when the user asked for a lower-jargon naming set, then requested a reusable heading template and a saved file in the repo.

### Ended
The session landed on a plain-language document pattern, a reusable naming set, and a saved Markdown template intended to make regular use of framework artifacts easier without weakening governance.

## ARTIFACT

### A1
- Artifact: Plain-language reusable heading template for framework and specification documents.
- Final state: A Markdown template was created and saved at [templates/plain_language_document_template.md](../templates/plain_language_document_template.md). It organizes documents into practical sections such as `Purpose`, `Start Here`, `What To Do`, `What To Read Next`, and `More Detail`.
- Evolution: The artifact followed a design discussion that first established a naming set to reduce governance-heavy terminology before converting that naming set into a reusable structure.
- Source: "create this reusable heading template, then create a templates folder" (Transcript L10-L10)

## DECISION

### D1
- Decision: Optimize the framework for repeat-use readability by separating quick-use guidance from deeper reference material.
- Issue: Delivery owners start using the framework but get lost midway, even when they open the correct document.
- Positions: Keep the framework largely as-is; reduce fatigue through clearer navigation and plain-language layering; shorten the framework broadly.
- Arguments: The user identified that people "get lost midway" and that even the right document can feel "too dense to use." The resulting direction focused on improving handoffs, routing, and document openings rather than stripping out governance content.
- Warrant: If the main failure mode is mid-stream drop-off among regular operators, the most effective fix is better progressive disclosure and lower-friction document structure rather than raw content reduction.
- Qualifier: for this repository and audience
- Status: settled
- Source: "people starting but getting lost midway" (Transcript L3-L3); "when they do open the right document, it seems too dense" (Transcript L5-L5)

## INSIGHT

### I1
- Insight: For regular delivery owners, fatigue comes more from repeated re-orientation and dense mixed-purpose documents than from document length alone.
- Domain: document_design
- Confidence: high
- Source: "someone who owns delivery and works with artifacts regularly" (Transcript L7-L8)

### I2
- Insight: The right structural split is not simply "theory vs practice" but a plainer separation between why a document exists, what to do now, and where to go for exceptions or deeper detail.
- Domain: governance
- Confidence: high
- Source: "separating `control intent`, `operating instructions`, and `reference depth`" (Transcript L9-L9)

## PATTERN

### P1
- Pattern: Plain-language three-speed document pattern for governed delivery artifacts.
- Scope: local
- Components:
  - `Purpose`: explain why the document exists in plain language.
  - `Start Here` / `Use This When`: orient the reader quickly and prevent misuse.
  - `What You Need First` / `What To Do`: support day-to-day execution.
  - `Required Checks`, `Required Approvals`, `Evidence To Keep`: preserve the necessary control points without burying them in explanation.
  - `If This Is Not Straightforward` / `More Detail`: isolate edge cases and fuller rationale so they remain available without overwhelming routine use.
- Why it matters: This pattern preserves governance value while reducing cognitive load for repeat users who need to act quickly and accurately.
- Source: "A simple three-part pattern could be: `Purpose` ... `More detail`" (Transcript L9-L9); "Recommended Naming Set" (Transcript L11-L11)

## NEXT_STEP

### NS1
- What: Apply the plain-language template to one high-friction framework document, starting with the work delivery framework, and validate whether navigation improves for delivery owners.
- Prompted by: The creation of the reusable template and the diagnosis that users get lost midway.
- Urgency: soon
- Source: "the next sensible step is to apply this pattern" (Transcript L10-L10)

## Connections

D1 --[led_to]--> P1
D1 --[led_to]--> A1
I1 --[informed_by]--> D1
I2 --[informed_by]--> P1
A1 --[led_to]--> NS1
D1 --[related_to]--> work-delivery-framework-simplification-and-overlay:D1
P1 --[related_to]--> work-delivery-framework-simplification-and-overlay:P1

## Trail Updates

- Creates trail `framework-usability` for work focused on improving the usability of governed documentation without weakening required checks.
- Extends [20260410_work_delivery_framework_simplification_and_overlay.md](../session_digests/20260410_work_delivery_framework_simplification_and_overlay.md) by adding a readability and repeat-use layer on top of the earlier 4-phase operating overlay decision.
- This session established a reusable naming set and a concrete template artifact that later framework revisions can instance.
