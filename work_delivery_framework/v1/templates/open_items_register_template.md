# Open Items Register

## 1. Usage Note

Use this as the single canonical register for blockers, risks, issues, assumptions, and dependencies.

## 2. Register Entries

Use these statuses consistently:

1. `open` - identified, recorded, and assigned, but active response has not yet materially started
2. `in progress` - active work is underway to resolve, reduce, clarify, or decide the item
3. `monitoring` - the item remains unresolved, but observation is the chosen control strategy for now
4. `resolved` - the underlying condition has been dealt with in substance, but formal confirmation or closure is still pending
5. `closed` - the item has completed its lifecycle in the register and requires no further action, monitoring, or decision

| Entry ID | Type | Title | Description | Owner | Status | Affected stage or gate | Impact summary | Next action | Target resolution or decision date | Created date | Last updated date | Resolution note | Origin reference |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| OIR-001 | blocker / risk / issue / assumption / dependency | | | | open / in progress / monitoring / resolved / closed | | | | | | | | |

## 3. Rules

1. Any open `blocker` affecting the current gate forces gate failure.
2. Use `Origin reference` when a blocker arose from another open item.
3. Use `Resolution note` when status is `resolved` or `closed`.
4. Do not use `monitoring` as a passive placeholder. Use it only when observation is the deliberate current treatment.
5. Move an item to `closed` only after any required confirmation, decision, or administrative follow-through is complete.
