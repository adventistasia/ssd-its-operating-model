# Solution Modules Specification

## 1. Purpose

Define what Solution Modules are, how they are formed from approved Functional Capabilities, and how they are used during delivery.

Solution Modules group approved capabilities into clear, testable units that can be built, deployed, and accepted.

Modules may be outlined during Stage 2 to support authorization decisions and refined in Stage 4 without changing approved Functional Capabilities.

This document:

- Does not add new scope.
- Does not change Capability IDs.
- Does not change the named Acceptance Authority.

## 2. What Is a Solution Module?

A Solution Module is a group of approved Functional Capabilities that together deliver a meaningful piece of system behavior.

Solution Modules:

- Are formed only from approved Functional Capabilities.
- Serve as the primary unit of testing, deployment, and acceptance within the Solution Deliverables domain.
- Do not expand or reinterpret approved Functional Capabilities.

## 3. How Solution Modules Are Created

Solution Modules are created by:

1. Reviewing the approved Functional Capabilities.
2. Grouping related capabilities based on user flows, business processes, or system boundaries.
3. Ensuring every Capability ID belongs to at least one Solution Module (and may belong to more than one when behavior spans modules).
4. Confirming that grouping does not introduce new capabilities.



## 4. Governance Rules

A Solution Module is valid only if the following are true:

- All listed Capability IDs exist in the approved Functional Capabilities document.
- No new Capability IDs are created within this document.
- The module does not change the meaning or intent of any approved Capability.
- If new or missing behavior is identified, the Functional Capabilities document is updated and agreed to by the relevant owners before continuing.

Modules organize approved Functional Capabilities for delivery. They do not redefine them.

## 5. Solution Module Summary

| Solution Module ID | Module Name | Purpose | Included Capability IDs | Primary Users | Acceptance Approach |
| ------------------ | ----------- | ------- | ----------------------- | ------------- | ------------------- |
| SM-###             |             |         |                         |               |                     |

## 6. Detailed Solution Module Definition

### Solution Module ID: SM-##\#

### Module Name:

**Purpose**\
Brief description of what this module enables.

**Included Functional Capabilities**\
List all FC-### IDs in this module.

**Primary Users**\
Users or roles interacting with this module.

**Module Boundary**

- What is included
- What is explicitly excluded (if needed)

**Dependencies**

- Other Solution Modules
- External systems (if applicable)

**Planned Use Cases (IDs only)**\
UC-###\
UC-###

(Repeat for each module.)

## 7. Capability-to-Module Mapping

Every approved Capability ID must be assigned to at least one Solution Module. A Capability ID may be assigned to more than one Solution Module if the behavior logically spans modules.

| Capability ID | Assigned Module ID |
| ------------- | ------------------ |
| FC-###        | SM-###             |

No capability may be left unassigned.

## 8. Module-Level Testing and Acceptance

Solution Modules are tested and accepted as complete units.

Testing must validate how the capabilities work together inside the module — not in isolation.

For each Solution Module:

- All associated Use Cases must be validated.
- Acceptance criteria must be met.
- Evidence must show integrated behavior across included capabilities.

Modules may be deployed one at a time.
Each module represents the smallest deployable unit unless otherwise approved.

Final acceptance remains with the Stage 2 named Acceptance Authority.

## 9. Change Control

If during detailing:

- A new Capability ID is required, or
- Approved scope changes,

The Functional Capabilities document must be formally updated and agreed to by the relevant owners before proceeding.



