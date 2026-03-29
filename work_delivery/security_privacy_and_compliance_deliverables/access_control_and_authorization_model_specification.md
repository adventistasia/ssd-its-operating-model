# Access Control & Authorization Model Specification

## 1. What This Artifact Is For

The Access Control & Authorization Model defines how access to the solution is granted, restricted, reviewed, and governed.

It exists to make access decisions intentional, reviewable, and aligned with role responsibilities and risk. A useful model supports least privilege, separation of duties, and accountable access lifecycle management.

The intended outcome is that access remains deliberately controlled, appropriately limited, and reviewable across the full user lifecycle, with clear accountability for privileged and sensitive access.

Intended readers include:

- Security / Data Protection Officer
- Business Owner / Process Owner
- identity and access administrators
- Delivery Owner and solution leads
- audit reviewers

## 2. When to Use It

This artifact is required when the solution has role-based access, privileged functions, sensitive data, approval authority, or integration with identity systems.

Use this artifact before implementation is finalized and before access is provisioned in production. It is most useful where access rights, privileged functions, review controls, and identity assumptions must be explicit and defensible.

It should align with NIST SP 800-53 access-control expectations, NIST SP 800-63 identity guidance where relevant, and CIS Control 6 on access control management.

## 3. Stage Fit and Handoffs

Identified in Stage 2 where access boundaries affect authorization decisions, elaborated in Stage 4, validated in Stage 6, and referenced during Stage 7 acceptance and operational handover.

Upstream inputs:

- [Functional Capabilities Specification](../solution_deliverables/functional_capabilities_specification.md)
- [User Roles, Personas & Access Model Specification](../solution_deliverables/user_roles_personas_and_access_model_specification.md)
- [Security & Privacy Risk Assessment Specification](security_and_privacy_risk_assessment_specification.md)

Downstream outputs inform:

- [Audit & Monitoring Design Summary Specification](audit_and_monitoring_design_summary_specification.md)
- [DevOps Guide Specification](../operational_readiness_deliverables/devops_guide_specification.md)
- [Operations & Support Model Specification](../operational_readiness_deliverables/operations_and_support_model_specification.md)

Also relates to:

- [Use Case Narratives Specification](../solution_deliverables/use_case_narratives_specification.md)

## 4. Before You Start

Before drafting, confirm you have:

- approved solution scope and functional capabilities
- User Roles and Personas model or equivalent
- known privileged functions, sensitive data categories, and identity system constraints
- named security lead and Delivery Owner
- understanding of integration with identity platforms or directories

## 5. How to Draft It

1. Define access model context — identify the solution, scope, date, and owner (from 6.1).
2. Structure roles and authorization — define roles or groupings, what each may do, and what each must not do (from 6.2).
3. Define privileged and sensitive access treatment — identify elevated access cases and apply stronger controls and separation-of-duties expectations (from 6.3).
4. Specify access lifecycle controls — document provisioning, change, review, and de-provisioning expectations including non-human and service access (from 6.4).
5. Populate the summary table — complete the role-permission table using the recommended column structure (from 6.5).
6. Review for least-privilege, separation-of-duties gaps, and missing lifecycle controls.

## 6. Minimum Structure

### 6.1. Access Model Context

Must include:

- solution or service name
- scope of the access model
- date or version
- owner

This section identifies what environment and functionality the model covers.

### 6.2. Role and Authorization Structure

Must include:

- roles or authorization groupings
- what each role is allowed to do
- what each role must not do where restriction is material

This section defines the core authorization model.

### 6.3. Privileged and Sensitive Access Treatment

Must include:

- privileged access cases
- stronger controls for elevated access where needed
- separation-of-duties assumptions where relevant
- emergency, temporary, or break-glass access handling where such access is possible

This section helps protect high-risk actions from casual or ambiguous handling.

### 6.4. Access Lifecycle Controls

Must include:

- provisioning expectations
- change or approval expectations
- periodic review expectations
- de-provisioning expectations
- treatment of non-human, shared, or service access where those access paths exist

This section makes access governance operational rather than theoretical.

### 6.5. Template Guide

Recommended summary columns:

| Role or access group | Allowed actions | Restricted actions | Approval basis | Review expectation | Notes |
| --- | --- | --- | --- | --- | --- |

Use references for platform-specific implementation detail rather than embedding it here.

## 7. Writing Rules

Include enough detail to explain access roles, authorization rules, privileged access treatment, account lifecycle expectations, and review controls. Do not turn it into a directory configuration manual.

Keep the following out of this artifact:

- raw user account lists unless the artifact is explicitly a controlled access register
- secrets or credential values
- implementation-specific group syntax that belongs in technical administration records

## 8. Traceability, Ownership, and Review

The security lead, identity lead, or solution lead usually prepares this artifact with business owner input.

It should be reviewed by the Security / Data Protection Officer and relevant role owners.

The Delivery Owner is accountable for making sure the approved access model is reflected in delivery outputs and support handover. The relevant Acceptance Authority should confirm that high-risk access controls are in place before final acceptance.

## 9. Maintenance Expectations

Update when roles, privileges, approval logic, identity integration, or review requirements change materially.

## 10. Validation Guide

- Is it clear who can do what and under what approval basis?
- Are privileged and sensitive actions handled more strictly where needed?
- Are emergency, temporary, and non-human access paths governed clearly enough for audit and control review?
- Are provisioning and removal expectations visible?
- Does the artifact support review and audit rather than just initial setup?

If weak, clarify the permission model and make lifecycle controls more explicit.

## 11. Done When

- Access model context and scope are documented.
- Roles and authorization groupings are defined with allowed and restricted actions.
- Privileged access is given stronger controls.
- Access lifecycle (provision, review, de-provision) is specified.
- Summary table is populated.
- Reviewed by Security / Data Protection Officer and relevant role owners.

## 12. What Comes Next

1. Review with Security / Data Protection Officer and identity administrators before production access provisioning.
2. Reference in [DevOps Guide Specification](../operational_readiness_deliverables/devops_guide_specification.md) and [Operations & Support Model Specification](../operational_readiness_deliverables/operations_and_support_model_specification.md) for operational access handling.
3. Confirm alignment with [Audit & Monitoring Design Summary Specification](audit_and_monitoring_design_summary_specification.md).
4. Update before acceptance and handover as part of Stage 7.

## 13. Prompt Guide

### 13.1. Starter Prompt

```
Draft an Access Control & Authorization Model for this solution.
Define roles, permissions, restricted actions, privileged access rules, separation-of-duties assumptions, and how access is approved, reviewed, and revoked.
Keep it governance-focused and implementation-light.
```

### 13.2. Validation Prompt

```
Review this Access Control & Authorization Model.
Check that each role has clear allowed and restricted actions, privileged access is handled with stronger controls, access lifecycle (provision, review, de-provision) is specified, and the summary table is complete.
Flag any least-privilege gaps, missing separation-of-duties assumptions, or unclear lifecycle controls.
```
