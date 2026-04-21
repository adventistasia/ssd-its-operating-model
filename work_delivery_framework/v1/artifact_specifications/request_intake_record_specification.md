# Request Intake Record Specification

## 1. Purpose

The `Request Intake Record` is the lightweight intake and assessment record used to capture the minimum information needed to decide whether a request is a qualified framework candidate.

## 2. When Required

Always required for in-scope candidate work.

## 3. Required By

Gate 1: `Qualified Request`

## 4. Required Contents

1. requester name
2. background, problem, or opportunity
3. desired outcome
4. success measures, with `Unknown` explicitly allowed at entry
5. affected systems or processes, with `Unknown` explicitly allowed at entry
6. triage owner
7. initial in-scope or out-of-scope assessment
8. initial known unknowns, dependencies, or blockers

## 5. Completeness Rules

The record is complete when:

1. the request can be understood without relying on informal conversation
2. ownership is explicit
3. the initial scope judgment is visible
4. known unknowns are visible enough to support qualification, rejection, or clarification

## 6. Common Failure Conditions

1. the request can only be understood from meeting context
2. requester or triage owner is missing
3. scope qualification is implied rather than explicit
4. the record hides important unknowns that affect qualification

## 7. Related Files

1. `../templates/request_intake_record_template.md`
2. `../machine_readable/artifacts.yaml`
