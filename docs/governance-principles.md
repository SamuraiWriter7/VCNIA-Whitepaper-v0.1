# Governance Principles

## Governance Principles for VCNIA

This document defines governance principles for **VCNIA: Value-Circulating Network Intelligence Architecture**.

VCNIA is a conceptual and technical architecture for value-circulating network intelligence.

Its core stack is:

```text
Existence Proof → Gratitude → Trust → Royalty / Value Allocation → Network Intelligence

Its core principle is:

Intelligence emerges where value circulates.
1. Purpose of Governance

Governance in VCNIA exists to ensure that value circulation remains:

transparent,
auditable,
fair,
privacy-aware,
resistant to manipulation,
open to correction,
respectful of human dignity,
compatible with human-AI and AI-to-AI networks.

VCNIA does not treat governance as an optional add-on.

Governance is part of the architecture.

Without governance, trace records may become unreliable, gratitude may become spam, trust may become manipulation, and value allocation may become extraction.

2. Core Governance Principle

The core governance principle of VCNIA is:

No value return without traceability,
no trust without verification,
no allocation without auditability.

In simpler form:

Trace → Recognition → Reliability → Return

Each stage should be reviewable before it influences the next stage.

3. Governance Across the Four Layers

VCNIA governance must apply to all four layers.

Layer	Governance Question
Existence Proof	Who can register traces, and how are they verified?
Gratitude	Who can issue gratitude, and how is abuse prevented?
Trust	How is trust calculated, updated, challenged, and recovered?
Royalty / Value Allocation	How is value allocated, audited, and disputed?

Governance should not begin only at the value allocation stage.

It must begin at trace registration.

4. Principle 1: Transparency

Rules should be visible and understandable.

VCNIA-compatible systems should clearly explain:

what records are created,
who can create them,
how they are verified,
how trust is calculated,
how value is allocated,
how disputes are handled,
how privacy is protected.

A system that circulates value through hidden rules cannot be trusted.

Opaque circulation becomes extraction.
Transparent circulation becomes governance.
5. Principle 2: Auditability

Important events should be reviewable.

A value allocation event should be traceable back through the stack:

value_allocation_event
  → trust_event / trust_profile
  → gratitude_event
  → trace_record

Auditability helps answer:

why was value allocated?
which traces contributed?
which gratitude events were used?
which trust profile influenced the decision?
which governance policy was applied?

Without auditability, value allocation becomes a black box.

6. Principle 3: Separation of Layers

VCNIA layers should not be collapsed into one another.

Important distinctions:

Existence proof is not ownership proof.
Gratitude is not payment.
Trust is not legal certification.
Royalty is not automatic legal entitlement.

Each layer has a different role.

Layer	What It Means	What It Does Not Mean
Existence Proof	A trace exists	Legal ownership is proven
Gratitude	A trace was recognized	Payment is owed
Trust	Reliability signal exists	Legal certification exists
Value Allocation	Value was returned	Universal legal entitlement exists

Keeping these distinctions clear prevents confusion and abuse.

7. Principle 4: Verification Before Influence

A record should not strongly influence trust or value allocation unless its verification status is clear.

VCNIA records may use verification states such as:

unverified
self_attested
system_verified
human_verified
multi_source_verified
disputed
rejected

Governance should define how each verification status affects downstream use.

For example:

Verification Status	Suggested Use
unverified	Store only, low influence
self_attested	Limited influence
system_verified	Moderate influence
human_verified	Stronger influence
multi_source_verified	Strongest influence
disputed	Pause or reduce influence
rejected	Exclude from allocation
8. Principle 5: Anti-Manipulation

VCNIA-compatible systems should resist manipulation.

Possible manipulation patterns include:

fake trace registration,
false gratitude,
gratitude spam,
trust farming,
Sybil attacks,
attribution laundering,
collusive value loops,
artificial impact inflation,
duplicate contribution claims,
centralized manipulation of allocation rules.

Governance should include detection and response mechanisms.

Possible countermeasures:

rate limits,
anomaly detection,
multi-source verification,
trust decay,
human review,
dispute procedures,
transparent formulas,
audit logs,
identity safeguards.
9. Principle 6: Privacy Protection

Traceability must not become surveillance.

VCNIA records may include sensitive data such as:

contributor identifiers,
timestamps,
source URIs,
provenance history,
gratitude messages,
trust histories,
allocation records.

Governance should support:

data minimization,
pseudonymous identifiers,
selective disclosure,
permissioned access,
private trace records,
redaction mechanisms,
retention limits,
contributor consent,
privacy-preserving verification.

The goal is not to expose everything.

The goal is to preserve enough structure for fair circulation.

Transparency for governance.
Privacy for dignity.
10. Principle 7: Human Review for High-Impact Decisions

Automation can support VCNIA governance, but high-impact decisions should allow human review.

High-impact cases include:

negative trust events,
disputed attribution,
suspected manipulation,
exclusion from value allocation,
monetary allocation,
public trust scoring,
identity conflict,
sensitive trace disclosure.

AI systems may assist with review, but should not become unquestionable authorities.

AI may recommend.
Governance must decide.
11. Principle 8: Dispute Resolution

VCNIA-compatible systems should include dispute resolution.

Disputes may involve:

trace authorship,
provenance accuracy,
false gratitude,
trust score changes,
value allocation weights,
duplicate claims,
identity conflicts,
privacy concerns,
governance rule interpretation.

A minimal dispute flow:

Claim → Evidence Review → Decision → Correction / Rejection → Appeal

Dispute records should be:

documented,
reviewable,
proportionate,
privacy-aware,
open to correction.

A system without dispute resolution cannot fairly handle value circulation.

12. Principle 9: Trust Must Be Dynamic

Trust should not be permanent or fatalistic.

Trust should be:

earned,
updated,
reviewable,
contextual,
recoverable,
decay-aware.

Trust may increase through:

verified contribution,
repeated recognition,
high-quality references,
long-term usefulness,
integrity,
collaboration.

Trust may decrease through:

manipulation,
false claims,
disputed records,
low-quality attribution,
repeated abuse,
outdated relevance.

Trust recovery should also be possible.

Trust without recovery becomes punishment.
Trust without decay becomes stagnation.
13. Principle 10: Dimensional Trust

VCNIA should avoid reducing trust to a single simplistic score.

Trust may include multiple dimensions:

originality,
reliability,
usefulness,
integrity,
citation quality,
verification quality,
long-term value,
network contribution,
collaboration quality,
governance alignment.

Dimensional trust allows more nuanced governance.

For example, a contributor may be highly original but weak in citation quality.
Another may be highly reliable but less innovative.

A single score hides these distinctions.

14. Principle 11: Proportionality

Value allocation should be proportional to contribution, confidence, and context.

Governance should avoid:

rewarding only visibility,
over-amplifying weak signals,
converting every gratitude event into value,
treating popularity as reliability,
ignoring indirect contributors,
allocating value without auditability.

Proportionality means that value return should reflect structured contribution, not noise.

15. Principle 12: Plurality of Value Systems

Different communities may define value differently.

VCNIA should not impose one universal value model.

Some communities may value:

originality,
accuracy,
usefulness,
care,
maintenance,
review,
governance,
openness,
long-term stability,
creative influence.

Governance should allow community-specific policies while preserving core VCNIA distinctions.

One architecture.
Many value cultures.
16. Principle 13: Non-Extraction

VCNIA is designed to prevent one-way extraction.

A value-circulating network should not only collect traces, gratitude, and trust.

It should also return value.

Without value return:

Creation → Trace → Use → Extraction

With value return:

Creation → Trace → Gratitude → Trust → Return → New Creation

Governance should ensure that value does not remain permanently trapped in platforms, systems, or downstream users.

17. Principle 14: AI-Agent Accountability

VCNIA may include AI agents as participants.

AI agents may:

create traces,
issue gratitude,
evaluate trust,
recommend allocation,
participate in workflows.

Governance should define:

how AI agents are identified,
what AI agents are allowed to do,
whether AI agents can issue gratitude,
whether AI agents can influence trust,
whether AI agents can recommend allocation,
when human review is required,
how self-referential AI loops are prevented.

AI-agent participation does not imply AI legal personhood.

18. Principle 15: Separation of Roles

High-integrity systems should separate key roles.

Possible roles include:

trace creator,
trace registrar,
gratitude issuer,
trust evaluator,
allocation calculator,
governance reviewer,
dispute resolver,
auditor.

A single entity should not control all stages without review.

Separation of roles reduces capture and manipulation.

Generate ≠ Verify ≠ Allocate ≠ Audit
19. Principle 16: Explainability

VCNIA-compatible decisions should be explainable.

For important outcomes, systems should be able to answer:

what happened?
which records were used?
what rule was applied?
why did trust change?
why was value allocated?
what can be disputed?
how can correction occur?

Explainability is especially important for:

trust changes,
negative events,
allocation decisions,
disputed records,
governance updates.
20. Principle 17: Versioned Governance

Governance policies should be versioned.

A record should be able to reference the policy that governed it.

Example:

{
  "governance_policy": {
    "policy_id": "vcnia-governance-policy",
    "policy_version": "0.1.0",
    "policy_uri": "https://example.org/vcnia/governance-policy-v0.1"
  }
}

Versioning helps preserve auditability when governance rules change.

21. Principle 18: Minimal Necessary Data

VCNIA-compatible systems should collect only the data necessary for value circulation.

Avoid collecting excessive:

personal identity data,
behavioral history,
private messages,
sensitive provenance,
unnecessary timestamps,
social relationship data.

More data does not automatically mean better governance.

Sometimes, it means more risk.

Collect enough to govern.
Do not collect enough to surveil.
22. Principle 19: Open Correction

VCNIA records should be correctable where appropriate.

Possible correction types include:

metadata correction,
provenance update,
duplicate trace merge,
gratitude retraction,
trust event correction,
allocation adjustment,
dispute status update.

Correction should preserve audit history where possible.

A corrected system should not erase the fact that correction occurred.

23. Principle 20: Safe Defaults

VCNIA implementations should use safe defaults.

Recommended defaults:

unverified records should have limited influence,
disputed records should not drive high-value allocation,
private records should not become public by default,
AI-generated trust updates should require review for high-impact cases,
monetary allocation should require stronger governance than non-monetary recognition,
schema validation should not be treated as truth verification.

Safe defaults protect the system before it becomes mature.

24. Governance Objects

Future VCNIA implementations may define structured governance objects.

Examples:

governance_policy
dispute_record
appeal_record
audit_record
review_event
verification_event
allocation_policy
privacy_policy
agent_permission_profile

These may become future schemas.

25. Minimal Governance Policy Example

A minimal governance policy may include:

{
  "policy_id": "vcnia-governance-policy",
  "policy_version": "0.1.0",
  "scope": "VCNIA v0.1 four-layer stack",
  "trace_registration": {
    "default_verification_status": "self_attested",
    "requires_content_hash": false
  },
  "gratitude": {
    "ai_agents_can_issue": true,
    "impact_score_range": [0, 1],
    "requires_trace_id": true
  },
  "trust": {
    "uses_dimensional_trust": true,
    "supports_decay": true,
    "supports_recovery": true
  },
  "value_allocation": {
    "monetary_allocation_enabled": false,
    "requires_audit_path": true,
    "requires_dispute_process": true
  },
  "privacy": {
    "pseudonymous_ids_allowed": true,
    "selective_disclosure_supported": true
  }
}

This is illustrative only.

Formal governance schemas may be added in future versions.

26. Governance Failure Modes

Governance should be designed against common failure modes.

Failure Mode	Description
Trace Capture	A platform records traces but does not return value
Gratitude Inflation	Recognition signals become spam or manipulation
Trust Farming	Actors artificially inflate reliability
Allocation Capture	A central actor controls value distribution unfairly
Metric Reduction	Complex contribution is reduced to a single score
Surveillance Drift	Traceability becomes behavioral monitoring
Dispute Suppression	Contributors cannot challenge records
AI Loop Inflation	AI agents amplify each other without real contribution
Policy Drift	Governance rules change without auditability
27. Governance Maturity Levels

VCNIA governance can mature gradually.

Level	Description
Level 0	No explicit governance
Level 1	Human-readable governance principles
Level 2	Versioned governance policy
Level 3	Dispute resolution process
Level 4	Audit trails and review logs
Level 5	Privacy-preserving verification
Level 6	Multi-agent governance
Level 7	Regulated value allocation

VCNIA v0.1 begins at the human-readable principle level.

28. Relationship to Legal Status

Governance is not the same as law.

VCNIA governance may define internal system rules, but legal enforceability depends on external legal systems.

Important distinction:

Governance provides process.
Law provides enforceability.
Implementation provides responsibility.

For legal boundaries, see:

docs/legal-status.md
29. Relationship to Security

Governance and security are deeply connected.

Security protects records from manipulation.
Governance defines how records should be used.

A technically secure system can still be unfair if governance is poor.

A well-governed system can still fail if security is weak.

VCNIA requires both.

Security without governance is rigid.
Governance without security is fragile.
30. Summary

VCNIA governance exists to preserve the integrity of value circulation.

It should ensure that:

traces are recorded responsibly,
gratitude remains meaningful,
trust remains reliable,
value allocation remains fair,
privacy is protected,
disputes can be resolved,
AI agents are accountable,
contributors are treated with dignity.

In short:

Good governance keeps value circulation from becoming extraction.
31. Closing Statement

VCNIA is not only about recording value.

It is about returning value wisely.

That requires governance.

A network that remembers traces but cannot govern them becomes unstable.
A network that recognizes contribution but cannot verify it becomes noisy.
A network that allocates value but cannot audit it becomes extractive.

Governance is the structure that keeps circulation alive.

Trace with governance becomes memory.
Gratitude with governance becomes recognition.
Trust with governance becomes reliability.
Royalty with governance becomes renewal.
