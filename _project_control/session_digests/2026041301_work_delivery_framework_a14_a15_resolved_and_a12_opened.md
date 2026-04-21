---
lorespec: "0.1"
id: "2026041301"
date: "2026-04-13"
source: "codex"
topic: "Resolved A14 and A15 for the work delivery framework and advanced the ambiguity sequence to A12"
tags: [work-delivery-framework, ambiguity-resolution, governance, ai-readiness, lore]
classification:
  type: "drafting"
  secondary_type: "operational"
  domains: [framework-design, delivery-readiness, ai-consumability]
  value: "high"
trails: [work-delivery-framework]
---

## Session Arc

### Started
The session began with a request to continue the ambiguity-resolution sequence for `work_delivery_framework/work_delivery_framework_specification.md`, following the registered order in the resolution plan and updating both the specification and the plan after each resolved ambiguity.

### Pivots
- The first major pivot was from orientation into a structured interview focused on A14, where the discussion converged on replacing a RAID-style optional artifact with a mandatory single Open Items Register using typed entries. Source: "Let's go with Option 3 from question 1. Our organization will adjust." (Transcript L7-L7)
- The second pivot clarified that blockers should be a first-class type, not a status overlay, and that gate-disqualifying non-blockers must become blockers. Source: "2" and "yes" in response to blocker classification and reclassification questions. (Transcript L8-L8, L11-L11)
- The third pivot resolved A15 by adopting a human-plus AI-sufficiency standard integrated into completeness rather than creating a separate control track. Source: "2" and "yes" on checklist and completeness integration. (Transcript L24-L24, L27-L27)
- The fourth pivot tightened A15 into a strong traceability model by requiring stable local identifiers, numbered normative structure by default, explicit actor/action/object wording, controlled placeholders, and explicit labeling of AI-sufficiency failures. Source: "Let's go with 2. It would also make sense to number headings, sections, sub-sections, and lists by default..." and "yes but the framework should explicitly show that it failed AI-sufficiency check." (Transcript L35-L35, L43-L43)

### Ended
The session ended after A14 and A15 were written into the specification, marked resolved in the resolution plan, and the next ambiguity was advanced to A12 (external engagement modes and handoff variants). A new request then redirected the work to producing this session digest.

## ARTIFACT

### A1
- Artifact: Updated `work_delivery_framework/work_delivery_framework_specification.md` to add a mandatory Open Items Register model for A14 and a new AI-agent sufficiency standard for A15, and updated `work_delivery_framework/resolution_plan_work_delivery_framework_specification.md` to mark both ambiguities resolved and advance the sequence.
- Final state: The specification now contains:
  1. a canonical Open Items Register artifact with typed entries and status rules
  2. a resolved A14 section defining blocker handling, escalation, closure authority, and Decision Log boundaries
  3. a resolved A15 section defining a human-plus AI-sufficiency checklist, immediate-fail patterns, numbering/traceability rules, and explicit AI-sufficiency failure reporting
- Evolution: The session first replaced the earlier optional RAID-oriented model conceptually, then integrated A14 into artifact taxonomy and completeness, then added a dedicated A15 section and completeness hooks for AI sufficiency.
- Source: "I’m updating the specification to define the Open Items Register..." and "I’m updating the spec to make AI sufficiency a mandatory completeness sub-dimension..." (Transcript L20-L20, L44-L44)

## DECISION

### D1
- Decision: Resolve A14 by mandating a single Open Items Register for every initiative, using typed entries `blocker`, `risk`, `issue`, `assumption`, and `dependency`.
- Issue: Whether unresolved blockers, risks, issues, assumptions, and dependencies should continue to follow a RAID-style model or be standardized into one canonical control mechanism.
- Positions:
  1. Keep a RAID-style model with blocker as status
  2. Use a single canonical register with typed entries
- Arguments: One canonical register gives clearer gate logic, stronger AI parsing, and less local interpretation, while still allowing origin semantics and escalation traceability.
- Warrant: If the framework is meant to be enforceable and AI-usable, unresolved items must live in one authoritative, structured register rather than in optional or locally variable tracking patterns.
- Qualifier: for this framework operating model
- Status: settled
- Source: "Let's go with Option 3 from question 1. Our organization will adjust." (Transcript L7-L7)

### D2
- Decision: Treat `blocker` as a first-class type, require gate-disqualifying non-blockers to be reclassified or recorded as blockers, and require blocker entries to reference their originating item.
- Issue: Whether blocking conditions should be represented as a status overlay or as a distinct item class with explicit gate-stop semantics.
- Positions:
  1. Blocker as status/flag on another type
  2. Blocker as its own type with origin reference
- Arguments: A first-class blocker makes gate failure explicit, reduces ambiguity at review time, and preserves traceability when coupled with an origin reference.
- Warrant: If something stops progression, the register should make that visible as a direct object of control rather than expecting reviewers to infer it from another item's status.
- Qualifier: within the Open Items Register model
- Status: settled
- Source: "2" and "yes reference it" in response to blocker modeling questions. (Transcript L8-L8, L12-L12)

### D3
- Decision: Resolve A15 by adopting a human-plus AI-sufficiency standard integrated into completeness for all required artifacts and gates.
- Issue: What additional standard is required for outputs to be genuinely usable by AI agents without making the framework AI-first or purely advisory.
- Positions:
  1. Human-equivalent
  2. Human-plus
  3. AI-first
- Arguments: Human-plus preserves human readability while requiring extra explicitness, traceability, structure, and anti-ambiguity rules where AI agents are more fragile than humans.
- Warrant: If the framework claims outputs are usable by AI agents, AI sufficiency must be a real completeness property rather than a side note or formatting preference.
- Qualifier: as the baseline for all required artifacts and gates
- Status: settled
- Source: "2" and "yes" on checklist-based, completeness-integrated AI sufficiency. (Transcript L24-L24, L26-L27)

### D4
- Decision: AI-sufficiency failures must explicitly appear in review output as AI-sufficiency failures, not just generic completeness defects.
- Issue: Whether AI-sufficiency problems should be silent subcriteria under completeness or visible named failure modes.
- Positions:
  1. Fail completeness silently under general review comments
  2. Fail completeness and label the failure explicitly as AI-sufficiency
- Arguments: Explicit labeling improves auditability, preserves the meaning of the AI-ready claim, and helps teams distinguish human-readability issues from AI-consumption issues.
- Warrant: If AI sufficiency matters enough to fail a gate, the reason for failure should be visible as a named control outcome.
- Qualifier: whenever one or more mandatory AI-sufficiency checks fail
- Status: settled
- Source: "yes but the framework should explicitly show that it failed AI-sufficiency check." (Transcript L43-L43)

## INSIGHT

### I1
- Insight: The user's organization can tolerate changing established RAID practice if the replacement improves canonicality, enforceability, and AI-compatibility.
- Domain: framework-design
- Confidence: high
- Source: "Let's go with Option 3 from question 1. Our organization will adjust." (Transcript L7-L7)

### I2
- Insight: For this framework, numbered headings, sections, subsections, and lists are not just presentation preferences; they are traceability mechanisms for both humans and AI agents.
- Domain: ai-consumability
- Confidence: high
- Source: "It would also make sense to number headings, sections, sub-sections, and lists by default..." (Transcript L35-L35)

## PATTERN

### P1
- Pattern: Ambiguity-first framework refinement through sequenced single-question interviews.
- Scope: local
- Components:
  1. read the current spec and registered resolution plan
  2. take the next ambiguity in the stated sequence
  3. explain what the ambiguity is about and why it matters
  4. present options with pros, cons, and a recommendation
  5. ask exactly one narrowing question at a time
  6. synthesize only after confidence is high
  7. update both the specification and the resolution plan together
- Why it matters: This pattern prevents premature drafting and forces operational precision before text is changed.
- Source: "work with me to resolve ambiguities one by one... follow the proposed sequence. interview me until you are 95% confident..." (Transcript L1-L1)

## OPEN_QUESTION

### OQ1
- Question: How should external engagement modes and handoff variants (A12) be modeled in the framework?
- What remains unresolved: Whether the framework should define a small set of canonical external engagement modes and, if so, how those modes should change handoff and governance requirements.
- What blocks: The next ambiguity in the registered sequence has been opened but not yet interviewed through to resolution.
- Partial progress: The next question was asked and a recommendation was made to define a small set of canonical external engagement modes, but no user answer was captured before the session redirected to digest creation.
- Source: "A12 focus: external engagement modes and handoff variants..." and "Question 1 for A12..." (Transcript L23-L23)

## NEXT_STEP

### NS1
- What: Resume the ambiguity-resolution sequence at A12 and continue the one-question-at-a-time interview from the first external-engagement-mode question.
- Prompted by: A14 and A15 were resolved and the resolution plan now advances to A12.
- Urgency: soon
- Source: "The next active ambiguity is now A12." (Transcript L46-L46)

## Connections

D1 --[led_to]--> A1
D2 --[informed_by]--> D1
D2 --[led_to]--> A1
D3 --[led_to]--> A1
D4 --[depends_on]--> D3
D4 --[led_to]--> A1
I1 --[informed_by]--> D1
I2 --[informed_by]--> D3
P1 --[led_to]--> D1
P1 --[led_to]--> D3
A1 --[led_to]--> NS1
OQ1 --[related_to]--> NS1

## Trail Updates

- Extends the `work-delivery-framework` trail.
- Continues the ambiguity-resolution run captured in prior digests, especially [2026041206_work_delivery_framework_a13_review_assurance_audit_resolved.md](</home/rmicua/projects/ssd-its-operating-model/session_digests/2026041206_work_delivery_framework_a13_review_assurance_audit_resolved.md>) and [2026041102_work_delivery_framework_ambiguity_resolution_plan.md](</home/rmicua/projects/ssd-its-operating-model/session_digests/2026041102_work_delivery_framework_ambiguity_resolution_plan.md>).
- Adds new settled objects for A14 and A15 and carries forward A12 as the next open question in sequence.
