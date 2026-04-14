# Access Model Specification

## 1. Purpose

The `Access Model` defines the intended access-control model, role boundaries, and related lifecycle expectations for secure operation.

## 2. When Required

Required when the initiative has security or compliance impact.

## 3. Required By

Gate 4: `Specification Complete`

## 4. Required Contents

1. roles and permissions model
2. authentication and authorization expectations
3. provisioning and deprovisioning where applicable
4. audit and logging expectations where applicable

## 5. Completeness Rules

The model is complete when:

1. access expectations are explicit enough to understand who can do what
2. lifecycle expectations for access governance are visible
3. the model aligns with user roles, security expectations, and operational ownership elsewhere

## 6. Common Failure Conditions

1. material role, permission, or lifecycle gaps remain unresolved
2. authentication or authorization assumptions conflict with other artifacts

## 7. Related Files

1. `../templates/access_model_template.md`
