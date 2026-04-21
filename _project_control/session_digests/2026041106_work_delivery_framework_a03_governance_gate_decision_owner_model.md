---
lorespec: "0.1"
id: "2026041106"
date: "2026-04-11"
source: "codex"
topic: "A03 governance resolved: PMO owns the framework and every gate requires a named Gate Decision Owner"
tags: [work_delivery_framework, governance, pmo, gate, decision_rights]
classification:
  type: "operational"
  secondary_type: "drafting"
  domains: [work-delivery, governance, documentation]
  value: "high"
trails: [work-delivery-framework]
---

## Session Arc

### Started
The session started with a process for resolving specification ambiguities one item at a time, beginning with the next unresolved item in the resolution plan. ("determine which ambiguity item is currently active" (Transcript L2-L2))

### Pivots
- The session pivoted from interviewing to a stop request: the user asked for a report and to end the sub-agent session before completing the full A03 interview. ("give a resolution report then end session" (Transcript L9-L9))
- The user then requested a repo-based review of the latest specification and resolution plan updates, shifting from intent-capture to evidence-based reporting. ("review the latest changes to the specification and resolution" (Transcript L11-L11))

### Ended
The session ended with an updated report reflecting that A03 was committed as resolved in the repository, plus a noted inconsistency in the resolution plan progress summary. ("A03 is now checked off" (Transcript L12-L12))

## ARTIFACT

### A1
- Artifact: Updated framework specification and resolution plan reflecting A03 governance resolution.
- What changed (as observed in-session):
  - The specification now states: PMO owns the framework; each gate must have a single named Gate Decision Owner; assignment/recording requirements; and default decision owner roles by gate. ("§6.7 ... now contains a concrete governance model" (Transcript L12-L12))
  - The resolution plan now marks A03 as checked/resolved and advances the “next active ambiguity” to A04. ("Tracking note now says the next active ambiguity is A04" (Transcript L12-L12))
- Where: `work_delivery_framework/work_delivery_framework_specification.md` and `work_delivery_framework/resolution_plan_work_delivery_framework_specification.md`. ("latest commit message suggests governance was marked resolved" (Transcript L11-L11))

## DECISION

### D1
- Decision: Treat A03 as resolved in the spec by defining PMO ownership and per-gate decision accountability via a named Gate Decision Owner model.
- Issue: A03 was ambiguous because governance/authority for stop/go decisions and framework ownership were underdefined. ("A03 — Governance, ownership, and decision rights are underdefined" (Transcript L4-L4))
- Positions:
  - P1: PMO is the framework owner and each gate has a named accountable decision owner (with default role mapping) recorded in initiative artifacts. ("the framework owner would be the PMO" (Transcript L5-L5))
  - P2: Leave governance implicit or role-based (risk: inconsistent enforcement and invented vetoes). ("A03 ... underdefined" (Transcript L4-L4))
- Arguments:
  - Named accountability is the key operational requirement to avoid unclear or stage-dependent ambiguity about who can decide. ("there should be a named person who is documented and accountable for the decision" (Transcript L7-L7))
  - Encoding decision ownership in the specification and resolution plan provides a repeatable enforcement anchor and a consistent mechanism for agents and humans. ("A03 is now checked off and marked Status: Resolved" (Transcript L12-L12))
- Warrant: If governance is not explicit and attributable to a named accountable decision owner, reviewers and agents will invent authority and gating behavior, causing inconsistency and failures of enforceability.
- Qualifier: As documented in the repo at the time of the session; some edge-case governance mechanics remain unspecified (see OQ1).
- Status: settled (documented in the repository).

## INSIGHT

### I1
- Insight: The repo’s “A03 resolved” state includes machine-consumable gate fields (`default_decision_owner_role`, `requires_named_decision_owner`) and advances the plan to A04, but the resolution plan progress summary appears internally inconsistent.
- Evidence: "The gate YAML shape was extended ..." and "A03 is now checked off ... next active ambiguity is A04." (Transcript L12-L12)
- Confidence: medium-high (based on in-session repo inspection).

## OPEN_QUESTION

### OQ1
- Question: Should the resolution plan progress summary be updated to reflect that A01–A03 are resolved (3 resolved / 13 remaining), rather than 2 resolved / 14 remaining?
- Why it matters: The summary is used as a quick status signal; inconsistent counts can mislead prioritization and sequencing.
- Partial progress: The inconsistency was detected and reported. ("Progress tracking inconsistency ... A01–A03 are checked" (Transcript L12-L12))

## NEXT_STEP

### NS1
- What: Proceed to A04 (minimum intake inputs and entry readiness) as the next ambiguity to resolve via interview and spec updates.
- Prompted by: Resolution plan tracking note advancing the next active ambiguity to A04. ("The next active ambiguity per the plan ... A04" (Transcript L12-L12))
- Urgency: soon

## Connections

D1 --[led_to]--> A1
I1 --[informed_by]--> A1
I1 --[led_to]--> OQ1
D1 --[led_to]--> NS1

## Trail Updates

- Creates/extends trail: `work-delivery-framework`.
- Related prior digests likely exist in `session_digests/` for A01 and A02; this session extends the same ambiguity-resolution sequence by capturing A03 as “resolved in repo” with governance and decision-rights mechanics. ("A01, A02, and A03 have been resolved" (Transcript L12-L12))
