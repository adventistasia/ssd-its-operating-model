# Audit & Monitoring Design Summary Specification

## 1. What This Artifact Is For

The Audit & Monitoring Design Summary describes how key actions, states, and exceptions within the solution are logged, monitored, reviewed, and escalated.

It exists to support accountability, forensic reconstruction, and operational response without becoming a full SIEM implementation guide. A useful summary tells reviewers what events matter, how they become visible, who acts on them, and what limitations remain.

The intended outcome is that material events and exceptions are visible early enough to support accountability, investigation, response, and ongoing operational oversight.

Intended readers include: security reviewers, IT Operations / Service Owner, support and monitoring teams, audit reviewers, and Delivery Owner.

## 2. When to Use It

This artifact is required when the solution handles sensitive data, privileged actions, important approvals, material operational events, or compliance-relevant transactions.

Use this artifact before go-live and during control review. It is most useful where important events must be traceable and where monitoring or alerting needs to support detection, review, and response.

It should align with NIST SP 800-53 audit and accountability expectations, NIST CSF Detect and Respond outcomes, CIS Control 8 on audit log management, and ITIL 4 Monitoring and Event Management practice.

## 3. Stage Fit and Handoffs

Usually elaborated in Stage 4, operationalized in Stage 5 and Stage 6, and referenced in Stage 7 to confirm traceability and supportability controls are in place.

Upstream inputs:

- [Access Control & Authorization Model Specification](access_control_and_authorization_model_specification.md)
- [Security & Privacy Risk Assessment Specification](security_and_privacy_risk_assessment_specification.md)
- [Technical Design Document Specification](../operational_readiness_deliverables/technical_design_document_specification.md)

Downstream outputs inform:

- [Operations & Support Model Specification](../operational_readiness_deliverables/operations_and_support_model_specification.md)
- [Compliance & Regulatory Alignment Statement Specification](compliance_and_regulatory_alignment_statement_specification.md)
- [Operational Readiness Confirmation Record Specification](../operational_readiness_deliverables/operational_readiness_confirmation_record_specification.md)

## 4. Before You Start

Before drafting, confirm you have:

- confirmed solution scope
- known sensitive data, privileged actions, and compliance obligations
- identified monitoring or alerting tools
- named security lead and operations team
- understanding of log retention obligations or SIEM tooling

## 5. How to Draft It

1. Define scope and purpose — identify the solution, coverage scope, date, and owner (from 6.1).
2. Identify events and actions that must be visible — name key actions, events, or conditions that must be logged or monitored and why they matter (from 6.2).
3. Define review, alerting, and response expectations — specify what triggers alerts or review, who responds, escalation paths, and any known limitations (from 6.3).
4. Document evidence and retention notes — record authoritative log sources, traceability expectations, and retention or custody considerations (from 6.4).
5. Populate the summary table — complete the event-visibility table using the recommended column structure (from 6.5).

## 6. Minimum Structure

### 6.1. Scope and Purpose

Must include:

- solution or service name
- scope of monitoring and audit coverage
- date or version
- owner

This section identifies what the summary covers.

### 6.2. Events and Actions That Must Be Visible

Must include:

- key actions, events, or conditions that must be logged or monitored
- why those items matter

This section defines the high-value visibility requirements.

### 6.3. Review, Alerting, and Response Expectations

Must include:

- what should trigger alerting or review
- who reviews or responds
- escalation expectations where relevant
- any coverage limitations, response dependencies, or known blind spots that materially affect detection confidence

This section connects visibility to operational action.

### 6.4. Evidence and Retention Notes

Must include where relevant:

- authoritative log sources or systems
- traceability expectations
- retention or evidence considerations that materially affect auditability
- ownership or custody expectations for retained evidence where that affects investigation or compliance handling

This section shows how the information remains usable for later investigation or review.

### 6.5. Template Guide

Recommended summary columns:

| Event or action | Why it matters | Logged or monitored where | Review or alert expectation | Owner |
| --- | --- | --- | --- | --- |

Use short, high-value entries. Do not list every low-level technical event.

## 7. Writing Rules

Include enough detail to explain which events matter, what must be logged, how alerts or reviews happen, who responds, and how traceability is maintained. Do not turn it into a full tool configuration manual.

Keep the following out of this artifact:

- every low-value technical event
- full SIEM rule bodies unless they are the approved design artifact
- vague statements such as "logging enabled" without defining what matters

## 8. Traceability, Ownership, and Review

The security lead, monitoring lead, or solution lead usually authors the summary.

Review should include operations and any team that will receive or respond to alerts.

The Delivery Owner is accountable for ensuring monitoring and alert-response responsibilities are explicit before go-live. The relevant Acceptance Authority should confirm that monitoring coverage and ownership are sufficient for operational support and auditability.

## 9. Maintenance Expectations

Update when monitored events, alert logic, retention needs, or response ownership change.

## 10. Done When

- The important actions and events are clearly identified.
- A reviewer can tell how sensitive or high-risk activity becomes visible.
- Escalation and review responsibilities are clear.
- Any material limitations or blind spots are explicit rather than implied.
- The summary stays focused on high-value audit and monitoring expectations.

## 11. What Comes Next

1. Review with operations and alert-response teams before go-live.
2. Confirm alignment with [Access Control & Authorization Model Specification](access_control_and_authorization_model_specification.md) and [Security & Privacy Risk Assessment Specification](security_and_privacy_risk_assessment_specification.md).
3. Reference in [Operational Readiness Confirmation Record Specification](../operational_readiness_deliverables/operational_readiness_confirmation_record_specification.md).

## 12. Prompt Guide

### 12.1. Starter Prompt

```
Draft an Audit & Monitoring Design Summary for this solution.
Identify the actions and events that must be logged or monitored, the expected review or alerting behavior, who responds, and any traceability or retention requirements that materially affect control review.
Keep it summary-level and high-value.
```

### 12.2. Validation Prompt

```
Review this Audit & Monitoring Design Summary.
Check that important events are identified, review and response ownership is clear, any material limitations or blind spots are stated, and the summary table is populated with high-value entries.
Flag any vague logging statements, missing response owners, or low-value noise that should be removed.
```
