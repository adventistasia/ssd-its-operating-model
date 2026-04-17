---
lorespec: "0.1"
id: "2026041302"
date: "2026-04-13"
source: "codex"
topic: "Work Delivery Framework A12, A16, and A17 resolved; ambiguity register closed"
tags: [work-delivery-framework, ambiguity-resolution, A12, A16, A17, closure-record, lore]
classification:
  type: "drafting"
  secondary_type: "operational"
  domains: [framework-design, delivery-readiness, governance]
  value: "high"
trails: [work-delivery-framework]
---

## Session Arc

### Started
The session resumed the registered ambiguity-resolution sequence for `work_delivery_framework/work_delivery_framework_specification.md`, with the user asking for one-by-one interviewing, recommendations with tradeoffs, and synchronized updates to both the specification and the resolution plan until the intent was understood well enough to resolve each item.

### Pivots
- The first major pivot resolved `A12` by rejecting a generic external-vendor model in favor of three canonical modes: staff augmentation, co-delivery, and full external delivery. Source: "Let's go with the 3-mode model." (Transcript L7-L7)
- The second pivot made `full external delivery` materially different from `co-delivery` by requiring the handoff package to stand almost entirely on its own, while keeping formal gate ownership internal. Source: "handoff package to be expected to stand almost entirely on its own" (Transcript L19-L19)
- The third pivot turned anti-bureaucracy from a slogan into a control system by selecting a hybrid waiver model with non-waivable core controls, a readiness-impact test, tiered PMO review triggers, and Decision Log recording. Source: "3" / "yes" / "2" across the anti-bureaucracy decisions (Transcript L23-L33)
- The fourth pivot resolved `A17` by choosing a rule-based gate-to-critical-artifact mapping, persistent control artifacts from Gate 2 onward, packet-mode elevation rules for explicitly gate-tied deliverables, and a new universal `Closure Record` for Gate 8. Source: "2" on the rule-based mapping, "2" on persistence, and "a new Closure Record in the framework." (Transcript L35-L35, L47-L47, L67-L67)

### Ended
The session ended with `A12`, `A16`, and `A17` written into the specification, checked off in the resolution plan, and the ambiguity register fully closed at 17 of 17 resolved items. The user then redirected the thread to creating this session digest.

## ARTIFACT

### A1
- Artifact: Updated `work_delivery_framework/work_delivery_framework_specification.md` and `work_delivery_framework/resolution_plan_work_delivery_framework_specification.md` to resolve `A12`, `A16`, and `A17`, and to close the ambiguity register.
- Final state: The specification now includes:
  1. a resolved external-engagement model with three canonical modes and explicit handoff/governance implications
  2. a resolved anti-bureaucracy control model in new Section `2.13`
  3. a resolved gate-to-critical-artifact mapping model in new Section `2.14`
  4. explicit gate YAML `critical_stage_defining_artifacts` and stable mapping-rule references
  5. a new `Request Intake Record` artifact for Gate 1 and a new `Closure Record` artifact for Gate 8
- Evolution: The session first closed `A12`, then `A16`, then expanded `A17` from a mapping exercise into a small taxonomy update when the user chose to introduce a universal closure artifact.
- Source: "The edits are in." and "All ambiguities in the current resolution plan are now closed." (Transcript L22-L22, L68-L68)

### A2
- Artifact: Canonical framework additions `ARTIFACT-REQUEST-INTAKE-RECORD` and `ARTIFACT-CLOSURE-RECORD`.
- Final state: `Request Intake Record` now anchors Gate 1 qualification evidence, and `Closure Record` is a universal framework artifact required by Gate 8 to support formal closure.
- Evolution: The intake record emerged from the decision that Gate 1 should remain artifact-light but still have decisive evidence, while the closure artifact emerged only after the user explicitly chose a dedicated closure record rather than a stronger decision-record section.
- Source: "Do you want Gate 1 to use the intake/request record..." / "a new Closure Record in the framework." (Transcript L52-L53, L66-L67)

## DECISION

### D1
- Decision: Resolve `A12` by defining exactly three canonical external engagement modes: `staff augmentation`, `co-delivery`, and `full external delivery`.
- Issue: Whether the framework should treat external involvement as one generic vendor case or distinguish modes that materially change governance and handoff expectations.
- Positions:
  1. One generic external-delivery mode
  2. A small fixed set of canonical modes
  3. A freeform project-by-project engagement profile
- Arguments: A small fixed set preserves repeatability and auditability without bloating the framework; it distinguishes embedded capacity from shared delivery and from autonomous external execution.
- Warrant: If external participation changes who needs the documentation and how independently they can act, the framework must model those differences explicitly rather than hiding them behind one label.
- Qualifier: for this operating model
- Status: settled
- Source: "Let's go with the 3-mode model." (Transcript L7-L7)

### D2
- Decision: `Staff augmentation` is not a formal external handoff mode; `co-delivery` and `full external delivery` both require a `Delivery Charter`; `full external delivery` carries the stronger standalone-handoff standard.
- Issue: How the three engagement modes should differ in governance and handoff rigor.
- Positions:
  1. Treat staff augmentation as a non-handoff embedded mode
  2. Treat staff augmentation as a light external mode
  3. Treat staff augmentation like co-delivery
- Arguments: Staff augmentation changes capacity more than handoff, while full external delivery requires near-standalone execution ability and therefore a stronger completeness bar than co-delivery.
- Warrant: If the external team is expected to execute autonomously, the package must stand on its own; if the external people are embedded in the internal delivery model, forcing full handoff controls adds bureaucracy without improving readiness.
- Qualifier: within the three-mode model
- Status: settled
- Source: "1" on staff augmentation and "handoff package to be expected to stand almost entirely on its own" (Transcript L11-L11, L19-L19)

### D3
- Decision: Resolve `A16` with a hybrid anti-bureaucracy model: core controls are never waivable, only explicitly waivable non-core items may be omitted, and omissions are valid only if they do not weaken readiness outcomes.
- Issue: How to prevent the framework from becoming bureaucratic without letting teams skip rigor informally.
- Positions:
  1. Strict mandatory model
  2. Broad waiver model
  3. Hybrid model with protected core controls and controlled omissions
- Arguments: The hybrid model preserves speed where low-value overhead exists, while keeping gates, named ownership, required artifacts, control registers, and triggered conditionals non-waivable.
- Warrant: Anti-bureaucracy is credible only when omission rules are explicit, reviewable, and tied to the same readiness/traceability standard that justifies the framework.
- Qualifier: across small-work and large-work
- Status: settled
- Source: "3" / "yes" / "2" / "yes" across the anti-bureaucracy interview sequence. (Transcript L23-L33)

### D4
- Decision: Resolve `A17` with a rule-based critical-artifact mapping model, persistent control artifacts from Gate 2 onward, packet-mode gate-elevation rules, and a universal `Closure Record` at Gate 8.
- Issue: How to determine which artifacts are truly stage-defining at each gate when packaging modes, triggered conditionals, and embedded evidence vary.
- Positions:
  1. Minimal or flat gate mappings
  2. Rule-based mappings with substitution, persistence, and trigger logic
  3. Case-by-case reviewer inference
- Arguments: Rule-based mapping keeps gate evaluation repeatable without forcing a separate artifact for every gate, while still allowing conditional artifacts to become critical when the current gate materially depends on them.
- Warrant: If gate quality depends on the artifacts that actually define stop/proceed readiness, the framework must express that dependency structurally rather than leaving it to reviewer intuition.
- Qualifier: for the current artifact taxonomy, with one new closure artifact introduced by this session
- Status: settled
- Source: "2" on the rule-based model, "2" on persistence, and "a new Closure Record in the framework." (Transcript L35-L35, L47-L47, L67-L67)

## INSIGHT

### I1
- Insight: In this framework, external participation is not a single phenomenon; the distinction that matters most is whether the external party is embedded, shared, or expected to execute autonomously.
- Domain: governance
- Confidence: high
- Source: "Let's go with the 3-mode model." and "handoff package to be expected to stand almost entirely on its own" (Transcript L7-L7, L19-L19)

### I2
- Insight: Anti-bureaucracy became enforceable only after the conversation reframed it as an omission-control system rather than a general preference for less process.
- Domain: framework-design
- Confidence: high
- Source: "3" on the hybrid model and "yes" on non-waivable core controls. (Transcript L23-L25)

### I3
- Insight: Gate-criticality in a mixed packet/standalone framework cannot be represented well by a simple required-by-gate list; it needs persistence, substitution, trigger, and embedded-evidence rules.
- Domain: delivery-readiness
- Confidence: high
- Source: "2" on rule-based mapping, "Yes. But work brief may also define required artifacts as part of deliverables..." and "1" on embedded evidence. (Transcript L35-L35, L41-L41, L55-L55)

## PATTERN

### P1
- Pattern: Resolve framework ambiguity by layering three levels of precision.
- Scope: local
- Components:
  1. choose the conceptual model for the ambiguity
  2. convert that model into enforceable control rules
  3. push the rule into both prose and machine-consumable YAML
  4. update the resolution plan immediately so the sequence state remains truthful
- Why it matters: The session did not stop at conceptual agreement. Each ambiguity was only treated as resolved once the rule, artifact model, and tracker state all aligned.
- Source: "Once you are satisfied, synthesize the findings, update ... specification.md and ... resolution plan ... (check off the ambiguity item)." (Transcript L1-L1)

## SOLUTION

### S1
- Problem: The specification's completeness model required `critical_stage_defining_artifacts`, but later gates still relied on placeholders and reviewer inference, especially where packet mode and conditional artifacts complicated the evidence set.
- Fix: Added Section `2.14`, replaced `A17` placeholders in gate YAML with explicit artifact lists and stable mapping-rule references, and introduced `Request Intake Record` and `Closure Record` so Gate 1 and Gate 8 have canonical decisive evidence.
- Why the fix works: It preserves a single artifact taxonomy while making gate evidence repeatable across small-work, large-work, triggered conditionals, and embedded-evidence cases.
- Caveats: The new `Closure Record` slightly expands the canonical artifact set beyond what existed before this session, so downstream templates or guidance that assumed closure lived only in a review record may need alignment later.
- Source: "a new Closure Record in the framework." and the final state that "All ambiguities ... are now closed." (Transcript L67-L68)

## Connections

D1 --[led_to]--> A1
D2 --[depends_on]--> D1
D2 --[led_to]--> A1
D3 --[led_to]--> A1
D4 --[led_to]--> A1
D4 --[led_to]--> A2
I1 --[informed_by]--> D1
I2 --[informed_by]--> D3
I3 --[informed_by]--> D4
P1 --[led_to]--> D1
P1 --[led_to]--> D3
P1 --[led_to]--> D4
S1 --[depends_on]--> D4
A2 --[related_to]--> S1

## Trail Updates

- Extends the `work-delivery-framework` trail.
- Continues directly from [2026041301_work_delivery_framework_a14_a15_resolved_and_a12_opened.md](</home/rmicua/projects/ssd-its-operating-model/session_digests/2026041301_work_delivery_framework_a14_a15_resolved_and_a12_opened.md>), which left `A12` as the next active ambiguity.
- Closes the deferred mapping thread opened in [2026041203_work_delivery_framework_a08_completeness_and_delivery_readiness_resolved.md](</home/rmicua/projects/ssd-its-operating-model/session_digests/2026041203_work_delivery_framework_a08_completeness_and_delivery_readiness_resolved.md>), where `A17` was intentionally postponed instead of inferred.
- Adds settled objects for the external-engagement model, anti-bureaucracy control model, and final gate-to-critical-artifact mapping, and records that the current ambiguity register is fully closed.
