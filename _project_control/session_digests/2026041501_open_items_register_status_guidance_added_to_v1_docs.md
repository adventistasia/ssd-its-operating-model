---
lorespec: "0.1"
id: "2026041501"
date: "2026-04-15"
source: "codex"
topic: "Added Open Items Register status guidance to v1 and a framework-level rule requiring status-list descriptions"
tags: [work-delivery-framework, open-items-register, status-model, v1, ai-sufficiency, lore]
classification:
  type: "drafting"
  secondary_type: "operational"
  domains: [framework-design, documentation, delivery-readiness]
  value: "medium"
trails: [work-delivery-framework]
---

## Session Arc

### Started
The session began with a question about what the Open Items Register statuses mean in the `v1` artifact specification, with an explicit request to also check `session_digests/` and the authoritative `work_delivery_framework_specification.md` before answering.

### Pivots
- The first pivot was from a generic "what do the statuses mean" question into a scoped interpretation request anchored to `work_delivery_framework/v1/artifact_specifications/open_items_register_specification.md` and cross-checked against the authoritative framework specification. Source: "what do the status mean? also check session_digests/ and ... work_delivery_framework_specification.md before answering." (Transcript L3-L3)
- The second pivot turned explanation into documentation work: the user asked that the status descriptions be incorporated into the `v1` files related to the Open Items Register so readers would know both what each status means and when to use it. Source: "incorporate the description for the statuses into the v1 files related to open items register..." (Transcript L5-L5)
- The third pivot settled the implementation approach by confirming that the `v1` wording should stay aligned to the authoritative model while adding local guidance in the specification, template, and example. Source: "yes that's what I want. make the edits." (Transcript L7-L7)
- The fourth pivot broadened the local documentation fix into a framework policy rule: the user requested that the authoritative specification explicitly require short descriptions for status lists so readers understand what such statuses are for wherever they appear. Source: "include instructions or policy statement in the ... work_delivery_framework_specification.md about including a short description of any statuses list..." (Transcript L11-L11)

### Ended
The session ended after the `v1` Open Items Register specification, template, and example were updated, a new framework-level policy statement was added to `work_delivery_framework_specification.md`, and the user asked that this digest be rewritten to include that final addition.

## ARTIFACT

### A1
- Artifact: Updated the `v1` Open Items Register documentation set:
  1. `work_delivery_framework/v1/artifact_specifications/open_items_register_specification.md`
  2. `work_delivery_framework/v1/templates/open_items_register_template.md`
  3. `work_delivery_framework/v1/examples/open_items_register_example.md`
- Final state: The `v1` specification now defines all five allowed statuses with plain-language meaning and usage guidance; the template now explains the statuses where authors fill the register and adds guardrails for `monitoring` and `closed`; the example now shows all five lifecycle states in realistic rows rather than only `open` and `in progress`.
- Evolution: The session first established the authoritative meaning from Section `2.11.2` of `work_delivery_framework_specification.md`, then applied that model into the `v1` docs without changing the underlying lifecycle semantics.
- Source: "I’m applying the agreed documentation changes in the v1 Open Items Register spec, template, and example." and "Updated the v1 Open Items Register docs so the status model is defined where people read and use it." (Transcript L8-L8)

### A2
- Artifact: Updated `work_delivery_framework/work_delivery_framework_specification.md` to add a framework-level policy statement requiring short descriptions for status lists and other controlled state vocabularies.
- Final state: The authoritative specification now states that where an artifact, template, or machine-readable block defines an allowed status list or other controlled state vocabulary, the document must also include a short description of what the statuses are for and what each status means in use, unless that meaning is already stated immediately adjacent to the list in equally explicit terms.
- Evolution: This addition generalized the Open Items Register clarification into a reusable framework rule under the AI-sufficiency baseline checklist rather than leaving it as a one-off documentation improvement in the `v1` files.
- Source: "I’m adding one general normative rule there so any status list in the framework must carry a short purpose/meaning description..." (Transcript L12-L12)

## DECISION

### D1
- Decision: Keep the `v1` Open Items Register status wording aligned with the authoritative status model in `work_delivery_framework_specification.md`, and add short usage guidance in the `v1` specification, template, and example instead of inventing a separate `v1` interpretation.
- Issue: How to make the `v1` Open Items Register files understandable at point of use without creating drift from the canonical framework.
- Positions:
  1. Leave `v1` terse and rely on readers to consult the authoritative framework
  2. Re-express the authoritative status model directly in the `v1` docs with usage guidance
  3. Introduce a new simplified `v1` status interpretation
- Arguments: Readers need the meanings where they author and review the register, but the lifecycle semantics should remain identical to the canonical A14 control model to avoid inconsistency across the framework.
- Warrant: If `v1` is meant to be usable on its own for drafting and review, it must carry enough local guidance to prevent misinterpretation, but it should not fork the framework's control model.
- Qualifier: for the `v1` Open Items Register documentation set
- Status: settled
- Source: "I recommend keeping the wording aligned to the authoritative spec, then adding short usage guidance in the v1 docs..." and "yes that's what I want. make the edits." (Transcript L6-L7)

### D2
- Decision: Add a general policy statement to the authoritative framework requiring short descriptions for status lists and other controlled state vocabularies wherever they are defined.
- Issue: Whether the need for status explanations should remain a local documentation improvement for the Open Items Register or be encoded as a reusable framework rule.
- Positions:
  1. Keep the clarification local to the `v1` Open Items Register files
  2. Add a framework-wide rule so status vocabularies must be explained wherever they appear
- Arguments: The same ambiguity can recur in other artifacts, templates, or machine-readable blocks, so the requirement should live in the authoritative framework rather than depending on local author discipline.
- Warrant: If controlled vocabularies are meant to be used consistently by humans and AI agents, their operational purpose and meanings must be stated as part of the framework's sufficiency rules, not assumed from a bare list.
- Qualifier: for status lists and comparable controlled state vocabularies
- Status: settled
- Source: "include instructions or policy statement in the ... work_delivery_framework_specification.md..." and the inserted requirement text. (Transcript L11-L12)

## INSIGHT

### I1
- Insight: For operational framework artifacts, readers need status definitions at the point of use, not only in the authoritative master specification.
- Domain: documentation
- Confidence: high
- Source: "so that readers will understand when to use each status and what the statuses mean when they see it." (Transcript L5-L5)

### I2
- Insight: The main status distinction most likely to be misunderstood is not the list itself but the behavioral boundary between `monitoring`, `resolved`, and `closed`.
- Domain: delivery-readiness
- Confidence: medium
- Source: The user asked what the statuses mean, and the resulting edits added explicit guidance that `monitoring` is deliberate observation and that `resolved` is not yet `closed`. (Transcript L3-L8)

### I3
- Insight: A documentation clarification becomes more durable when it is converted from a local fix into a framework-level authoring rule.
- Domain: framework-design
- Confidence: high
- Source: The session moved from updating `v1` files to adding a normative policy statement in the authoritative specification. (Transcript L11-L12)

## PATTERN

### P1
- Pattern: Clarify a localized documentation ambiguity by tracing the authoritative rule first, then propagating it into point-of-use artifacts.
- Scope: local
- Components:
  1. identify the local artifact the user is reading
  2. confirm the canonical definition in the authoritative framework source
  3. check recent session digests for prior rationale or competing interpretations
  4. answer the immediate question using the canonical model
  5. if requested, propagate that model into templates/examples/specs where authors will encounter it
- Why it matters: This avoids local reinterpretation while still improving usability for readers who work primarily from local templates or examples, and it can surface when a local clarification should be generalized into a framework rule.
- Source: "also check session_digests/ and ... work_delivery_framework_specification.md before answering." (Transcript L3-L3)

## REFERENCE

### R1
- Reference: Prior session digest [2026041301_work_delivery_framework_a14_a15_resolved_and_a12_opened.md](</home/rmicua/projects/ssd-its-operating-model/session_digests/2026041301_work_delivery_framework_a14_a15_resolved_and_a12_opened.md>)
- Relevance: That session recorded the A14 decision that established the canonical Open Items Register model, including typed entries, blocker handling, escalation, and the authoritative lifecycle status model later reused here.
- Source: The session explicitly checked `session_digests/` before answering and found alignment with the A14 model. (Transcript L3-L4)

## SOLUTION

### S1
- Problem: The `v1` Open Items Register files listed allowed statuses but did not explain what each status meant or when to use it, leaving readers to infer semantics from the authoritative framework or guess at lifecycle meaning.
- Fix: Added plain-language status definitions to the `v1` artifact specification, added status guidance and lifecycle guardrails to the `v1` template, and expanded the `v1` example to demonstrate `open`, `in progress`, `monitoring`, `resolved`, and `closed`.
- Why the fix works: It preserves the canonical status model while making drafting and review self-explanatory inside the `v1` document set.
- Caveats: The `v1` Open Items Register files were updated directly, but other status vocabularies in the broader framework will still require local implementation follow-through where needed.
- Source: "Updated the v1 Open Items Register docs so the status model is defined where people read and use it." (Transcript L8-L8)

### S2
- Problem: The framework had no explicit cross-cutting rule requiring authors to explain what status lists are for, so the same ambiguity could recur in other artifacts and structured blocks.
- Fix: Added a normative statement to the AI-sufficiency baseline checklist in `work_delivery_framework_specification.md` requiring short purpose-and-meaning descriptions for allowed status lists and other controlled state vocabularies unless equally explicit wording already appears adjacent to the list.
- Why the fix works: It turns a one-off clarification into an enforceable framework expectation that supports both human readability and AI interpretation.
- Caveats: The new rule sets the standard, but existing artifacts may still need targeted updates to fully comply.
- Source: "Added the policy statement..." and the inserted rule text in the authoritative specification. (Transcript L12-L13)

## Connections

D1 --[led_to]--> A1
D2 --[led_to]--> A2
I1 --[informed_by]--> D1
I2 --[informed_by]--> S1
I3 --[informed_by]--> D2
P1 --[led_to]--> D1
P1 --[led_to]--> D2
R1 --[informed_by]--> D1
S1 --[led_to]--> A1
S2 --[led_to]--> A2
S2 --[related_to]--> S1
R1 --[related_to]--> A1
A2 --[related_to]--> A1

## Trail Updates

- Extends the `work-delivery-framework` trail.
- Builds on [2026041301_work_delivery_framework_a14_a15_resolved_and_a12_opened.md](</home/rmicua/projects/ssd-its-operating-model/session_digests/2026041301_work_delivery_framework_a14_a15_resolved_and_a12_opened.md>), which established the canonical Open Items Register model and status lifecycle that this session propagated into `v1`.
- Adds a documentation-layer follow-through to the A14 control model by making the status meanings visible in the `v1` authoring and example materials.
- Extends that local follow-through into a framework-level authoring rule in `work_delivery_framework_specification.md`, so future status vocabularies must carry short explanatory descriptions rather than appearing as bare lists.
