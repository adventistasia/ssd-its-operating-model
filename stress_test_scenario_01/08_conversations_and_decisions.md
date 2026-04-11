# Conversations And Decisions

Status: working draft  
Purpose: preserve the simulated multi-agent interactions that shaped the Delivery Owner's path.

## 1. Delivery Owner and Jane

### 1.1. Key signals

- wants a simple and trustworthy tracker
- wants low maintenance
- resists heavy process
- does not want the work to turn into a project for its own sake

### 1.2. Transcript excerpt

Delivery Owner: What problem are we solving first?

Jane: Just visibility. Right now I have to ask around every time someone needs to know where staff are.

Delivery Owner: Do we have a sponsor or decision owner for this?

Jane: Not yet, but Angie is listening. I just need something people will actually open.

Delivery Owner: What would simple look like?

Jane: A single tracker that shows who is out, where they are, and when they are back. Nothing fancy.

### 1.3. Delivery Owner interpretation

Jane validates the need, but she does not solve the control gaps.

## 2. Delivery Owner and Angie the Sponsor

### 2.1. Key signals

- skeptical of overbuilding
- supports a proportionate solution
- wants the work to stay useful, not ceremonial
- does not want a new system if existing records can be reused

### 2.2. Transcript excerpt

Delivery Owner: This is small, but we still need a control path.

Angie: Then keep it small. I do not want a custom app if a controlled tracker is enough.

Delivery Owner: What is the one thing you care about most?

Angie: That the answer is trustworthy, the work is proportionate, and we do not create more process than the problem deserves.

### 2.3. Delivery Owner interpretation

Angie becomes the sponsor signal that lets the Delivery Owner keep the path lightweight without treating it casually.

## 3. Delivery Owner and Programmer / Technical SME

### 3.1. Key signals

- source-of-truth choice is unresolved
- revision logic is unresolved
- a quick build would hard-code unapproved process logic
- structured Microsoft 365 is the most proportionate technical direction

### 3.2. Transcript excerpt

Delivery Owner: We just need a staff itinerary tracker. Can you build the form this week?

Programmer: I can build it, but not until I know the system of record and who approves changes.

Delivery Owner: It's just a tracker. Why do we need that level of detail?

Programmer: Because "just a tracker" becomes three versions of truth the moment someone edits a trip after approval.

Delivery Owner: So what do you need from me?

Programmer: One owner for the data, one owner for acceptance, the edit and approval rule, and a decision on whether the tracker or the document is the authoritative record.

### 3.3. Delivery Owner interpretation

The Programmer converts vague friction into concrete definition needs. This is the point where the Delivery Owner stops thinking in terms of a task note.

## 4. Delivery Owner and Committee Secretary

### 4.1. Key signals

- approved itinerary record must remain controlling
- chat or informal clearance is not approval
- revision history matters
- duplicate encoding is a real risk

### 4.2. Transcript excerpt

Committee Secretary: I need the tracker to match the approved itinerary record, not a chat thread.

Delivery Owner: So if someone says "okay" in chat, that is not enough?

Committee Secretary: Correct. If the committee record does not show it, the tracker cannot present it as approved.

Delivery Owner: What about revisions?

Committee Secretary: Keep the prior version visible until the revision is formally approved. Do not hide the trail.

### 4.3. Delivery Owner interpretation

This conversation sharply reduces ambiguity about itinerary authority, but it also makes the first release more disciplined than a plain shared sheet.

## 5. Delivery Owner and leave-record owner

### 5.1. Key signals

- leave status is a separate authoritative record
- the tracker should not duplicate HR or leave approval logic
- visibility is acceptable if it does not create a second source of truth

### 5.2. Transcript excerpt

Delivery Owner: If the tracker shows leave status, do we need to rebuild the leave process too?

Leave-record owner: No. Do not turn this into a leave system. Publish only the status the office needs, and keep the leave record authoritative.

### 5.3. Delivery Owner interpretation

This keeps the work small, but it also confirms that the solution has to respect more than one record owner.

## 6. Delivery Owner and Office Operations lead

### 6.1. Key signals

- outcome focus is coordination speed and trust
- acceptance focus is usefulness plus correct ownership mapping
- the work remains small enough for a Work Brief

### 6.2. Transcript excerpt

Delivery Owner: Would you accept a small visibility tracker if the source-of-truth rules are explicit?

Office Operations lead: Yes. I want less confusion, not a bigger system. But I need the ownership story to be clean.

### 6.3. Delivery Owner interpretation

This conversation gives the Delivery Owner a plausible outcome owner and keeps the work within a light governed path.

## 7. Decisions shaped by the conversations

### 7.1. Decision: start at Stage 1

Reason:

- current stage was unclear
- ownership was incomplete

### 7.2. Decision: use the Work Brief path

Reason:

- the work stayed small enough for a scaled path
- still too governed for an informal note

### 7.3. Decision: keep the first-release solution direction visibility-focused

Reason:

- useful sooner
- lower burden than a full workflow redesign
- more realistic for the request size

### 7.4. Decision: stop short of build-ready design

Reason:

- source-of-truth and acceptance questions remained unresolved at the start of assessment
- pretending otherwise would hide the framework's real test result

### 7.5. Decision: approve the small governed item with conditions

Reason:

- the sponsor wants proportionate control
- the work is useful and small
- the first release can stay as a visibility layer over existing authoritative records

Conditions:

- use existing authoritative records
- do not create a second system of record
- keep the Delivery Charter and roadmap light but explicit
