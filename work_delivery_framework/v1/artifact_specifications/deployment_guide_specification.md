# Deployment Guide Specification

## 1. Purpose

The `Deployment Guide` is the operational deployment and recovery artifact that enables controlled release, validation, rollback, and support handoff.

## 2. When Required

Required when the initiative has material ops or support impact.

## 3. Required By

Gate 6: `All Deliverables Accepted`

It may remain gate-critical at Gate 7 where supported operation depends on it.

## 4. Required Contents

1. deployment steps and prerequisites
2. environments and configuration expectations
3. rollback or recovery approach
4. operational validation steps
5. monitoring and support handover notes where applicable
6. support ownership
7. observability plan
8. maintainability commitments
9. transition checklist

## 5. Completeness Rules

The guide is complete when:

1. a qualified operator can deploy, validate, and recover the solution in the intended environments
2. release and support steps are explicit enough to establish supported operating state
3. operational ownership and observability are visible enough for transition acceptance

## 6. Common Failure Conditions

1. deployment or rollback depends on undocumented knowledge
2. operational validation or handover expectations are too vague to support transition
3. support ownership is absent or unclear

## 7. Related Files

1. `../templates/deployment_guide_template.md`
