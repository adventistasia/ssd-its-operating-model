# Challenges and Needs Specification

## 1. Purpose and Intended Outcome

The Challenges and Needs artifact captures the practical problem basis behind a work request before deeper analysis begins.

It exists to make visible who is affected, what is happening today, where the issue appears, why it matters now, what business pain or unmet need exists, what likely causes are already visible, and what consequence follows if nothing changes. A useful Challenges and Needs artifact shows the primary challenge or need clearly, while also surfacing the related secondary challenges and needs that materially contribute to it. It gives Validation Assessment a clearer, more evidence-aware problem basis without turning into solutioning, detailed requirements, or a full business case.

The intended outcome is that the work request enters Validation Assessment with a clearer, more traceable statement of challenge, impact, and need so later analysis does not have to rediscover the basic problem framing.

## 2. When It Is Required

This artifact is required as a supporting assessment artifact for work that moves from Initial Review into Validation Assessment.

It may be brief for simple work, but the minimum content still needs to be captured explicitly so the assessment has a stable problem basis.

Where the Initial Review already contains some of this content, this artifact should refine and organize it rather than repeat it mechanically.

## 3. Intended Readers and Users

- Assessment Owner
- requestor or submitter
- sponsor or sponsor candidate
- requester SMEs and immediate team
- ITS leadership or governance reviewers
- practitioners preparing the Validation Assessment or later analysis

## 4. Intended Project Context

Use this artifact early in Work Assessment after a request has passed initial triage and needs a clearer problem framing before deeper validation.

It is especially useful when:

- the request is currently described as a preferred solution rather than a business problem
- multiple complaints or symptoms are being mixed together
- affected stakeholders or operational impacts are not yet clear
- there is urgency, pain, risk, or service degradation that needs clearer explanation

This artifact is not meant to prove the whole case for change. It is meant to sharpen the challenge and need basis for further assessment.

## 5. How Much Detail to Include

Include enough detail to show what the current challenge is, who is affected, why it matters now, what needs sit underneath the symptoms, and what likely consequence follows if nothing changes.

Keep it lightweight. The goal is a clear, evidence-aware framing of the problem and needs, not a deep root-cause study or a recommendation pack.

Where evidence is thin, anecdotal, or still forming, say so plainly rather than implying more certainty than the assessment currently has.

The governing principle is:

> Clarify the challenge, impact, and unmet need early enough to guide assessment. Do not rush into solution definition, requirements, or business case detail.

## 6. Required Content or Minimum Structure

### 6.1. Work request identity

Must include:

- work request or opportunity title
- requestor or source
- Assessment Owner
- date or version
- short note on the business area, service area, or operational context affected

### 6.2. Affected parties and operating context

Must include:

- the main users, teams, business units, customers, or stakeholders affected
- where the issue appears in practice
- any relevant timing, volume, service, compliance, or operational context that helps explain the challenge

### 6.3. Primary challenge statement

Must include:

- what is happening today
- the triggering condition, event, or reason the issue is now receiving attention
- why the timing matters now rather than later
- where the issue appears or is most visible

The statement should describe the main present challenge in plain language rather than naming a preferred solution.

### 6.4. Challenge and symptom breakdown

Must include:

- the main pain points, friction points, or failure conditions currently visible
- the way those symptoms show up in day-to-day work, service delivery, control performance, or user experience
- any secondary or contributing challenges that materially make up the main challenge

Where more than one challenge is materially relevant, present them as a short list or table so the primary challenge and the supporting challenges stay distinct.

### 6.5. Needs breakdown and desired improvement

Must include:

- the unmet business, service, operational, control, or user need underneath the visible symptoms
- any secondary or supporting needs that materially sit under the main need
- the practical improvement that stakeholders are seeking
- any visible solution assumption that should remain treated as an assumption rather than an accepted need

Where possible, distinguish the main underlying need from the symptom that triggered attention, and distinguish supporting needs from preferred solutions. Do not let a requested tool, feature, vendor, or delivery approach silently become the accepted statement of need.

### 6.6. Likely causes or contributing factors

Must include:

- the likely causes, drivers, or contributing factors already visible
- a clear note where these are still assumptions rather than validated findings
- any notable evidence gap or confidence limit that affects how strongly the causes can be stated

This section should frame likely causes lightly. It should not become a full root-cause analysis exercise unless that is separately justified later.

### 6.7. Why it matters now and consequence of inaction

Must include:

- why the matter needs attention now
- the business, operational, service, control, user, or compliance impact
- the likely consequence of doing nothing in the near to medium term

### 6.8. Assessment framing notes

Must include:

- what Validation Assessment should test, confirm, or clarify next
- any key assumption, boundary note, or open question that should stay visible
- the concise problem basis and cautions that later assessment should carry forward rather than rediscover

### 6.9. Example content showing the minimum structure

Example only. Adapt to the real work request.

**6.1. Work request identity**

- Work request title: Volunteer onboarding delays and inconsistent approvals
- Requestor: Mission administration office
- Assessment Owner: ITS business analysis lead
- Date: 2026-03-22
- Context affected: volunteer intake and screening across mission offices

**6.2. Affected parties and operating context**

- Affected parties: mission office administrators, volunteers, HR support staff, local approvers
- Where the issue appears: intake, approval, and confirmation steps before a volunteer starts service
- Operating context: high intake periods before major programs create delay and confusion

**6.3. Primary challenge statement**

- Today the volunteer onboarding process is slow and inconsistent across offices.
- The issue has gained attention because upcoming regional programs require faster onboarding with clearer accountability.
- The issue is most visible between document submission, approval, and confirmation.

**6.4. Challenge and symptom breakdown**

| Challenge | How it shows up today |
| --- | --- |
| Primary challenge: delayed onboarding | volunteers wait for status updates and start dates move without clear explanation |
| Contributing challenge: fragmented approvals | different offices use different approval sequences and email chains |
| Contributing challenge: poor status visibility | administrators and volunteers cannot see where an application is stuck |
| Contributing challenge: repeated document checking | the same supporting documents are reviewed more than once |

**6.5. Needs breakdown and desired improvement**

| Need | Why it matters |
| --- | --- |
| Primary need: a consistent and visible onboarding path | reduces confusion and allows work to move predictably |
| Supporting need: clearer ownership at each approval point | prevents requests from sitting unattended |
| Supporting need: reusable status information | allows staff and volunteers to know the current position without manual follow-up |
| Desired improvement | onboarding should move through a consistent path with clearer status and fewer repeated checks |

**6.6. Likely causes or contributing factors**

- approval steps are locally interpreted rather than consistently defined
- information is tracked in email and spreadsheets instead of one visible record
- ownership between administration and local approvers is not always explicit
- these are current signals and still need validation

**6.7. Why it matters now and consequence of inaction**

- Why now: upcoming regional programs increase volume and timing pressure
- Impact: delayed service start, administrator workload, poor user confidence, and weak traceability
- Consequence of inaction: onboarding delays and inconsistent approval records will continue into the next program cycle

**6.8. Assessment framing notes**

- Validation should confirm whether the main delay sits in approval sequencing, status visibility, or document handling
- Validation should test whether one common process exists today or whether offices are operating materially different variants
- Open question: who should own the end-to-end onboarding outcome

## 7. What to Keep Out

Keep the following out of this artifact:

- preferred solution descriptions presented as the answer
- detailed requirements
- target-state design
- implementation plans or estimates
- vendor preferences or product comparisons
- full business case content

## 8. Relationships to Other Artifacts

This artifact builds on the [Initial Review](initial_review_specification.md) and provides direct input to the [Validation Assessment](validation_assessment_specification.md).

It may also inform the:

- [Current State Analysis Report](current_state_analysis_report_specification.md)
- [Work Assessment Report](work_assessment_report_specification.md)

It is a supporting assessment artifact, not a replacement for the Validation Assessment decision record.

## 9. Ownership, Review, and Acceptance Expectations

The Assessment Owner usually prepares this artifact with the requestor, affected subject matter experts, and sponsor candidate where available.

Because this artifact frames the problem basis for later assessment, the requestor side and the IT Assessment Owner should both be comfortable that it represents the challenge fairly and in plain language.

Formal acceptance is not normally required, but the artifact should be credible enough to guide Validation Assessment.

Where the request began in solution-shaped language, reviewers should check that the documented need still reads as a business or operational problem rather than a disguised implementation ask.

## 10. Maintenance Expectations

This artifact may be updated during Validation Assessment if the challenge, impact, or underlying need is materially clarified.

Once the Validation Assessment recommendation is recorded, the artifact normally becomes stable unless the work is deferred and later re-opened under materially changed circumstances.

## 11. Validation Guide

- Does the artifact make clear who is affected, what is happening today, where it appears, and why it matters now?
- Does it describe the primary challenge and need clearly while also surfacing any material contributing challenges and needs?
- Does it describe the challenge and unmet need without jumping straight to a preferred solution?
- Are visible pain points and likely impacts explained in practical language?
- Does it distinguish symptoms from underlying needs where that distinction matters?
- Does it make clear why the issue matters now rather than later?
- Are likely causes or contributing factors framed carefully rather than treated as already proven?
- Are important solution assumptions, evidence gaps, or confidence limits still visible?
- Does it give Validation Assessment a clearer problem basis and set of questions to test next?

## 12. Prompt Guide for Drafting the Artifact

### 12.1. Starter prompt

> Draft a Challenges and Needs artifact for a work item that has passed initial triage.
> Explain who is affected, what is happening today, where the issue appears, why it matters now, what the primary challenge or need is, what related secondary challenges or needs also materially contribute, what likely causes are already visible, what impact is being felt, and what consequence may follow if nothing changes.
> Note any evidence gap, confidence limit, or solution assumption that still needs validation.
> Keep it practical, lightweight, and free of solution design or detailed requirements.

### 12.2. Section prompts

> Rewrite the challenge statement so it describes the business problem and operating reality without naming a preferred system, tool, or delivery approach.

> Distinguish the visible symptoms from the underlying business or operational needs in plain language, and make the primary need clear without hiding the supporting needs.

> Identify any requested solution idea that should remain visible as an assumption to test rather than as accepted need.

### 12.3. Validation prompts

> Check whether this artifact gives Validation Assessment a clear problem basis without becoming a business case, requirement set, or solution brief.

> Rewrite any section that turns a likely cause into a confirmed fact, hides an evidence gap, or turns an unmet need into a premature solution statement.
