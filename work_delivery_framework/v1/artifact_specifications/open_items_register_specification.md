# Open Items Register Specification

## 1. Purpose

The `Open Items Register` is the canonical initiative-level register for blockers, risks, issues, assumptions, and dependencies.

## 2. When Required

Always required for every initiative.

## 3. Required By

Must exist no later than Gate 2.

It remains a persistent critical artifact from Gate 2 through Gate 8.

## 4. Required Structure

The register must use one table or equivalent single-register structure.

Allowed entry types are:

1. blocker
2. risk
3. issue
4. assumption
5. dependency

Allowed statuses are:

1. open
2. in progress
3. monitoring
4. resolved
5. closed

Status meanings and usage are:

1. `open` - the item has been identified, recorded, and assigned, but active response work has not yet materially started. Use this when the item is known and owned, but the next action has not yet begun in substance.
2. `in progress` - active work is underway to resolve, reduce, clarify, or decide the item. Use this when someone is currently working the item rather than only tracking it.
3. `monitoring` - the item remains unresolved, but observation is the chosen control strategy for now. Use this only when watchful observation is the intentional treatment; it is not the default state for unresolved items.
4. `resolved` - the underlying condition has been dealt with in substance, but formal confirmation or closure is still pending where required. Use this when the practical issue is addressed, but the register entry is not yet ready to be fully closed.
5. `closed` - the item has completed its lifecycle in the register and requires no further action, monitoring, or decision. Use this when any required confirmation is complete and the entry no longer needs active management.

## 5. Minimum Entry Fields

1. entry ID
2. entry type
3. title
4. description
5. owner
6. status
7. affected stage or gate
8. impact summary
9. next action
10. target resolution or decision date
11. created date
12. last updated date
13. resolution note when resolved or closed
14. origin reference when a blocker arose from another open item

## 6. Completeness Rules

The register is complete when:

1. it exists even if there are few entries
2. every open item is specific enough to support gate review
3. no open blocker affecting the current gate remains at gate passage
4. any remaining open non-blocker item is explicitly owned, actionable, and controlled
5. status values are used consistently so reviewers can distinguish newly logged items, actively worked items, monitored items, substantively resolved items, and fully closed items

## 7. Common Failure Conditions

1. unresolved items are tracked in local notes instead of the canonical register
2. entries omit ownership, impact, or next action
3. gate-disqualifying items remain misclassified as non-blockers

## 8. Related Files

1. `../templates/open_items_register_template.md`
2. `../examples/open_items_register_example.md`
