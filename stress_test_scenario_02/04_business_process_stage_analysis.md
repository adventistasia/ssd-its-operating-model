# Business Process Stage Analysis

Status: working draft
Stage: Stage 1 - Work Assessment
Specification used: [Business Process Stage Analysis Specification](../work_delivery/work_assessment/business_process_stage_analysis_specification.md)

## 1. Process boundary

This analysis covers the current staff availability visibility path that office staff use when they need to know whether a person is away on itinerary, away on leave, or expected in office.

It does not redesign the underlying approval processes. It only makes the current flow visible enough that later definition does not have to rediscover it from scratch.

## 2. Current process stages

| Stage | Main actor | Input | Output | Control or handoff issue |
| --- | --- | --- | --- | --- |
| Itinerary request and approval | Traveler, Committee Secretary | Travel request, supporting approval information | Approved itinerary record | Approval is formal, but the record is not easy for office staff to consume directly |
| Leave request and approval | Staff member, HR Leave Records Owner | Leave request and HR rules | Approved leave record | Leave is controlled by HR and cannot be casually duplicated into another team record |
| Office coordination lookup | Jane and other office staff | Questions about current availability | Informal answer or manual reconstruction | People rely on chats, email, and memory because no single trusted view exists |
| Revision handling | Traveler, Committee Secretary | Change to itinerary | Revised approved itinerary record | Revision history is easy to lose or overwrite in informal summaries |
| Status display / consumption | Office staff | Current approved itinerary and leave signals | Combined availability view or manual judgment | The combined answer is currently reconstructed instead of governed |

## 3. Material bottlenecks and control gaps

- office staff need a combined answer, but the underlying sources have different owners
- itinerary approval and leave approval are separate control paths
- revision history matters because "latest approved" is part of the business question
- the current process encourages informal parallel views
- no one owns the combined visibility outcome today

## 4. Why the process matters to the delivery decision

The process analysis shows that the work is not just a list or dashboard.

The solution has to respect:

- formal itinerary approval ownership
- HR ownership of leave data
- a visible revision trail
- a single trustworthy view without duplicate encoding

That is why the Delivery Owner started to lean toward a fuller Stage 2 baseline instead of a Work Brief.
