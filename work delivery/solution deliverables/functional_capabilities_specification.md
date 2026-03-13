# Functional Capabilities Specification

## 1. Purpose

A Functional Capabilities document defines **WHAT** the solution must be able to do. It establishes the approved functional scope for an initiative.

Functional Capabilities describe business abilities. They do not describe workflows, sequencing, implementation design, technical details, or test cases.

## 2. Role in the Project Delivery Framework

Functional Capabilities define the approval-level functional scope in **Stage 2 (Delivery Definition)**.

They serve as the baseline from which:

- Solution Modules are formed,
- Detailed design and Use-Case Specifications are derived, and
- Scope changes are evaluated.

All downstream artifacts must remain consistent with the approved Functional Capabilities.

## 3. Inputs Needed

To create a Functional Capabilities document (human or AI), the following inputs are required:

- **Initiative Definition:** outcome statement, measurable success indicators, and scope boundaries (in/out)
- **Users / actors:** who will use the solution and who is impacted
- **Current state summary:** what exists today and what problem is being solved
- **Constraints:** policy, security, compliance, or major technical constraints
- **Key terms:** important definitions used in capability statements

If these inputs are unclear, the Functional Capabilities document will be incomplete or unstable.

## 4. What Is a Functional Capability?

A Functional Capability is a single **business ability** the solution must provide.

A good capability statement:

- Describes an ability (not a process)
- Is clear and specific, but not design detail
- Can stand alone and be understood independently
- Links back to at least one measurable success indicator

A capability statement is **not**:

- A step-by-step workflow
- A screen description
- A technical design decision
- A list of detailed business rules

## 5. Required Contents of a Functional Capabilities Document

A Functional Capabilities document must include a clear, complete Functional Capabilities list.

Capabilities should be grouped logically by business area when helpful. Grouping is recommended but not mandatory.

Each capability entry must include:

- **Capability ID** (stable once assigned)
- **Capability statement** (one clear business ability)
- **Business intent / value** (why this capability exists)

Other recommended fields (include when useful for clarity and acceptance):

- **Primary user role(s)** (who uses or benefits)
- **Supported success indicator(s)** (which outcome measure(s) this capability supports)
- **Notes** (short clarifications only; do not add workflow or design)

Optional: short notes may be included to support later derivation of Use Cases and acceptance criteria.

### Capability ID Format

Capability IDs must follow a consistent structure.

Recommended format:

- **FC-X.Y**

Where:

- **X** = capability group number (business grouping)
- **Y** = capability number within that group

Examples:

- FC-1.1
- FC-1.2
- FC-2.1

Guidelines:

- Group related capabilities under the same X value.
- Number capabilities sequentially within each group.
- Do not renumber existing IDs once assigned.
- Retired IDs must not be reused.

## 6. Writing and Governance Rules

Capability statements must follow these rules:

- **Atomic:** one clear ability per capability
- **Non-overlapping:** avoid duplicates or partial repeats
- **No sequencing:** do not describe steps (that belongs in Use Cases)
- **No implementation detail:** do not describe systems, screens, APIs, or technical choices
- **No embedded validation rules:** detailed rules belong in downstream artifacts

A capability is valid only if:

- It supports the outcome and success criteria defined in the Initiative Definition.
- It fits within the scope boundaries (in/out) defined in the Initiative Definition.
- It follows the writing rules above.

ID discipline:

- Capability IDs must remain stable once assigned.
- If a capability must change meaning, the Functional Capabilities document must be formally updated and agreed to by the relevant owners.

Functional Capabilities define approved scope. They do not define how the solution is built.

## 7. AI Drafting Guidance

When drafting with AI:

1. Provide the inputs listed in Section 3.
2. Ask for atomic capability statements expressed as business abilities.
3. Remove sequencing or implementation language.
4. Check for overlap and split combined abilities.
5. Assign stable Capability IDs only after the list is agreed.
6. Confirm each capability links to a measurable success indicator.

Quality checks:

- Every capability supports the outcome.
- No capability contains workflow steps or design details.
- Scope boundaries are explicit.
- Capability IDs are unique and stable.

