# ITS Operating Model

## 1. Purpose

The ITS Operating Model exists to systematically reduce operational, security, compliance, and continuity risk while delivering reliable, auditable, and mission-aligned IT outcomes.

It is the management control model for how ITS work is governed, executed, supported, and closed.

Unmanaged work, unclear ownership, undocumented systems, weak closure, and person-dependent knowledge are not inefficiencies. They are operational risks. This model exists to eliminate those risks through the structure of how ITS operates every day.

This document explains the control intent. It does not replace the detailed work stages in the [Work Delivery Framework](work%20delivery/work_delivery_framework.md).

## 2. Risks This Model Is Designed to Reduce

The operating model is built around six categories of risk that ITS must actively manage:

| Risk | What goes wrong without control |
|---|---|
| **Operational risk** | Work runs informally, ownership is unclear, failures repeat, and quality degrades over time |
| **Security risk** | Changes are untracked, access is ungoverned, and the attack surface grows without visibility |
| **Compliance risk** | Decisions are undocumented, approvals cannot be demonstrated, and audits cannot be answered |
| **Continuity risk** | Systems, services, and processes cannot continue operating through staff change, absence, or disruption |
| **Key-person dependency risk** | Operational knowledge lives in one person's head and cannot be transferred, recovered, or accessed when that person is unavailable |
| **Change and support risk** | Changes are made without control, solutions cannot be supported, and problems compound after delivery |

When the operating model is applied consistently, each of these risks is reduced because work is visible, owned, documented, and formally closed.

## 3. How the Core Documents Work Together

Use the repository documents as one risk control system:

1. This document explains why the controls exist and what risk they reduce.
2. The [ITS Work Management Model](its_work_management_model.md) states the simple control logic for planned work: define, decide, and deliver properly.
3. The [Work Delivery Framework](work%20delivery/work_delivery_framework.md) is the practical stage-by-stage control path for planned work from intake to closure.
4. The [Standard Deliverables Guide](work%20delivery/standard_deliverables_guide.md) and [Deliverable Specifications Index](work%20delivery/deliverable_specifications_index.md) help teams select and produce the right artifacts at each control point.

If two documents appear to overlap, use this rule:

- this document explains why the controls exist and what risk they address
- the ITS Work Management Model explains the simple control logic
- the Work Delivery Framework explains how planned work operates in practice

## 4. Controls That Reduce Risk

Each control below directly reduces one or more of the risks in Section 2. These are not optional preferences. They are the minimum conditions for safe, governable ITS work.

| Control | Risk it reduces |
|---|---|
| **Visibility** — work is visible before and during execution | Operational risk; prevents undetected scope creep, effort duplication, and uncontrolled activity |
| **Explicit ownership** — accountable people are named, not assumed | Operational risk; ensures accountability is clear, work does not stall, and responsibility cannot be disclaimed |
| **Documented decisions** — approvals and choices are recorded with evidence | Compliance risk; enables audit, reduces disputes, and makes decisions defensible |
| **Controlled change** — changes are logged, reviewed, and traceable | Security risk and change risk; prevents unauthorized changes and supports recovery |
| **Supportable systems** — solutions are documented for handover beyond the original implementer | Continuity risk and key-person dependency risk; enables recovery and staff transition |
| **Formal closure** — work closes with acceptance, evidence, and handoff | Support risk; prevents open ownership gaps, unresolved conditions, and undocumented live systems |
| **Documentation as a control** — documentation is treated as an operational requirement, not an optional extra | Continuity risk and key-person dependency risk; ensures the organization can recover, audit, and sustain operations independently of individuals |

## 5. Operating Principles

Each principle below is a risk control. Breaking any of them introduces a specific, avoidable failure.

1. **Visibility before control.** Work that cannot be seen cannot be governed. Invisible work is unmanaged risk.
2. **Explicit ownership before execution.** Unowned work is nobody's responsibility. Accountability must be named, not assumed.
3. **Defined scope before commitment.** Starting work without defined scope is a change risk. The organization must know what it is agreeing to before effort and cost begin.
4. **Traceability as an audit and recovery control.** Decisions and changes that leave no record cannot be audited, defended, or reversed. Every material decision should be traceable.
5. **Supportability as a completion requirement.** A solution that only one person can run or support is a continuity risk. Work is not complete until it can be handed over and sustained.
6. **Formal closure to remove residual risk.** Work that fades out without formal closure leaves ownership, support, and decision gaps open. Open gaps are operational risks.

## 6. Operating Areas

### 6.1. Service Operations

**Risk controlled:** Operational risk, continuity risk, and key-person dependency risk.

ITS should deliver through defined services, not informal personal channels. When service delivery is informal and unstructured, it becomes dependent on individuals, demand is invisible, and quality cannot be maintained.

**What failure looks like:** Service requests are routed to specific people rather than through a defined path. Incidents are resolved ad hoc without improvement. Demand is invisible and unprioritized. Knowledge about how services run lives only with the people who built them.

**What this control requires:**

- requests and incidents use the agreed intake path so demand is visible and routable
- service ownership is named and visible so accountability is clear
- support demand is routed and prioritized deliberately so capacity is managed
- recurring issues lead to improvement, not repeated workarounds

### 6.2. Planned Work

**Risk controlled:** Operational risk, compliance risk, change risk, and continuity risk.

Planned work should move through a governed path from intake to closure. Work that starts without definition, progresses without authorization, and closes without acceptance is uncontrolled activity. Uncontrolled activity is the root cause of most avoidable delivery failures.

**What failure looks like:** Work starts because someone asked verbally or because it seems urgent. Scope expands silently. No one knows the full picture of what is in flight. Ownership is unclear. Closure is assumed rather than confirmed.

**What this control requires:**

- work is assessed before definition effort grows, so investment is made deliberately
- scope, outcomes, owners, and deliverables are clear before authorization, so commitments are informed
- progress is visible through deliverables, evidence, decisions, and current status
- scope change is explicit and controlled, so commitments remain accurate
- acceptance, handover, and closure are formal, so the organization knows what it has accepted and who owns it

Planned work follows the [Work Delivery Framework](work%20delivery/work_delivery_framework.md).

### 6.3. Stability and Change Control

**Risk controlled:** Security risk, change risk, and compliance risk.

ITS should operate in a way that keeps changes understandable, recoverable, and reviewable. Uncontrolled changes are a primary source of security incidents, service disruptions, and compliance failures.

**What failure looks like:** Changes are made without logging. Access is granted informally and not reviewed. Problems emerge and recovery is blocked because no one can explain what changed. Operational shortcuts quietly become the standard practice.

**What this control requires:**

- changes are logged and explainable so the state of systems is always known
- access is governed and attributable so security risk is bounded
- recovery and rollback are considered before material change, so recovery is possible
- operational shortcuts do not quietly replace controlled practice

### 6.4. Sustainability and Continuity

**Risk controlled:** Continuity risk, key-person dependency risk, and support risk.

ITS should reduce dependency on individual memory or heroics. When operational knowledge lives with one person, that person's absence, departure, or unavailability becomes an organizational risk.

**What failure looks like:** A system goes down and only one person knows how to recover it. A staff member leaves and their work cannot be handed over. A solution is delivered but no one can support it. Runbooks and configuration details exist only in email threads.

**What this control requires:**

- systems and work are documented enough for handover
- run and support ownership are named and explicit
- knowledge is shared so multiple people can operate and recover systems
- operational responsibility can continue through staff change, absence, or turnover

## 7. Planned Work Lifecycle as a Risk Control Path

Each stage of the planned work lifecycle is a risk control gate, not just a process step. Skipping or weakening a stage does not save time. It defers risk into delivery, operations, or support.

1. **Assess** — control gate for investment risk: is this work worth defining at all?
2. **Define** — control gate for scope and commitment risk: is the work clear enough to authorize?
3. **Authorize** — control gate for compliance risk: is there an explicit, attributable decision to proceed?
4. **Elaborate** — control gate for change risk: is detail added only for what was authorized?
5. **Mobilize** — control gate for delivery risk: are the right people, tools, and controls in place before execution starts?
6. **Deliver** — control gate for operational and evidence risk: is progress visible and are decisions and changes recorded as work proceeds?
7. **Accept, hand over, and close** — control gate for continuity and support risk: is the work formally accepted, ownership handed over, and residual risk closed?

This lifecycle is implemented through the [Work Delivery Framework](work%20delivery/work_delivery_framework.md).

## 8. Risk Indicators

Use these indicators to assess whether the operating model is working.

**Lower risk — these are positive signs:**

- people can explain what work is active, who owns it, and what it is waiting for
- scope and deliverables are understandable without verbal reconstruction
- decisions and changes can be traced back to records
- services and solutions can be supported by someone other than the original implementer
- work closes with visible acceptance and handover evidence

**Higher risk — these are warning signs:**

- work starts from conversations or urgency alone with no visible definition or owner
- scope changes without a recorded decision
- ownership is unclear or informally shared between people
- evidence is reconstructed at the end rather than collected during delivery
- live services depend on undocumented personal knowledge
- work is treated as complete without acceptance, handover, or closure

The warning signs are not just process gaps. Each one is an open operational risk.

## 9. Why This Matters

The purpose of this operating model is not to impose process for its own sake.

It exists because unmanaged work, unclear ownership, undocumented systems, and informal operations produce predictable and avoidable failures: outages that could not be recovered, audits that cannot be answered, staff departures that take critical knowledge with them, and changes that break things with no clear path to resolution.

The operating model makes ITS work safer, more recoverable, more accountable, and more sustainable. It does this by making risk visible and making the controls that reduce risk part of how ITS operates every day.

## 10. Related Documents

- [README](README.md)
- [ITS Work Management Model](its_work_management_model.md)
- [Work Delivery Framework](work%20delivery/work_delivery_framework.md)
- [Work Assessment Process](work%20delivery/work_assessment/work_assessment_process.md)
- [Work Brief Specification](work%20delivery/work_brief/work_brief_specification.md)
