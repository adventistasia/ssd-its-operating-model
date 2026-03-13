# Initiative Definition (ID) Specification

## 1. Purpose

The Initiative Definition (ID) is the **primary reference document** for an initiative.

It exists to:

- Explain **what the initiative is**
- Explain **why it exists** (problem, value, outcomes)
- Define **what will be delivered** (deliverables, scope boundaries, acceptance owners)
- Provide an **approved definition** that the initiative can be managed against
- Remain a **living document** that is updated as the initiative progresses

After completion, the ID remains the **authoritative record** of the initiative’s intended outcomes, delivered scope, and acceptance ownership.

## 2. When the ID Is Required

An ID is required for:

- Projects
- Significant enhancements
- Planned initiatives that change systems, data, services, security posture, operational load, or cost

## 3. Intended Readers

The ID should be usable by:

- Sponsors and leadership
- Outcome Owner, Delivery Owner, Delivery Team
- Acceptance Authorities
- Operations and Support
- Audit and future maintainers

## 4. How the ID Is Maintained

The ID is expected to be updated throughout the initiative.

Minimum expectations:

- Keep the **deliverables list (Section 6.6)** current (status + acceptance).
- Record changes through versioning and a short change log.
- Keep the ID readable; do not copy large detailed artifacts into it.
- If content becomes large, highly detailed, or technical in nature, create a **separate dedicated artifact** for that content and reference (link) it from the appropriate section of the ID instead of embedding it directly.

## 5. Level of Detail

The governing principle for the ID is:

> Include enough information to make a sound decision and to understand what is happening in the initiative — and create or reference separate artifacts for detailed content.

The ID should allow a reader to:

- Understand the purpose and value of the initiative
- Understand what is in scope and out of scope
- Understand what must be delivered and who must accept it
- Understand the major cost, risk, and operational implications

If additional detail is required to design, build, test, operate, or govern the initiative, that detail should exist in a **separate artifact**, with the ID referencing it where appropriate.

### At authorization time

The ID must contain enough clarity to:

- Support an informed approval decision
- Confirm scope boundaries
- Confirm ownership and acceptance structure
- Confirm financial and risk exposure at approval level

### During delivery

The ID must remain understandable without becoming a design document. It should:

- Be updated to reflect current scope and deliverable status
- Add clarifying detail only when needed for understanding
- Reference detailed artifacts rather than embedding them

### Appropriate content in the ID

- Clear outcomes and success measures
- Clear scope boundaries (in / out)
- Named owners, decision makers, and Acceptance Authorities
- Major impacts such as financial (CapEx/OpEx) and regulatory impacts
- Risks, dependencies, and feasibility summary
- Deliverables aligned to the Standard Deliverables Reference

### Content that belongs in separate artifacts

- Detailed architecture and configuration unless it fits in one page
- Playbooks and SOPs
- Task plans / sprint plans
- Detailed test scripts
- Technical specifications beyond what is needed to understand scope or risk

## 6. Recommended Document Structure

### 6.1 Document Control

**Must include:**

- Initiative name
- Initiative/Project ID
- Version, status (Draft / Active / Final)
- Last updated date
- Owners (Outcome Owner, Delivery Owner)
- Sponsor / Sponsoring Body (the person or organizational unit sponsoring the initiative and accountable for ensuring the initiative remains supported)
- Decision Authorities (list of individuals and/or committees who make final decisions within this initiative, and the level/type of decision each is authorized to make)
- Authorization (who granted authority to proceed with the initiative and reference to the formal record of that authorization, e.g., minutes, resolution, or decision record)
- Change log (short summary of what changed by version)

### 6.2 Executive Summary

**Purpose:** Make the initiative understandable in 2–3 minutes.

**Must include:**

- Plain-language description
- Why now (driver)
- Expected outcomes (what will change)
- What will be delivered (high-level)
- Estimated one-time cost (CapEx) and ongoing annual operating cost (OpEx)
- Approved budget and current expenditure status (budget vs. actual to date, including variance if applicable)

### 6.3 Business Need and Rationale

**Must include:**

- Current situation and pain points
- Who is impacted
- Cost of inaction

### 6.4 Outcomes and Success Measures

**Must include:**

- Outcome statement(s)
- Measurable success criteria
- What is explicitly *not* a success criterion

### 6.5 Scope Boundaries

**Must include:**

- In-scope list
- Out-of-scope list
- Assumptions
- Key constraints (technical, financial, regulatory, policy, timeline, platform, or organizational constraints that limit scope or solution options)

If functional scope is material to understanding the initiative, include either:

- A concise summary of **Functional Capabilities (what the solution must be able to do)**, or
- A reference to the Functional Capabilities deliverable defined in Section 6.6.

Scope Boundaries define the limits of the initiative. Detailed functional definition through Functional Capabilities deliverable should be managed as a deliverable.

### 6.6 Deliverables

**Purpose:** Define what will be produced, who is responsible for delivering it, and who must accept it.

It is recommended to organize deliverables by **Deliverable Domains**. For smaller initiatives, a single consolidated deliverables list is acceptable.

Deliverables may be selected from the Standard Deliverables Reference or created where appropriate.

The ID is the authoritative definition of what is being delivered.

**Recommended information for each deliverable:**

- Deliverable name and brief description
- Named **Delivery Owner** (accountable for producing the deliverable)
- Named **Acceptance Authority** (accountable for final sign-off)
- Acceptance focus (what matters for sign-off)
- Current status (Planned / In Progress / Delivered / Accepted)

**When applicable, also include:**

- Reference (link) to the delivered artifact when delivered
- Reference (link) to supporting evidence
- Reference (link) to the acceptance record
- Acceptance date

**Control rule:** A deliverable is only “Accepted” when the named Acceptance Authority has formally confirmed that the acceptance focus has been met.

### 6.7 Service Operations & Support Model (Required When a Service/System Is Impacted)

**Purpose:** Define the minimum operations and support expectations so the initiative can be run after delivery.

**This is part of the Operational Readiness deliverable domain.** This section exists to provide a summary of operations and support expectations.

**Recommended information:**

- Operational (Run) Owner and Support Owner
- Support tier model (L1/L2/L3) and escalation path (conceptual)
- Monitoring and recovery intent (conceptual)
- **Estimated ongoing OpEx impact**:
  - Recurring technology costs (licenses, hosting, tools)
  - Support labor impact (approximate additional hours)
  - Total estimated annual OpEx (range acceptable)
  - Confidence level (Low/Medium/High)

### 6.8 Related Resources & References

**Purpose:** Provide references to initiative-relevant context that is not itself a deliverable artifact.

**May include (as applicable):**

- Opportunity Assessment document(s) and supporting analysis
- Strategic or policy references relevant to this initiative
- Standards used
- Vendor documentation, contracts, or licensing references
- Related initiatives or dependencies
- Known constraints with reference links

## 7. Lifecycle of the ID

### Stage 1 — Opportunity Assessment&#x20;

- ID not created yet.
- Inputs are captured in the opportunity assessment material.

### Stage 2 — Definition

- Create the ID based on the Opportunity Assessment material.
- Identify Outcome Owner, Delivery Owner, Sponsor, Decision Authorities, required level of authorization (Personal/Departmental/Committee/Organization), and the authorization record (email, committee action, resolution, contract, etc.)
- Define outcomes, scope boundaries, owners, and deliverable domains.
- Identify required deliverables using the Standard Deliverables Reference and define new ones as appropriate.
- For each deliverable, identify Delivery Owners, Acceptance Authorities and document acceptance focus.
- Finalize the ID for authorization review (status remains **Draft** until authorized).

### Stage 3 — Decision / Authorization&#x20;

- The Draft ID is used to support the authorization decision.
- Once formally authorized, update status to **Active**.
- After authorization, the ID becomes the controlled reference for the initiative and must follow the Change Rule (Section 8) for material changes.

### Stage 4 — Detailed Design and Planning&#x20;

- Update the ID only to improve clarity, confirm deliverables, and maintain current status.
- Do not change outcomes/scope unless handled through the change rule.

### Stage 5 — Mobilization&#x20;

- Confirm the delivery approach and working rhythm for execution.
- Confirm that deliverables, owners, and acceptance authorities remain current in the ID.
- Confirm delivery team understands what needs to be delivered.

### Stage 6 — Delivery and Execution

- Keep Section 6.6 current:
  - Update deliverable status
  - Add references (links) to delivered artifacts, evidence, and acceptance records as they become available

### Stage 7 — Acceptance and Closure&#x20;

- Ensure deliverables show accepted status and acceptance dates.
- Ensure Acceptance Authorities and ownership are clearly recorded.
- Confirm final budget vs. actual financial summary.
- Update status to Final.

## 8. Change Rule

Changes that alter outcomes, scope boundaries, deliverable domains, Acceptance Authorities, or major cost/risk must:

1. Be recorded as a change to the ID (new version)
2. Be reviewed by the relevant owners
3. Be re-authorized if material

## 9. Minimal Template (Copy/Paste Outline)

1. Document Control
2. Executive Summary
3. Business Need and Rationale
4. Outcomes and Success Measures
5. Scope Boundaries
6. Deliverables (by domain or consolidated list)
7. Service Operations & Support Model (if needed)
8. Related Resources & References

---

# Appendix A — Quality & Completeness Checklist

The following questions are provided as a **recommended self-check** to assess the quality and completeness of the ID.

### Understanding and purpose

1. Can a new reader explain what the initiative is and why it exists after reading Sections 6.2–6.4?
2. Are the intended outcomes and success measures clearly stated (and measurable)?

### Scope and accountability

3. Are in-scope and out-of-scope boundaries explicit and unambiguous?
4. Do Outcome Owner, Delivery Owner, and Decision Authorities exist and are they named?

### Deliverables and acceptance

5. Are all deliverables clearly listed in the ID (either organized by domain or as a consolidated list)?
6. Does each deliverable have a named Delivery Owner and Acceptance Authority?
7. Is the acceptance focus for each deliverable clearly defined?
8. If deliverable domains are used, are they clearly defined and appropriate for the initiative?

### Living document expectations

9. For each listed deliverable, does a current status exist (Planned / In Progress / Delivered / Accepted)?
10. Where a deliverable is delivered, does a reference (link) to the delivered artifact exist under that deliverable entry?
11. Where evidence is required, does evidence exist and is it referenced under the deliverable entry?
12. Where a deliverable is accepted, does an acceptance record exist and is it referenced (with acceptance date recorded)?
13. Is the ID current (last updated date reflects recent progress) and does the change log reflect material updates?

### Operational and financial viability (when applicable)

14. If the initiative impacts a service/system, do Support Owner and Operational (Run) Owner exist and is OpEx impact estimated (SOSM under Operational Readiness)?
15. Does the Governance & Control domain include approval-level CapEx/OpEx, approved budget, current expenditure (actuals), variance summary, and a risk/feasibility summary?

### Change control

16. Are material changes handled via the change rule (Section 8), with re-authorization when required?





