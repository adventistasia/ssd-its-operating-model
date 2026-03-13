# AI-Assisted Work Delivery Recommendations

## 1. Purpose

This document provides practical recommendations to make the work delivery model easier to understand, easier to execute, and better suited to an AI-assisted workflow in the Codex app.

The recommendations focus on:

- execution clarity for delivery teams
- stronger ownership and decision traceability
- controlled AI-assisted document production with human steering
- faster review and revision cycles directly in Codex

## 2. Current-State Observations

Based on review of the current framework and references:

- The Project Delivery Framework clearly defines stage gates and control intent, but practitioners may still struggle with "what to produce now" at each stage.
- The Solution Documentation Process is strong on traceability but is currently described as a document standard, not yet as an explicit AI-assisted operating workflow.
- The Standard Deliverables Reference is now easier to read, but teams still need implementation guidance on how to generate deliverables quickly and consistently with AI while preserving governance controls.
- Specification documents for non-solution domains now exist, but they should be adopted with a common AI prompt protocol, review protocol, and version discipline.

## 3. Target Operating Intent

Adopt a **Human-Steered, AI-Produced, Authority-Approved** delivery model:

1. Humans define intent, scope boundaries, constraints, and acceptance expectations.
2. AI drafts and revises deliverables using approved templates and traceability rules.
3. Named owners review and refine.
4. Acceptance Authorities formally approve based on evidence.

This keeps delivery fast without weakening governance.

## 4. Cross-Document Recommendations

## 4.1 Project Delivery Framework Recommendations

1. Add a "Stage Output Checklist" subsection under each stage with:
   - mandatory artifacts
   - conditional artifacts
   - owner accountable for each artifact
   - acceptance authority for each domain
2. Add a short "AI Use in This Stage" note per stage describing:
   - what AI can draft
   - what humans must approve
   - prohibited AI actions (e.g., changing authorized scope)
3. Add a "Decision Record Minimum" standard for Stage 1, 2, 3, and 7 decisions:
   - decision taken
   - decision authority
   - basis/evidence used
   - conditions and follow-up owner
4. Add one single visual flow (or compact table) mapping:
   - stage -> key decisions -> expected artifact maturity -> go/no-go outcome

Result: teams can execute the framework without interpreting long prose under time pressure.

## 4.2 Solution Documentation Process Recommendations

1. Add an "AI-Assisted Authoring Workflow" section aligned to Steps 1-4:
   - Step 1 prompt set (Functional Capabilities)
   - Step 2 prompt set (Modules and Use Cases)
   - Step 3 prompt set (Evidence packaging)
   - Step 4 prompt set (Acceptance readiness review)
2. Add "Human Validation Gates" after each step:
   - scope check (no new FC intent)
   - traceability check (FC -> SM -> UC -> evidence)
   - ownership check (named owner and reviewer)
3. Add a "Codex Review Loop" pattern:
   - reviewer comment in document
   - AI revision request with explicit instruction
   - change summary generated in the same session
4. Add a "Definition of Ready to Generate" rule before AI drafting starts:
   - authorized scope available
   - required IDs established
   - acceptance authority named

Result: AI generation becomes controlled, repeatable, and audit-friendly.

## 4.3 Standard Deliverables Reference Recommendations

1. Add a "Domain Selection Matrix" appendix with quick criteria:
   - trigger conditions
   - typical risk indicators
   - minimum deliverables by risk profile (low/medium/high)
2. Add "Minimum Viable Deliverable (MVD)" guidance for each domain:
   - smallest acceptable content set
   - when to expand depth
3. Add an "AI Drafting Guidance" block per domain:
   - required inputs
   - output format expectations
   - mandatory traceability fields
4. Add a "Do Not Use This Domain For" note per domain to prevent boundary confusion.

Result: teams can rapidly choose and right-size deliverables instead of over-documenting.

## 4.4 Non-Solution Deliverable Specifications Recommendations

1. Introduce a common, explicit front-matter standard in every specification:
   - document owner
   - review frequency
   - acceptance authority
   - classification/sensitivity (if relevant)
   - source references
2. Add a "Prompt Seed" section in each specification with:
   - one initial drafting prompt
   - one review prompt
   - one quality check prompt
3. Add "evidence examples" per specification so teams know what good acceptance evidence looks like.
4. Add a simple "quality scorecard" (clear/complete/traceable/actionable) to support fast reviews in Codex.

Result: every specification becomes executable, not just descriptive.

## 5. Codex-Centered AI Workflow Recommendation

## 5.1 Standard Workflow

1. **Initiate**
   - Human provides context, constraints, and required domain.
2. **Generate**
   - AI drafts artifact using the relevant specification.
3. **Review in Codex**
   - Reviewer adds inline comments.
4. **Revise**
   - AI applies comments and produces a structured change summary.
5. **Validate**
   - AI runs checklist validation against acceptance focus and traceability rules.
6. **Approve**
   - Named owner and Acceptance Authority sign off.
7. **Record**
   - Final artifact version + decision log + evidence links recorded.

## 5.2 Mandatory Control Rules for AI-Assisted Work

- AI must not change authorized scope without explicit instruction and governance update.
- AI output must include owner, date, and version metadata.
- AI revisions must preserve ID stability (FC/SM/UC and evidence IDs).
- Every material revision must include a concise "what changed and why" note.
- Acceptance decisions remain human authority decisions.

## 5.3 Recommended Prompting Standard

Use this instruction order in Codex prompts:

1. Objective and domain
2. Scope boundaries (in-scope / out-of-scope)
3. Required structure/template
4. Traceability IDs and references
5. Required output format
6. Review criteria

This reduces rework and inconsistent outputs.

## 6. Implementation Plan (Practical)

## Phase 1 (Immediate: 1-2 weeks)

- Add AI-Assisted workflow sections to:
  - Project Delivery Framework
  - Solution Documentation Process
  - Standard Deliverables Reference
- Publish a single reusable "Codex prompting standard" page in `work delivery`.
- Pilot on one initiative with at least three domains in scope.

## Phase 2 (Near Term: 2-4 weeks)

- Add prompt seeds and quality scorecards to each non-solution specification.
- Add domain selection matrix and MVD guidance to Standard Deliverables Reference.
- Create one acceptance evidence checklist per deliverable domain.

## Phase 3 (Embed: 4-8 weeks)

- Track adoption metrics:
  - time to first usable draft
  - review cycles per artifact
  - acceptance rework rate
  - traceability defects found at Stage 6/7
- Calibrate templates and prompts based on pilot outcomes.

## 7. Governance Benefits Expected

If implemented, this model should produce:

- clearer execution expectations at each stage
- faster document turnaround without losing control
- stronger ownership and decision accountability
- better traceability from intent to acceptance evidence
- reduced dependency on individual document authors

## 8. Recommended Next Action

Approve this recommendation set, then prioritize three immediate edits:

1. Add stage-level AI usage and output checklists in the Project Delivery Framework.
2. Add explicit AI-assisted step prompts and human validation gates in the Solution Documentation Process.
3. Add domain selection matrix + minimum viable deliverable guidance in the Standard Deliverables Reference.

These three changes will deliver the fastest improvement in usability and execution confidence.
