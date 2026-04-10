# SSD Staff Itinerary Tracker Stress Test Scenario 01

Status: working draft  
Purpose: preserve the original request context used for this governed work-delivery simulation.

## 1. Exercise intent

This folder simulates how a Delivery Owner / Project Manager would use the repository's [Work Delivery Framework](../work_delivery/work_delivery_framework.md) in real time for a small but control-sensitive office request.

The exercise is intentionally practical. It is meant to test whether the framework:

- makes the next step clear without pre-deciding the lifecycle
- keeps the path proportionate when the work is small
- surfaces ownership, source-of-truth, and acceptance issues early
- avoids forcing a full initiative pack when a lighter governed path is enough
- still makes the work supportable and traceable

## 2. Original request

Request title: create a staff itinerary tracker for SSD

Requestor: Jane, Administrative Assistant / Secretary

Problem statement provided by Jane:

- office staff cannot easily tell whether a staff member is on an approved itinerary
- office staff cannot easily tell whether a staff member is on leave or vacation
- office staff cannot easily tell whether a staff member is expected in the office
- people keep asking around, which causes confusion and delays

## 3. Real-world context that emerged early

- approved itinerary records already exist and are kept by a committee secretary
- leave records are held elsewhere and are not owned by the same person or function
- the sponsor is skeptical of overbuilding and wants a proportionate answer
- the request appears small in delivery size, but not small in authority clarity

## 4. Requested business outcome

Jane wants a simple, low-maintenance, trustworthy tracker where office staff can quickly check whether a staff member is:

- on an approved itinerary
- on leave or vacation
- expected in the office

The tracker should ideally answer:

1. Is this staff member on an approved itinerary?
2. Is this staff member on leave or vacation?
3. Is this staff member expected in the office?
4. When is the next known office date or return date?
5. Is the displayed status based on the latest approved record?

## 5. Minimum participants in the simulation

- Delivery Owner / Project Manager
- Angie the Sponsor
- Jane the Requestor
- Programmer / Technical SME

## 6. Additional stakeholders that emerged

The simulation also surfaced additional stakeholders that cannot stay hidden if the work is to stay governable. Their roles are defined in [10_additional_stakeholders_discovered.md](10_additional_stakeholders_discovered.md).

## 7. Governing rule for this exercise

The Delivery Owner must not assume the path in advance. The framework must be read as written, and the path must be decided in real time from the current facts.

That means the simulation must determine:

- what stage the work appears to be in
- whether the work should proceed
- whether the work is small enough for a [Work Brief](../work_delivery/work_brief/work_brief_specification.md)
- which deliverable domains are actually in scope
- what is still blocked by missing ownership, source-of-truth, or acceptance decisions

## 8. Important simulation note

Nothing in this folder is an actual approval, authorization, acceptance, or deployment record for live work.

Where decisions are shown, they are simulated scenario outputs used to test the framework's usefulness, proportion, and friction.
