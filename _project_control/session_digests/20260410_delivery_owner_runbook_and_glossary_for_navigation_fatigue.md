---
lorespec: "0.1"
id: "delivery-owner-runbook-and-glossary-for-navigation-fatigue"
date: "2026-04-10"
source: "codex"
topic: "Applied the plain-language template to core process docs and drafted a Delivery Owner Runbook and Glossary to reduce navigation fatigue"
tags: [work-delivery, framework-usability, readability, plain-language, runbook, glossary]
classification:
  type: "drafting"
  secondary_type: "operational"
  domains: [work_delivery, document_design, governance]
  value: "high"
trails: [framework-usability, work-delivery-framework-simplification]
---

## Session Arc

### Started
The session started with a request to apply the repository's plain-language document template to the Work Delivery Framework and validate whether navigation improves for Delivery Owners. Source: "Apply the plain-language template ... validate whether navigation improves" (Transcript L1-L1)

### Pivots
- The scope widened from the framework only to also apply the same quick-use structure to adjacent high-traffic process docs (Solution Design Process and Work Assessment Process). Source: "appl the plain language template ... then ... work_assessment_process.md" (Transcript L3-L3)
- The conversation then shifted from template application to the next highest-impact fatigue fix: create a single-page runbook (control dashboard) and a glossary to reduce re-orientation overhead and inconsistent terminology. Source: "aside from applying the plain language template ... next high impact change" (Transcript L4-L4) and "our action items are ... runbook ... Glossary" (Transcript L7-L7)

### Ended
The session ended with confirmation that the agreed action items are to make the Delivery Owner Runbook and create a Glossary document, and those drafts were created in the repo. Source: "to confirm our action items ... runbook ... Glossary" (Transcript L8-L8)

## ARTIFACT

### A1
- Artifact: Applied the plain-language template as a quick-use navigation layer to the Work Delivery Framework.
- Final state: `work_delivery/work_delivery_framework.md` now opens with plain-language orientation and navigation (purpose, start-here, quick navigation, required checks/approvals/evidence) while preserving detailed content deeper in the document.
- Evolution: The change focused on delivery-owner navigation and reducing mid-document drop-off by surfacing stage routing and non-negotiable controls early.
- Source: "Apply the plain-language template ... to work_delivery_framework.md" (Transcript L1-L1)

### A2
- Artifact: Applied the same plain-language quick-use layer to adjacent process docs.
- Final state: `work_delivery/solution_design_process.md` and `work_delivery/work_assessment/work_assessment_process.md` gained template-style openings, with the existing detailed guidance retained under "More Detail".
- Source: "appl the plain language template ... to solution_design_process.md then work_assessment_process.md" (Transcript L3-L3)

### A3
- Artifact: Delivery Owner Runbook draft.
- Final state: `work_delivery/delivery_owner_runbook.md` was created as a single-page dashboard-style guide for delivery owners (stage checklist, weekly rhythm, non-negotiables, evidence to keep, and primary links).
- Source: "Next high-impact change: create a separate, single-page 'Delivery Owner Runbook'" (Transcript L5-L5)

### A4
- Artifact: Glossary (Plain Language) draft.
- Final state: `work_delivery/glossary.md` was created to standardize day-to-day terminology and reduce re-orientation from near-synonyms.
- Source: "create a Glossary document" (Transcript L7-L7)

## DECISION

### D1
- Decision: Apply the plain-language template next to the Solution Design Process, then to the Work Assessment Process.
- Issue: Which document(s) should receive the next round of template-based navigation improvements.
- Positions: Apply next to `solution_design_process.md`; apply next to `work_assessment_process.md`; do one but not the other.
- Arguments: These are high-traffic operator docs where readers need stage-appropriate routing and quick access to "what to do now".
- Warrant: If fatigue is primarily re-orientation and mid-stream drop-off, prioritize the documents most frequently opened during active work.
- Qualifier: for delivery-owner usability within this repository
- Status: settled
- Source: "appl ... next to solution_design_process.md ... then ... work_assessment_process.md" (Transcript L3-L3)

### D2
- Decision: Next non-template fatigue fix is to create a Delivery Owner Runbook and a Glossary.
- Issue: What change has the highest impact on human fatigue after template-based restructuring.
- Positions: Create a single-page runbook + glossary; continue applying the template only; simplify the underlying governance model.
- Arguments: A runbook functions as a stable control dashboard that removes repeated scanning and document hunting; a glossary reduces cognitive churn from inconsistent terms.
- Warrant: If the fatigue driver is repeated re-orientation during delivery, a stable dashboard and consistent vocabulary reduce load more than further restructuring alone.
- Qualifier: without weakening governance controls
- Status: settled
- Source: "our action items are make the delivery owner runbook, and create a Glossary document" (Transcript L7-L7)

## INSIGHT

### I1
- Insight: After improving navigation openings, the next fatigue bottleneck is repeated re-orientation while work is in progress; a single-page runbook is a higher-leverage fix than further template application alone.
- Domain: document_design
- Confidence: medium
- Source: "aside from applying the plain language template, what would be the next high impact change" (Transcript L4-L4) and "Next high-impact change ... 'Delivery Owner Runbook'" (Transcript L5-L5)

### I2
- Insight: Some concept simplification is still needed, but it should be targeted at surface vocabulary and decision cues (not removing control gates).
- Domain: governance
- Confidence: medium
- Source: "Would we need to simplify some of the concepts as well?" (Transcript L6-L6)

## PATTERN

### P1
- Pattern: "Quick-use layer + deep reference + runbook dashboard" for governed delivery documentation.
- Scope: local
- Components:
  - Add a plain-language quick-use layer to high-traffic documents (purpose, start-here, quick navigation, what-to-do-now).
  - Keep the detailed governing content intact under "More Detail".
  - Provide a single-page Delivery Owner runbook as the day-to-day control dashboard.
  - Add a glossary to standardize vocabulary and reduce re-orientation.
- Why it matters: This combination targets the fatigue failure mode (starting correctly but getting lost midstream) without weakening required checks, approvals, evidence, or acceptance discipline.
- Source: "Apply the plain-language template ... validate whether navigation improves" (Transcript L1-L1) and "Next high-impact change ... runbook" (Transcript L5-L5)

## NEXT_STEP

### NS1
- What: Link the runbook and glossary into the core navigation surfaces so delivery owners consistently land on them (README and the "Start Here" sections of the framework and process docs).
- Prompted by: The runbook and glossary being created as new navigation artifacts.
- Urgency: soon
- Source: "Then: Add a prominent link to it from ... README ... framework ... process docs" (Transcript L5-L5)

## Connections

D1 --[led_to]--> A2
D2 --[led_to]--> A3
D2 --[led_to]--> A4
I1 --[informed_by]--> D2
P1 --[informed_by]--> D1
P1 --[informed_by]--> D2
A1 --[related_to]--> framework-readability-fatigue-and-plain-language-template:NS1
A1 --[related_to]--> framework-readability-fatigue-and-plain-language-template:P1
A1 --[related_to]--> work-delivery-framework-simplification-and-overlay:D1

## Trail Updates

- Extends `framework-usability` by applying the plain-language template pattern to additional high-traffic operator documents (solution design and work assessment), not only the framework.
- Extends `work-delivery-framework-simplification` by strengthening repeat-use operation (runbook + glossary) on top of the preserved 7-stage governance spine and 4-phase operating view.
- Creates a likely follow-on thread: wire the runbook/glossary into repository navigation so owners consistently land on the dashboard first, then drill down as needed.