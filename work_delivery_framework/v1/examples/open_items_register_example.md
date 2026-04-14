# Open Items Register Example

This example shows how the status values are used across the lifecycle:

- `open` for an item that is known and assigned but not yet materially worked
- `in progress` for an item being actively worked
- `monitoring` for an unresolved item being watched as the chosen treatment
- `resolved` for an item dealt with in substance but awaiting final confirmation or closure
- `closed` for an item that no longer needs action, monitoring, or decision

| Entry ID | Type | Title | Description | Owner | Status | Affected stage or gate | Impact summary | Next action | Target resolution or decision date | Created date | Last updated date | Resolution note | Origin reference |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| OIR-001 | dependency | Identity provider integration details missing | Final claims mapping from the enterprise identity provider is still unknown. | Security Lead | in progress | Gate 4 | Access model cannot be finalized until claims mapping is confirmed. | Confirm mapping with IAM team and update Access Model. | 2026-04-21 | 2026-04-14 | | |
| OIR-002 | blocker | Acceptance owner not yet named | The business area has not yet assigned the named Acceptance Owner required for Gate 4 and Gate 6. | Delivery Owner | open | Gate 4 | Gate passage cannot proceed without a named Acceptance Owner. | Escalate to sponsor for owner assignment. | 2026-04-16 | 2026-04-14 | | OIR-003 |
| OIR-003 | risk | Procurement lead time may delay production environment setup | Firewall change approval may take longer than the current planning assumption. | Infrastructure Lead | monitoring | Gate 5 | MVP release timing could slip if approval times worsen. | Review approval status at weekly delivery checkpoint and escalate if no movement by 2026-04-19. | 2026-04-19 | 2026-04-14 | | |
| OIR-004 | issue | Data retention rule clarified with records team | The required retention period was unclear, but the records team has confirmed the policy and the Data Asset Specification is being updated. | Data Lead | resolved | Gate 4 | Specification wording can now be finalized, but the register entry remains open until the update is checked and referenced. | Confirm the updated Data Asset Specification is published and linked. | 2026-04-17 | 2026-04-15 | Retention policy confirmed with records team; waiting for specification update and reference link before closure. | |
| OIR-005 | assumption | Existing reporting feed can be retired after cutover | The assumption was validated during transition planning and no further action is required. | Reporting Lead | closed | Gate 7 | None after transition confirmation. | None. | 2026-04-10 | 2026-04-15 | Transition review confirmed the legacy reporting feed can be retired without downstream impact. | |
