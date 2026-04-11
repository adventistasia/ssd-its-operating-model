# SSD Staff Itinerary Tracker Stress Test Scenario 02

Status: working draft
Purpose: preserve the original request context used for this simulation exercise.

## 1. Exercise intent

This folder simulates how a Delivery Owner / Project Manager might use the repository's governed [work_delivery](../work_delivery) framework in real time for a small office solution request that turns out to be more governed than it first looks.

The exercise is intentionally practical rather than idealized. It is designed to surface:

- whether the framework makes the next step clear
- whether the work should stay as a Work Brief or escalate
- whether ownership and acceptance can be named in practice
- whether the required artifact set stays proportionate for a medium-complexity request
- where the framework creates friction, ambiguity, or helpful structure

## 2. Original request

Request title: Create a staff itinerary tracker for SSD

Requestor: Jane, Administrative Assistant / Secretary

Problem statement provided:

- Office staff cannot easily tell whether a staff member is on an approved itinerary.
- Office staff cannot easily tell whether a staff member is on leave or vacation.
- Office staff cannot easily tell whether a staff member is expected to be in the office.
- This causes confusion, delays, repeated follow-up, and poor meeting planning.

## 3. Requested business outcome

Jane wants a simple, low-maintenance, trustworthy tracker where office staff can quickly check whether a staff member is:

- on an approved itinerary
- on leave or vacation
- expected to be in the office

The tracker should ideally help answer:

1. Is this staff member on an approved itinerary?
2. Is this staff member on leave or vacation?
3. Is this staff member expected to be in the office?
4. When is the next known office date or return date?
5. Is the displayed status based on the latest approved record?

## 4. Why this scenario is intentionally medium complexity

The request is still small in visible footprint, but the control questions are no longer small:

- itinerary approvals are formal and controlled
- leave data is owned by HR
- revision handling matters
- one trustworthy view is required without duplicate encoding
- the answer has to be visible enough to support office coordination and governance

That makes this a useful test of whether the framework can escalate cleanly without turning every request into a full project pack.

## 5. Personas used in the simulation

- Jane, Administrative Assistant / requestor
- Angie, sponsor and office operations decision-maker
- Delivery Owner / Project Manager
- Programmer / Technical SME
- Committee Secretary, owner of formal itinerary approvals
- HR Leave Records Owner, owner of leave status data
- Data Steward / Records Custodian, governance owner for traceability and retention
- IT Service Owner / Support Lead, support owner for the live solution

## 6. Governing rule for this exercise

The Delivery Owner must not assume the path in advance. The Delivery Owner must use the framework as written, starting from the repository's source guidance and then deciding:

- what stage the work appears to be in
- whether the work should proceed
- whether the work is small enough for a Work Brief or needs a fuller definition set
- which domains and artifacts are actually needed
- what is still blocked by missing ownership, source-of-truth, or acceptance decisions

## 7. Important simulation note

Nothing in this folder is an actual approval, authorization, or acceptance record for live work.

Where decisions are shown, they are simulated scenario outputs used to test the framework's usability.
