# Dispute Resolution

## Dispute Resolution for VCNIA

This document defines a basic dispute resolution model for **VCNIA: Value-Circulating Network Intelligence Architecture**.

VCNIA is based on the following stack:

```text
Existence Proof → Gratitude → Trust → Royalty / Value Allocation → Network Intelligence

Its core principle is:

Intelligence emerges where value circulates.

Because VCNIA handles traces, gratitude, trust, and value allocation, disputes are inevitable.

A fair value circulation system must therefore include a clear process for review, correction, rejection, and appeal.

1. Purpose

The purpose of dispute resolution in VCNIA is to protect the integrity of value circulation.

Dispute resolution helps answer:

Was a trace registered correctly?
Was provenance accurate?
Was gratitude valid?
Was trust updated fairly?
Was value allocated correctly?
Was privacy respected?
Was manipulation involved?
Was a contributor unfairly excluded?

A VCNIA-compatible system should not assume that all records are final.

Records must be reviewable.

2. Core Principle

The core dispute principle of VCNIA is:

Every high-impact record should be reviewable,
every disputed record should be auditable,
and every correction should preserve traceability.

In shorter form:

No fair circulation without correction.

A system that cannot correct errors will eventually circulate distortion.

3. What Can Be Disputed?

Disputes may apply to any layer of VCNIA.

Layer	Disputable Object	Example
Existence Proof	Trace record	A trace was registered with false provenance
Gratitude	Gratitude event	Gratitude was issued falsely or manipulatively
Trust	Trust event / trust profile	Trust score changed unfairly
Royalty / Value Allocation	Allocation event	Value was distributed incorrectly
Governance	Policy decision	A rule was applied inconsistently
Privacy	Disclosure event	Sensitive trace data was exposed improperly
4. Dispute Categories

VCNIA disputes may be classified into several categories.

4.1 Trace Disputes

Trace disputes concern the existence, origin, or registration of a trace.

Examples:

false trace registration
duplicate trace claim
incorrect timestamp
copied content registered as original
missing parent trace
false provenance
unauthorized registration
4.2 Gratitude Disputes

Gratitude disputes concern recognition or impact signals.

Examples:

false gratitude
gratitude spam
gratitude issued to the wrong trace
artificial impact inflation
collusive gratitude loop
misleading gratitude message
gratitude issued without meaningful use
4.3 Trust Disputes

Trust disputes concern reliability signals.

Examples:

unfair trust reduction
inflated trust increase
incorrect risk flag
trust farming
outdated trust profile
lack of trust recovery
opaque trust calculation
improper use of disputed gratitude
4.4 Value Allocation Disputes

Value allocation disputes concern the return of value.

Examples:

incorrect allocation amount
excluded contributor
duplicate claim
wrong allocation rule
unfair contribution weight
allocation based on disputed trust
allocation without audit path
value captured by a central actor
4.5 Privacy Disputes

Privacy disputes concern exposure of contributor information.

Examples:

public trace record without consent
sensitive provenance exposed
private gratitude message disclosed
trust history made public improperly
allocation record exposing sensitive activity
failure to redact personal information
4.6 Governance Disputes

Governance disputes concern rules and processes.

Examples:

policy applied inconsistently
unclear dispute process
rule changed without versioning
no appeal path
reviewer conflict of interest
lack of transparency
centralized decision without audit
5. Minimal Dispute Flow

A minimal VCNIA dispute flow is:

Claim → Evidence Review → Decision → Correction / Rejection → Appeal

Expanded flow:

1. Dispute is submitted.
2. A dispute record is created.
3. Relevant records are frozen or flagged.
4. Evidence is collected.
5. Review is performed.
6. Decision is issued.
7. Records are corrected, rejected, or confirmed.
8. Appeal may be requested.
9. Final status is recorded.
6. Dispute Status Values

A VCNIA-compatible system may use the following dispute statuses:

Status	Meaning
none	No dispute exists
open	Dispute has been submitted
under_review	Evidence is being reviewed
resolved	Dispute has been resolved
rejected	Dispute was rejected
appealed	Decision has been appealed
closed	Dispute process is complete

Recommended lifecycle:

none → open → under_review → resolved / rejected → appealed → closed
7. Minimal Dispute Record

A dispute record may include:

Field	Description
dispute_id	Unique identifier for the dispute
dispute_type	Type of dispute
target_type	Object being disputed
target_id	ID of the disputed object
claimant_id	Party raising the dispute
reason	Human-readable reason
evidence_refs	Evidence supporting the dispute
status	Current dispute status
reviewer_id	Reviewer or reviewing system
decision	Outcome of the review
created_at	Time of dispute creation
updated_at	Time of latest update
8. Example Dispute Record
{
  "type": "dispute_record",
  "dispute_id": "dispute_vcnia_001",
  "dispute_type": "trace_provenance",
  "target_type": "trace_record",
  "target_id": "trace_vcnia_001",
  "claimant_id": "creator_example_002",
  "reason": "The trace record appears to omit a parent trace that influenced the contribution.",
  "evidence_refs": [
    {
      "ref_type": "document",
      "ref_id": "prior-design-note-001",
      "description": "Earlier design note that may have influenced the disputed trace."
    }
  ],
  "status": "open",
  "created_at": "2026-04-27T00:00:00Z",
  "updated_at": "2026-04-27T00:00:00Z"
}

This example is illustrative.
A formal dispute schema may be added in a future version.

9. Dispute Target Types

A dispute may target different record types.

Recommended target_type values:

trace_record
gratitude_event
trust_event
trust_profile
value_allocation_event
governance_policy
identity_record
privacy_record
other

Each target type requires a different review method.

10. Evidence

Disputes should be evidence-based.

Evidence may include:

trace records
source URIs
content hashes
repository commits
timestamps
screenshots
prior documents
gratitude events
trust events
governance policy versions
reviewer notes
audit logs

Evidence should be relevant, minimal, and privacy-aware.

11. Evidence Principles

Evidence used in disputes should follow these principles:

Relevance
Evidence should directly relate to the disputed record.
Traceability
Evidence should be referenceable and reviewable.
Proportionality
Do not expose excessive data for a minor dispute.
Privacy
Sensitive information should be redacted where possible.
Integrity
Evidence should not be altered without record.
Version Awareness
Governance rules and documents should be interpreted in their versioned context.
12. Temporary Effects During Dispute

When a record is disputed, downstream effects may need to be paused or reduced.

Recommended behavior:

Disputed Object	Suggested Temporary Effect
Trace record	Mark as disputed; reduce downstream influence
Gratitude event	Exclude or reduce influence on trust
Trust event	Pause trust update if high impact
Trust profile	Mark affected dimensions as under review
Value allocation event	Hold, reverse, or flag allocation depending on severity
Governance policy	Freeze rule change until review

A disputed record should not silently continue influencing high-stakes outcomes.

13. Possible Decisions

A dispute review may result in several outcomes.

Decision	Meaning
confirmed	Original record remains valid
corrected	Record is updated or amended
rejected	Dispute claim is rejected
partially_accepted	Some parts of dispute are accepted
revoked	Original record is invalidated
merged	Duplicate or related records are merged
escalated	Dispute requires higher-level review
deferred	Decision is postponed due to insufficient evidence
14. Correction Principles

Corrections should preserve auditability.

Recommended approach:

Do not erase history silently.
Add correction records.
Link corrections to original records.
Preserve timestamps.
Record reviewer or governance basis.

A correction should answer:

what changed?
why did it change?
who reviewed it?
when was it corrected?
which records are affected?
15. Correction Example
{
  "type": "correction_note",
  "correction_id": "correction_vcnia_001",
  "target_type": "trace_record",
  "target_id": "trace_vcnia_001",
  "reason": "Parent trace reference was missing from provenance.",
  "change_summary": "Added parent_trace_ids field to provenance metadata.",
  "related_dispute_id": "dispute_vcnia_001",
  "timestamp": "2026-04-27T01:00:00Z"
}

This example is illustrative.
A formal correction schema may be added later.

16. Appeals

A VCNIA-compatible dispute process should allow appeals for high-impact cases.

Appeals may be appropriate when:

new evidence appears,
reviewer conflict of interest is suspected,
process error occurred,
governance rule was misapplied,
decision affects value allocation,
decision affects public trust profile,
decision affects contributor identity or privacy.

Appeal status may be:

not_requested
requested
under_review
accepted
rejected
closed
17. Reviewer Roles

Different disputes may require different reviewers.

Possible reviewer roles include:

human maintainer
governance reviewer
technical reviewer
schema reviewer
privacy reviewer
attribution reviewer
community reviewer
automated validator
multi-agent review system

High-impact disputes should not rely only on automated review.

18. Conflict of Interest

Reviewers should avoid conflicts of interest.

A conflict may exist when the reviewer:

created the disputed record,
benefits from the disputed allocation,
issued the disputed gratitude,
has a direct relationship with claimant or respondent,
controls the relevant governance policy,
has a stake in the outcome.

VCNIA-compatible systems should allow reviewer replacement or escalation when conflicts exist.

19. Privacy in Disputes

Dispute processes can expose sensitive information.

Privacy-sensitive data may include:

identity information,
private source material,
unpublished work,
financial allocation records,
private gratitude messages,
trust history,
internal governance notes.

Privacy safeguards may include:

redaction,
pseudonymous IDs,
private evidence review,
limited reviewer access,
aggregated summaries,
selective disclosure,
retention limits.

Dispute resolution should not become a tool for surveillance or harassment.

20. Abuse of Dispute Process

The dispute process itself can be abused.

Possible abuse patterns include:

harassment through repeated disputes,
false claims,
strategic delay of allocation,
mass dispute spam,
bad-faith attribution claims,
attempts to expose private information,
retaliation through trust disputes.

Possible countermeasures:

rate limits,
evidence requirements,
reviewer discretion,
appeal thresholds,
abuse flags,
temporary restrictions,
transparent process rules.

A fair dispute system must protect both claimants and respondents.

21. Layer-Specific Review Guidance
21.1 Trace Record Review

Review questions:

Does the trace exist?
Is the timestamp plausible?
Is the creator ID correct?
Is provenance complete?
Are parent traces missing?
Is the content hash valid?
Was another person’s work registered improperly?
21.2 Gratitude Event Review

Review questions:

Does the referenced trace exist?
Was gratitude issued by a valid sender?
Is the receiver correct?
Is the impact score reasonable?
Is the message misleading?
Is there evidence of collusion or spam?
Should the event influence trust?
21.3 Trust Event Review

Review questions:

Which trace and gratitude records influenced the trust event?
Was the trust delta proportional?
Were risk flags justified?
Was trust decay applied correctly?
Was the subject given opportunity for correction or appeal?
Was the calculation transparent?
21.4 Value Allocation Review

Review questions:

Which source traces were used?
Which gratitude events influenced allocation?
Which trust profile or trust events were used?
Which allocation rule was applied?
Was the amount calculated correctly?
Was the policy version correct?
Was any disputed record used improperly?
21.5 Governance Policy Review

Review questions:

Was the correct policy version used?
Was the rule applied consistently?
Was the policy change announced?
Did the policy affect prior records retroactively?
Was there a conflict of interest?
Was an appeal path available?
22. Dispute Severity

Disputes may be classified by severity.

Severity	Meaning
Low	Minor metadata error or documentation ambiguity
Medium	Incorrect reference, unclear provenance, or moderate trust impact
High	Trust manipulation, privacy exposure, or value allocation error
Critical	Severe identity, allocation, privacy, or governance failure

Severity helps decide review urgency.

23. Recommended Response Times

For real implementations, response time targets may be useful.

Severity	Suggested Initial Response
Low	14 days
Medium	7 days
High	72 hours
Critical	24 hours

These are illustrative targets, not binding obligations for this repository.

24. Record Freezing

In high-impact disputes, affected records may need temporary freezing.

Freezing may mean:

no further trust influence,
no new value allocation based on the record,
no public display update,
no downstream automated decision,
manual review required before use.

Freezing should be proportional.

A minor metadata dispute should not freeze an entire network.

25. Reversal and Adjustment

Value allocation disputes may require reversal or adjustment.

Possible actions:

no change,
future adjustment,
corrected allocation event,
partial reversal,
full reversal,
compensating allocation,
disputed amount held in reserve.

Monetary systems require legal and accounting review before reversal.

VCNIA only provides the structural concept.

26. Dispute Audit Trail

Every dispute should create an audit trail.

A minimal audit trail may include:

dispute_record
  → evidence_refs
  → review_notes
  → decision
  → correction_record
  → appeal_record

The audit trail should preserve accountability without exposing unnecessary private information.

27. Relationship to Governance

Dispute resolution is part of VCNIA governance.

For governance principles, see:

docs/governance-principles.md

Governance defines the rules.
Dispute resolution handles cases where rules, records, or outcomes are challenged.

28. Relationship to Security

Disputes may reveal security issues.

For example:

repeated false gratitude may indicate trust farming,
fake trace records may indicate provenance spoofing,
allocation manipulation may indicate governance capture,
privacy complaints may indicate data exposure risk.

Security-relevant disputes should be handled according to:

SECURITY.md
29. Relationship to Legal Status

VCNIA dispute resolution is not a court process.

It does not replace:

legal claims,
copyright disputes,
contract enforcement,
employment disputes,
financial complaints,
regulatory processes.

For legal boundaries, see:

docs/legal-status.md

VCNIA dispute resolution provides internal process structure.

Legal enforceability is separate.

30. Minimal Future Schema Candidates

Future VCNIA versions may define schemas such as:

schemas/dispute-record-v0.1.schema.json
schemas/correction-record-v0.1.schema.json
schemas/appeal-record-v0.1.schema.json
schemas/review-event-v0.1.schema.json

These would make dispute resolution machine-readable and testable.

31. Summary

Dispute resolution protects the integrity of VCNIA.

It ensures that:

traces can be challenged,
gratitude can be reviewed,
trust can be corrected,
value allocation can be audited,
privacy can be protected,
governance can be improved.

In short:

Trace without dispute resolution becomes rigid.
Gratitude without dispute resolution becomes noise.
Trust without dispute resolution becomes power.
Royalty without dispute resolution becomes extraction.
32. Closing Statement

A value circulation system must be able to correct itself.

VCNIA does not assume perfect records.

It assumes that records need structure, review, correction, and appeal.

That is not weakness.

It is how circulation remains alive.

Claim → Review → Correction → Trust → Renewal
