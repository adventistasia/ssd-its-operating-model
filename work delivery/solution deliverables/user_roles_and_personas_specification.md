# User Roles and Personas Specification

## 1. Purpose

This specification defines what **User Roles** are, how a **User Roles** document must be written, and how it supports the **Project Delivery Framework**.

User Roles define **who uses the solution** and what access boundaries must exist (e.g., applicant vs staff). They provide shared language for drafting Functional Capabilities, Solution Modules, and Use Cases.

Personas are optional. When used, they add human context and help teams write clearer Use Cases and acceptance Success Conditions.


## 2. Role in the Project Delivery Framework

User Roles support consistent delivery by providing stable actors and access assumptions.

- **Stage 2 (Delivery Definition):** clarify actors, responsibilities, and access boundaries before approving Functional Capabilities and Solution Modules.
- **Stage 4 (Delivery Elaboration):** used directly in Use Cases to define primary/supporting actors and to check module boundaries.
- **Delivery and acceptance:** help ensure behavior is validated for the right users and that role-based access rules are respected.

User Roles do not define solution scope by themselves. They describe actors for the approved scope.


## 3. Inputs needed

To create a User Roles document (human or AI), the following inputs are required:

- Project outcome and scope boundaries
- List of stakeholder groups and job functions
- Known access model boundaries (e.g., internal staff vs external users)
- Any existing role models, policies, or org structures
- Security/compliance constraints that affect access
- Key terms and definitions

If these inputs are unclear, roles will be ambiguous and Use Cases will drift.


## 4. What is a User Role?

A User Role is a named category of users that share:

- Similar goals and responsibilities
- Similar access needs and restrictions
- Similar interaction patterns with the solution

A User Role is not:

- A specific person
- A department name (unless it directly maps to access and responsibilities)
- A list of permissions (permissions are derived)


## 5. Required contents of a User Roles document

A User Roles document must include the following sections.

### 5.1 Role list

A list of roles with stable role names. Each role entry must include:

- **Role name**
- **Role description** (what this role does in business terms)
- **Primary goals** (what success looks like for this role)
- **Key actions** (what this role typically does in the system)
- **Access boundary** (internal/external, applicant/staff, etc.)
- **Data sensitivity notes** (if the role touches sensitive data)

### 5.2 Role relationships (recommended)

Describe how roles relate to each other when it affects solution behavior.

Examples:
- reviewer chain (Org → Mission → Union → Division)
- separation of duties (committee decision vs execution)

### 5.3 Role-to-solution references (recommended)

A short mapping that helps downstream artifacts stay consistent:

- Roles used in Functional Capabilities (where relevant)
- Roles used in Solution Modules (primary users)
- Roles used in Use Cases (primary/supporting actors)


## 6. Writing and governance rules

User Roles must follow these rules:

- **Clear and distinct:** avoid overlapping roles unless overlap is intentional.
- **Behavior-oriented:** define what the role does, not how the system is built.
- **Stable naming:** role names should remain stable once agreed.
- **Access-aware:** roles must reflect real access boundaries (e.g., applicant vs staff).

If role definitions change after Stage 2 approval in a way that affects scope, use cases, or access assumptions, the change must be agreed to by the relevant owners before work continues.


## 7. Personas (optional)

Personas are optional. They are used when the team needs more context than a role name can provide.

### 7.1 Roles vs Personas

- **Role**: a named category of users used for access boundaries, responsibilities, and behavior in the system.
- **Persona**: a realistic example of a person within a role that highlights goals, constraints, and working context.

A role answers: **“Who is this user in the system?”**
A persona answers: **“What is this user like in real life, and what do they need to succeed?”**

### 7.2 Outcomes personas help achieve

Personas can improve delivery outcomes by making requirements and use cases easier to write and review. Typical outcomes include:

- Clearer Use Cases and Success Conditions (less ambiguity)
- Better usability decisions (especially for non-expert users)
- Fewer missed edge cases (low bandwidth, language, accessibility)
- More consistent training and support materials

### 7.3 When personas are most useful

Use personas when:

- The role represents a wide range of users and needs a concrete example.
- Use Cases are hard to write clearly without real-world context.
- Adoption risk is high (new process, new audience, low digital literacy).
- Communication flows matter (notifications, approvals, handoffs).

Personas can also add value outside delivery definition:

- **User enablement and training:** tailor guides to real user constraints.
- **Support workflows:** anticipate common failures and support needs.
- **Change management / marketing:** communicate value in language that fits real users.

### 7.4 Persona-informed workflow considerations

Personas are especially helpful when different users in the same role behave very differently.

Examples:

- **Digitally inexperienced user:** needs simpler steps, clearer prompts, fewer decisions per screen.
- **Low connectivity / mobile-only user:** needs offline-safe drafts, shorter sessions, and resumable actions.
- **Second-language user:** needs simpler language and clear terms.

Personas must not add new scope. If a persona reveals missing capability intent, handle it through the normal Functional Capabilities update and agreement process.

### 7.5 Persona fields (optional)

A persona should be short and practical.

- Persona name (fictional)
- Role
- Context and environment
- Key goals
- Pain points
- Constraints (language, connectivity, device, accessibility, digital skill)
- Enablement needs (optional; what training/help this user will need)


## 8. Prompt suggestions

Use the prompts below to draft roles and (optionally) personas consistently.

### 8.1 Inputs to provide to the AI

Provide:

- Outcome statement and measurable success indicators
- Scope boundaries (in/out)
- Stakeholder groups and org structure
- Known access boundaries and policies
- Any existing role lists
- Key terms and definitions

### 8.2 Prompt: draft role list

“Draft a User Roles list for this project.

Rules:
- Roles must be clear and distinct.
- Each role must include: description, primary goals, key actions, access boundary, and data sensitivity notes.
- Avoid defining permissions; describe responsibilities and access boundaries.
- Do not introduce new solution scope.

Output:
- A table with the required role fields.”

### 8.3 Prompt: draft role relationships

“Using the drafted roles, describe role relationships that affect behavior.

Rules:
- Include reviewer chains and separation-of-duties relationships where applicable.
- Keep it short and behavior-focused.

Output:
- A short list of role relationships and why they matter.”

### 8.4 Prompt: optional personas

“Create optional personas only where they improve clarity.

Rules:
- Keep each persona short.
- Personas must map to an existing role.
- Personas must not add scope.

Output:
- 0–3 personas with: name, role, context, goals, pain points, and constraints.”

### 8.5 Prompt: quality check

“Review the User Roles and Personas for:
- Role overlap or ambiguity
- Missing access boundaries
- Roles that imply new scope
- Roles missing goals or key actions

Output:
- Issues found and suggested fixes.”


## 9. Appendix: Example user roles and personas (fictional)

Example project: **Volunteer Program Registration Portal**

### 9.1 Example role list

| Role name | Role description | Primary goals | Key actions | Access boundary | Data sensitivity notes |
|---|---|---|---|---|---|
| Volunteer | External user who registers for programs and submits required information | Register successfully; receive clear confirmation | Create profile; submit forms; upload documents; check status | External | Personal data; contact details; identity documents |
| Program Coordinator | Staff who reviews registrations and manages program capacity | Fill slots; ensure eligibility; communicate decisions | Review submissions; request corrections; approve/decline; message volunteers | Internal staff | Can view personal data; must follow privacy rules |
| Site Supervisor | Staff who confirms attendance and records completion | Track participation accurately | View approved volunteers; confirm attendance; record completion notes | Internal staff | Limited personal data; attendance records |
| Finance Reviewer | Staff who reviews stipend or reimbursement eligibility | Pay correctly and on time | Review stipend eligibility; export approved payouts | Internal staff | Financial data; payout details |
| Admin | System administrator managing access and configuration | Keep system usable and secure | Manage roles; deactivate accounts; manage program templates | Internal admin | Broad access; highest risk role |

### 9.2 Example role relationships (recommended)

- Separation of duties: Program Coordinator approves participation; Finance Reviewer approves payouts.
- Visibility rule: Volunteers cannot see internal notes.

### 9.3 Example personas (optional)

**Persona: Maria (Volunteer, mobile-only)**
- Context: Rural area, mobile phone only, intermittent connectivity
- Goals: Register quickly; avoid repeating steps
- Pain points: Sessions time out; uploads fail
- Constraints: Low bandwidth; small screen
- Enablement needs: Short “how to register” guide with screenshots

**Persona: Daniel (Volunteer, digitally inexperienced)**
- Context: First time using an online portal for forms
- Goals: Know what to do next; avoid mistakes
- Pain points: Confusing terms; too many choices per step
- Constraints: Low digital skill; second-language English
- Enablement needs: Plain-language instructions and clear error messages

**Persona: Leah (Program Coordinator, high volume)**
- Context: Reviews hundreds of registrations near deadlines
- Goals: Process quickly; avoid missing required documents
- Pain points: Manual follow-ups; unclear statuses
- Constraints: Time pressure; needs bulk views
- Enablement needs: Short checklist for review decisions and standard message templates

