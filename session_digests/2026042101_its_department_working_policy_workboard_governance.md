---
lorespec: "0.1"
id: "2026042101"
date: "2026-04-21"
source: "other"
topic: "Draft ITS Department Working Policy defining workboard governance, work roles, cadence, acceptance/closure, and minimal documentation standards."
tags: [its_department_working_policy, workboard, governance, workbrief, roles, cadence, acceptance, closure, raid_log, metrics]
classification:
  type: drafting
  secondary_type: operational
  domains: [operating_model, work_management, governance]
  value: high
trails: [workboard_policy, its_department_working_policy]
---

## Session Arc

### Started
Draft a simple ITS Department Working Policy with two guardrails: it must not override SSD-level policies, and it must align with the ITS Operating Model. (Transcript L4-L14)

### Pivots
- The policy moved from a short skeleton to an operating policy centered around a workboard system (physical + digital), with required work documentation and recurring review cadence. (Transcript L25-L82, L187-L216)
- Governance clarity tightened by defining per-work accountability roles (Delivery/Decision/Acceptance Owners) separately from a standing workboard administration role (Workboard Manager). (Transcript L83-L185)
- Acceptance/closure flow was split into its own subsection to reduce repetition and separate “who owns” vs “how the workflow runs”. (Transcript L217-L313)

### Ended
The draft stabilized around a workboard-centric operating policy with roles, cadence (review + daily board walk), acceptance/closure triggers, and one initial metric (“Work Brief Redefinition”). (Transcript L315-L420)

## ARTIFACT

### A1 - ITS Department Working Policy (draft)
- **Artifact:** `workboard_policy/its_department_working_policy_draft.md`
- **What it contains (high level):**
  - Policy authority and alignment (SSD policies prevail; aligned to ITS Operating Model).
  - Workboard system (physical + digital; digital is primary source of truth).
  - Minimum documentation requirements per planned work (workbrief, due date, RAID log + lifecycle).
  - Work roles per planned work (Delivery Owner, Decision Owner, Acceptance Owner) with “Primary Goal / Accountability / Authority”.
  - Standing role (Workboard Manager) with governance/administration responsibilities.
  - Cadence (Workboard Review schedule + daily Board Walk focused on flow correctness, not status).
  - Work Acceptance and Closure workflow (declarations + triggers + meeting to resolve non-acceptance).
  - Initial metric: Work Brief Redefinition.
- **Status:** Draft (content was iterated in a “canvas”; this markdown reflects the captured draft in-repo).
- **Source excerpt (Transcript L8-L14):** "This Working Policy does not supersede... shall prevail."

## DECISION

### D1 - Department working policy does not override SSD policy; aligns to ITS Operating Model
- **Decision:** ITS Department Working Policy must not supersede SSD Working Policy / Employee Handbook; and must remain aligned to ITS Operating Model.
- **Issue:** Avoid conflicting policy authority; keep departmental guidance consistent with the operating model.
- **Positions:**
  - Department policy can override SSD-level policies (rejected).
  - SSD-level policies prevail; department policy must align (chosen).
- **Arguments:** Prevents ambiguity and conflict; keeps local working rules subordinate to SSD governance.
- **Warrant:** A departmental policy is a practical guide, not a higher authority than SSD-wide policy.
- **Qualifier:** always
- **Status:** settled
- **Source excerpt (Transcript L10-L14):** "does not supersede... shall prevail... aligned with the ITS Operating Model."

### D2 - ITS workboard exists in physical + digital forms; digital is the accessible source of truth
- **Decision:** Maintain both a physical and a digital workboard; treat the digital workboard as the primary accessible tracking system.
- **Issue:** Provide both on-site visibility and always-accessible work tracking.
- **Positions:**
  - Physical board only.
  - Digital board only.
  - Both physical + digital (chosen).
- **Arguments:** Physical supports co-located collaboration; digital supports ongoing visibility and access.
- **Warrant:** The board is a coordination system; accessibility and visibility reduce misalignment.
- **Qualifier:** usually
- **Status:** settled
- **Source excerpt (Transcript L29-L33):** "workboard... both physical and digital... digital... source of truth."

### D3 - Minimum documentation standards required per planned work
- **Decision:** All planned work must be documented on the workboard with a per-work workbrief; each work has a due date; each work/deliverable has a RAID log with entries opened/closed as part of delivery and acceptance.
- **Issue:** Ensure planned work is visible and governable, and that risks/issues/dependencies are tracked through acceptance.
- **Positions:**
  - Allow undocumented work (rejected).
  - Require workbrief + due date + RAID log discipline (chosen).
- **Arguments:** Clear definition improves delivery and acceptance; RAID lifecycle creates explicit closure hygiene.
- **Warrant:** Work visibility and definition quality are prerequisites to reliable execution.
- **Qualifier:** always
- **Status:** settled
- **Source excerpt (Transcript L39-L45):** "planned work... documented... workbrief... Work Brief Redefinition..."

### D4 - Per-work ownership roles are defined in the workbrief; Decision Owner has final authority in acceptance disputes
- **Decision:** For each planned work, define Delivery Owner, Decision Owner, and Acceptance Owner and document them in the workbrief; one person may hold multiple roles; Delivery and Acceptance Owners are recommended (not required) to be separate; Decision Owner has final authority if acceptance is disputed.
- **Issue:** Remove ambiguity over accountability boundaries and escalation paths.
- **Positions:**
  - Leave role accountability implicit (rejected).
  - Define roles explicitly per work and document them (chosen).
- **Arguments:** Explicit role assignment improves “who approves/authorizes” clarity and reduces delivery vs acceptance conflict.
- **Warrant:** A governance system needs named accountability owners to resolve disputes and authorize commitments.
- **Qualifier:** usually
- **Status:** settled
- **Source excerpt (Transcript L83-L85):** "roles: Delivery Owner, Decision Owner, Acceptance Owner."

### D5 - Separate work-specific roles from standing workboard administration
- **Decision:** Keep Workboard Manager separate from per-work owner roles (Delivery/Decision/Acceptance).
- **Issue:** The phrase “documented in the workbrief” fits per-work roles, but not a standing administration role.
- **Positions:**
  - Include Workboard Manager with per-work roles (rejected).
  - Separate “Work Roles” from “Workboard Management” (chosen).
- **Arguments:** Reduces conceptual mismatch; clarifies that Workboard Manager is a system steward, not a work owner.
- **Warrant:** Standing roles support the system; per-work roles own specific work items.
- **Qualifier:** in this case
- **Status:** settled
- **Source excerpt (Transcript L143-L151):** "separate Work-specific owner roles from the Workboard administration role."

### D6 - Acceptance and closure run as an explicit sequence of declarations and triggers
- **Decision:** Delivery Owner declares delivery complete; Workboard Manager triggers acceptance review; Acceptance Owner declares acceptance review complete; accepted work proceeds to closure review; Workboard Manager coordinates resolution meeting for non-acceptance; Acceptance Owner conducts closure review; Workboard Manager triggers formal closure and clears closed items.
- **Issue:** Define an unambiguous operational flow from “delivered” to “accepted” to “closed”.
- **Positions:**
  - Keep acceptance/closure implied or embedded in role descriptions (rejected).
  - Define an explicit workflow subsection (chosen).
- **Arguments:** Makes gate conditions and responsibilities explicit; reduces repetition and confusion.
- **Warrant:** Stage transitions require explicit triggers/criteria to maintain governance discipline.
- **Qualifier:** usually
- **Status:** settled
- **Source excerpt (Transcript L217-L223):** "declare... trigger... accepted... begin closure... organize a meeting..."

## INSIGHT

### I1 - Policy readability improves by removing repetitive “role is accountable for…” lead-ins
- **Insight:** For role sections, repeated lead-ins add noise; headings should carry the subject and list items should go directly to the point.
- **Why it matters:** Makes the policy easier to scan and enforce; reduces interpretive ambiguity.
- **Confidence:** high
- **Source excerpt (Transcript L347-L354):** "remove repeated phrases... make each numbered item a direct statement."

### I2 - Board Walk is a flow/correctness control, not a status meeting
- **Insight:** A daily Board Walk should focus on correcting work-state and unblocking flow (“preventing work from moving”), not individual status reporting.
- **Why it matters:** Protects the board from drifting into performative reporting; keeps attention on system throughput and state correctness.
- **Confidence:** high
- **Source excerpt (Transcript L315-L319):** "verify flow... not... status updates... preventing this work from moving."

### I3 - “Delivery Owner” should be understood as accountable, not necessarily the executor
- **Insight:** “Delivery Owner” is typically the accountable owner of delivery outcomes and coordination, not automatically the person doing all hands-on work.
- **Why it matters:** Prevents misassignment of work and supports delegation/resourcing without losing accountability.
- **Confidence:** medium (framed as “typically” / unless explicitly defined otherwise)
- **Source excerpt (Transcript L425-L430):** "typically accountable rather than the one doing all execution."

## PATTERN

### P1 - Local template for defining governance roles (Primary Goal → Accountability → Authority)
- **Pattern (scope: local):**
  1. Start each role with a one-sentence **Primary Goal**.
  2. Write **Accountability** items as noun phrases (what outcomes the role owns).
  3. Write **Authority** items as action verbs (what approvals/declarations the role can make).
  4. Keep list items direct; avoid repeating the role name inside each bullet/item.
- **When to use:** Any ITS governance artifact that defines roles (workbrief templates, policies, framework docs).
- **Source excerpt (Transcript L389-L404):** "use noun phrases... action verbs... Declare delivery complete..."

### P2 - Local cadence pattern: recurring review plus a daily flow check
- **Pattern (scope: local):**
  1. Set a team-defined Workboard Review schedule.
  2. If a session falls on a non-working day, defer to the next regular session unless a special session is agreed.
  3. Run a daily Board Walk to correct state and unblock flow; move cards immediately or schedule a follow-up.
- **When to use:** Maintaining workboard hygiene and keeping work-state accurate.
- **Source excerpt (Transcript L56-L66):** "meet on a regular schedule... falls on a non-working day... deferred..."

## NEXT_STEP

### N1 - Draft Acceptance Review Report (Joven)
- **Action:** Prepare a draft Acceptance Review Report for discussion in the next meeting (meeting date not specified).
- **Urgency:** soon
- **Prompted by:** User-provided next-meeting action items (image addendum, 2026-04-21)
- **Source excerpt (Image addendum, 2026-04-21):** "Acceptance Review Report - Joven"

### N2 - Draft Workboard Manager terms of reference (Joven)
- **Action:** Draft Workboard Manager terms of reference for review in the next meeting.
- **Urgency:** soon
- **Prompted by:** User-provided next-meeting action items (image addendum, 2026-04-21)
- **Source excerpt (Image addendum, 2026-04-21):** "Workboard Manager terms of reference draft - Joven"

### N3 - Draft Delivery Owner terms of reference (Joven)
- **Action:** Draft Delivery Owner terms of reference for review in the next meeting.
- **Urgency:** soon
- **Prompted by:** User-provided next-meeting action items (image addendum, 2026-04-21)
- **Source excerpt (Image addendum, 2026-04-21):** "Delivery Owner terms of reference draft - Joven"

## REFERENCE

### R1 - Prior related digest: Delivery Owner / Workbrief field split / removal of PM as core role
- **Reference:** `session_digests/2026042001_digital_workbrief_field_split_and_delivery_owner_accountability_clarification.md`
- **Why relevant:** Captures adjacent decisions that connect to this policy’s role/accountability framing and workbrief structure.

## Connections

- D1 -[led_to]-> A1
- D2 -[led_to]-> A1
- D3 -[led_to]-> A1
- D4 -[led_to]-> A1
- D5 -[led_to]-> A1
- D6 -[led_to]-> A1
- I1 -[informed_by]-> P1
- I2 -[instance_of]-> P2
- I3 -[related_to]-> R1
- D4 -[related_to]-> R1
- A1 -[related_to]-> R1

## Trail Updates

- Extends trail: `workboard_policy` (department-level workboard governance policy draft and operating cadence)
- Extends trail: `its_department_working_policy` (policy authority, roles, documentation standards, acceptance/closure workflow)
