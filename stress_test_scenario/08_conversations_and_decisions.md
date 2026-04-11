# Conversations And Decisions

Status: working draft  
Purpose: preserve the simulated multi-agent interactions that shaped the Delivery Owner's path.

## 1. Delivery Owner and Jane

### 1.1. Key signals

- wants a simple and trustworthy tracker
- wants low maintenance
- resists heavy process
- cannot name the sponsor or owner structure

### 1.2. Transcript excerpt

Delivery Owner: What problem are we solving first?  
Jane: Just visibility. Right now I have to ask around every time someone needs to know where staff are.

Delivery Owner: Do we have a sponsor or decision owner for this?  
Jane: Not that I know of. People just keep asking for it because the current way is messy.

Delivery Owner: What would simple look like?  
Jane: A single tracker that shows who is out, where they are, and when they are back. Nothing fancy.

Delivery Owner: Any hard no's?  
Jane: No complicated approvals, no long forms, no project language. I need something people will actually open.

### 1.3. Delivery Owner interpretation

Jane validated the need but did not solve the control gaps.

## 2. Delivery Owner and Programmer

### 2.1. Key signals

- source-of-truth choice is unresolved
- revision logic is unresolved
- a quick build would hard-code unapproved process logic
- structured Microsoft 365 is the most proportionate technical direction

### 2.2. Transcript excerpt

Delivery Owner: We just need a staff itinerary tracker. Can you build the form this week?  
Programmer: I can build it, but not until I know the system of record and who approves changes.

Delivery Owner: It's just a tracker. Why do we need that level of detail?  
Programmer: Because "just a tracker" becomes three versions of truth the moment someone edits a trip after approval.

Delivery Owner: So what do you need from me?  
Programmer: One owner for the data, one owner for acceptance, the edit and approval rule, and a decision on whether the tracker or a document is the authoritative record.

### 2.3. Delivery Owner interpretation

The programmer converted vague friction into concrete definition needs. This was the moment the Delivery Owner decided a mere task note would be insufficient.

## 3. Delivery Owner and Committee Secretary

### 3.1. Key signals

- approved itinerary record must remain controlling
- chat or informal clearance is not approval
- revision history matters
- duplicate encoding is a real risk

### 3.2. Transcript excerpt

Committee Secretary: I need the tracker to match the approved itinerary record exactly.  
Delivery Owner: The team said they already cleared it in chat, so I marked it as confirmed.

Committee Secretary: Chat clearance is not approval. If the committee record does not show it, the tracker cannot present it as approved.  
Delivery Owner: Then should I just replace the old entry with the new one?

Committee Secretary: No. Replace the status only if the revision is formally approved. Keep the prior version visible so we can see what changed.

### 3.3. Delivery Owner interpretation

This conversation sharply reduced ambiguity about itinerary authority, but it also made the first release harder to keep simple.

## 4. Delivery Owner and Disbursing Accountant

### 4.1. Key signals

- timeliness matters
- searchable and current status matters
- first release can stay lightweight if it reduces hunting through email

### 4.2. Transcript excerpt

Delivery Owner: What do you need from the tracker to make approvals and follow-up workable?  
Disbursing Accountant: The minimum is traveler name, dates, destination, purpose, approver, and supporting documents.

Delivery Owner: If we keep the first version lightweight, what can stay manual?  
Disbursing Accountant: Follow-up can stay manual for now, but the tracker has to stop us from hunting through email.

### 4.3. Delivery Owner interpretation

Finance pressure reinforced the need for usefulness now, not theoretical future completeness.

## 5. Additional stakeholder introduced by the Delivery Owner

Role added: HR / leave-record owner

Reason:

- the request explicitly combines itinerary and leave status
- no interviewed stakeholder owned the leave side of the truth model
- the framework made the missing ownership visible, but it did not provide a default answer

Working conclusion:

- leave-status integration cannot be treated as trivial
- any real project would need the leave-record owner engaged before authorization

## 6. Decisions shaped by the conversations

### 6.1. Decision: start at Stage 1

Reason:

- current stage was unclear
- ownership was incomplete

### 6.2. Decision: use the Work Brief path

Reason:

- the work stayed small enough for a scaled path
- still too governed for an informal note

### 6.3. Decision: keep the first-release solution direction visibility-focused

Reason:

- useful sooner
- lower burden than a full workflow redesign
- more realistic for the request size

### 6.4. Decision: stop short of build-ready design

Reason:

- source-of-truth and acceptance questions remained unresolved
- pretending otherwise would hide the framework's real test result
