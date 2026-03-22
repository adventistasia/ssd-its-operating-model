# Types of Diagrams Guide

## 1. Purpose

This guide helps practitioners and AI agents choose the lightest useful diagram when Work Assessment needs a visual view of the current process, current state, handoffs, data movement, or assessment boundary.

The intent is not to produce diagrams for their own sake. The intent is to choose a diagram only when it makes the current state easier to understand, review, or carry forward.

## 2. How to Use This Guide

Choose the simplest diagram that answers the assessment question clearly.

Use a diagram when it materially improves understanding of:

- process stages
- handoffs between roles or teams
- current-state boundaries
- inputs, outputs, and customers
- data movement between people, systems, and records

Do not use a heavy notation if a short table or simple flowchart is enough.

## 3. The 5 Most Helpful Diagram Types in This Context

### 3.1. SIPOC diagram

Best use:

- early assessment when you need a quick high-level process boundary
- clarifying suppliers, inputs, process, outputs, and customers before deeper analysis

Most helpful when:

- the process is still poorly framed
- the team needs a shared starting view before building a flowchart

Less helpful when:

- you need to show detailed handoffs, decisions, or exceptions

Why it fits our context:

- good for Challenges and Needs and early Validation Assessment
- keeps assessment light while making the process boundary explicit

References:

- [ASQ: SIPOC diagram](https://asq.org/quality-resources/sipoc)

### 3.2. Basic flowchart

Best use:

- a mostly linear process with a manageable number of decisions
- quickly showing the normal current path from start to finish

Most helpful when:

- one team or one owner mainly performs the work
- the main need is to show sequence rather than ownership complexity

Less helpful when:

- multiple teams, handoffs, or message exchanges matter

Why it fits our context:

- good for a light Business Process Stage Analysis where the stage sequence is more important than cross-team structure

References:

- [Microsoft Support: process diagrams in Visio](https://support.microsoft.com/en-gb/office/process-diagrams-in-visio-f064cd25-d7d5-47b8-87e1-ecb3c39cc165)

### 3.3. Cross-functional flowchart

Best use:

- showing who does what and where handoffs occur
- making lane ownership and phase progression visible

Most helpful when:

- the main issue sits between teams, roles, offices, or departments
- work moves across functional boundaries and delays or rework happen at handoff points

Less helpful when:

- the process is highly event-driven or message-heavy and needs a more formal notation

Why it fits our context:

- often the most practical choice for Work Assessment because it makes accountability and handoffs visible without requiring a heavy standard

References:

- [Microsoft Support: create a cross-functional flowchart](https://support.microsoft.com/en-us/office/create-a-cross-functional-flowchart-4a403033-9787-454f-b87e-b88452c47a21)
- [Microsoft Support: add swimlanes to a flowchart](https://support.microsoft.com/en-gb/office/add-swimlanes-to-a-flowchart-d794b112-8aa3-4360-8f12-e38bc62ad558)

### 3.4. BPMN diagram

Best use:

- processes with multiple participants, gateways, events, exceptions, messages, or control points
- cases where a common formal notation helps avoid ambiguity

Most helpful when:

- the workflow is complex enough that a basic or swimlane flowchart becomes hard to read
- the assessment must make decision logic, message flows, or collaboration boundaries explicit

Less helpful when:

- the audience only needs a lightweight current-state picture
- the process is simple and the notation would add more complexity than clarity

Why it fits our context:

- useful for higher-complexity Business Process Stage Analysis or Current State Analysis where controls, exceptions, and inter-team interactions materially shape the recommendation

References:

- [IBM: what is BPMN](https://www.ibm.com/think/topics/bpmn)
- [IBM Docs: BPMN diagrams](https://www.ibm.com/docs/SSCLKU_7.5.5/com.ibm.xtools.bpmn.diagram.doc/topics/c_bpmndiag.html)

### 3.5. Data flow diagram

Best use:

- showing how information moves between people, systems, processes, and data stores
- clarifying records, interfaces, inputs, outputs, and data dependencies

Most helpful when:

- the work request is shaped by fragmented systems, duplicate data entry, unclear records, or interface gaps
- the team needs to separate work sequence from data movement

Less helpful when:

- the main need is to show task sequence or role accountability

Why it fits our context:

- useful for Current State Analysis when records, data movement, or control evidence matter as much as the activity sequence

References:

- [Miro: what is a data flow diagram](https://miro.com/diagramming/what-is-a-data-flow-diagram/)
- [Lucidchart: how to make a data flow diagram](https://www.lucidchart.com/pages/data-flow-diagram/how-to-make-a-dfd)

## 4. Quick Selection Guide

| If you need to show... | Start with... | Move up to... |
| --- | --- | --- |
| basic process boundary and key inputs and outputs | SIPOC | basic flowchart |
| simple step sequence | basic flowchart | cross-functional flowchart |
| roles, handoffs, and accountability | cross-functional flowchart | BPMN |
| events, gateways, exceptions, or message exchanges | BPMN | BPMN with a short companion table |
| data movement, records, or data stores | data flow diagram | data flow diagram plus a simple process flow |

## 5. Practical Guidance for This Repository

- Use the lightest diagram that answers the assessment question.
- Pair diagrams with short text so the governance meaning is explicit.
- Do not let diagrams replace required narrative or table content in the specifications.
- In Work Assessment, diagram only the current state unless the artifact explicitly asks for something else.
- If the diagram becomes hard to explain quickly, it is probably too detailed for Work Assessment.

## 6. Additional Resources

- [Object Management Group: BPMN specification information](https://www.omg.org/spec/BPMN/2.0/Beta2/About-BPMN)
- [Microsoft Support: Visio diagram types](https://support.microsoft.com/en-us/office/types-of-diagrams-that-are-supported-in-visio-in-microsoft-365-877c30a8-0951-4b7a-a53b-daa3d81bea03)
- [IBM: workflow diagram overview](https://www.ibm.com/think/topics/workflow-diagram)
- [Lucidchart: UML use case diagram tutorial](https://www.lucidchart.com/pages/uml-use-case-diagram)
- [Figma: Types of Flow Charts](https://www.figma.com/resource-library/types-of-flow-charts/)

Use these as reading support. They should not override the lighter drafting and governance boundaries defined in this repository.
