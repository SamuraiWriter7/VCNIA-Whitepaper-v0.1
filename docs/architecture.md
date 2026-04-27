# VCNIA Architecture

## Value-Circulating Network Intelligence Architecture

This document describes the architecture of **VCNIA**:  
**Value-Circulating Network Intelligence Architecture**.

VCNIA is a four-layer architecture for network intelligence based on value circulation.

```text
Existence Proof → Gratitude → Trust → Royalty / Value Allocation → Network Intelligence

Its core idea is:

Intelligence emerges where value circulates.

1. Architectural Purpose

VCNIA is designed to explain and structure how intelligence can emerge from a network of humans, AI agents, systems, traces, recognition signals, trust records, and value allocation mechanisms.

Traditional AI architecture often focuses on:

model capability
reasoning ability
task performance
benchmark scores
autonomy
tool use

VCNIA shifts the focus from isolated capability to networked circulation.

In VCNIA, a network becomes intelligent when it can:

record traces,
recognize meaningful contributions,
accumulate trust,
allocate value,
adapt through circulation.
2. High-Level Architecture

VCNIA consists of four primary layers.

┌─────────────────────────────────────────────┐
│ Layer 4: Royalty / Value Allocation Layer    │
│ Returns value based on contribution          │
└─────────────────────────────────────────────┘
                    ↑
┌─────────────────────────────────────────────┐
│ Layer 3: Trust Layer                         │
│ Accumulates structural reliability           │
└─────────────────────────────────────────────┘
                    ↑
┌─────────────────────────────────────────────┐
│ Layer 2: Gratitude Layer                     │
│ Records recognition and impact               │
└─────────────────────────────────────────────┘
                    ↑
┌─────────────────────────────────────────────┐
│ Layer 1: Existence Proof Layer               │
│ Records traces and provenance                │
└─────────────────────────────────────────────┘

The architecture can also be understood as a circulation loop:

Trace Creation
      ↓
Existence Proof
      ↓
Gratitude
      ↓
Trust
      ↓
Value Allocation
      ↓
Value Return
      ↓
New Creation
3. Core Architectural Principle

VCNIA is based on the following principle:

A contribution must first exist as a trace before it can be recognized, trusted, and rewarded.

Therefore, each layer depends on the previous layer.

Layer	Depends On	Produces
Existence Proof	Trace creation	Proven trace
Gratitude	Proven trace	Recognition signal
Trust	Recognition signals	Trust profile
Value Allocation	Trust and contribution records	Value return
Network Intelligence	Full circulation loop	Adaptive intelligence
4. Layer 1: Existence Proof Layer
4.1 Purpose

The Existence Proof Layer records that a trace exists.

It answers:

What existed, when, where, and in what context?

This layer does not determine legal ownership, moral value, or financial reward.
It only establishes that a contribution, action, or output exists as a recordable trace.

4.2 Core Objects

Typical objects in this layer include:

trace_id
creator_id
timestamp
content_hash
provenance
source_uri
context
signature
metadata
4.3 Trace Types

A trace may include:

text
code
prompt
idea
design
image
dataset
review
decision
transformation
AI-generated output
human-authored input
system-generated event
4.4 Function

The Existence Proof Layer performs the following functions:

assigns an identifier to a trace,
records when the trace was created,
records who or what created it,
preserves provenance information,
optionally stores hashes or signatures,
enables later gratitude, trust, and value allocation.
4.5 Minimal Example
{
  "type": "trace_record",
  "trace_id": "trace_001",
  "creator_id": "creator_abc",
  "timestamp": "2026-04-26T00:00:00Z",
  "content_hash": "sha256:examplehash",
  "provenance": {
    "source": "human-authored-note",
    "method": "manual-registration"
  }
}
4.6 Architectural Role

The Existence Proof Layer is the foundation of VCNIA.

Without this layer:

gratitude has no stable target,
trust has no reliable history,
value allocation has no contribution basis,
network intelligence becomes unstable.
5. Layer 2: Gratitude Layer
5.1 Purpose

The Gratitude Layer records recognition or impact.

It answers:

Which trace was appreciated, referenced, used, or recognized?

In VCNIA, gratitude is not merely emotion.
It is a lightweight value signal.

5.2 Core Objects

Typical objects in this layer include:

gratitude_id
trace_id
sender_id
receiver_id
impact_score
message
contribution_ref
timestamp
context
verification_status
5.3 Gratitude Directions

Gratitude may flow in multiple directions:

Direction	Example
Human → Human	A reader thanks an author
Human → AI	A user recognizes an AI-generated contribution
AI → Human	An AI marks a human trace as useful
AI → AI	One agent recognizes another agent’s output
System → Contributor	A platform records contribution impact
Community → Project	A group recognizes an open-source contribution
5.4 Function

The Gratitude Layer performs the following functions:

links recognition to a trace,
records the source of recognition,
records the recipient of recognition,
expresses impact level,
creates a bridge between trace and trust,
enables non-monetary value circulation.
5.5 Minimal Example
{
  "type": "gratitude_event",
  "gratitude_id": "gratitude_001",
  "trace_id": "trace_001",
  "sender_id": "agent_xyz",
  "receiver_id": "creator_abc",
  "impact_score": 0.82,
  "message": "This trace contributed to a later design decision.",
  "timestamp": "2026-04-26T01:00:00Z"
}
5.6 Architectural Role

The Gratitude Layer activates circulation.

A trace may exist without gratitude.
But once gratitude is issued, the trace enters the value circulation process.

In this sense:

Trace + Gratitude = Recognized Contribution
6. Layer 3: Trust Layer
6.1 Purpose

The Trust Layer accumulates gratitude, verification, and contribution history into trust.

It answers:

Which contributors, traces, or agents have demonstrated structural reliability?

In VCNIA, trust is not treated as popularity.
It is treated as accumulated structural reliability.

6.2 Core Objects

Typical objects in this layer include:

trust_profile
trust_event
trust_score
trust_history
dimension_scores
verification_status
risk_flags
decay_factor
updated_at
6.3 Trust Dimensions

Trust may be evaluated across multiple dimensions.

Dimension	Meaning
originality	Degree of distinct contribution
reliability	Consistency of contribution
usefulness	Practical value
integrity	Low manipulation or abuse
citation_quality	Proper relation to sources
long_term_value	Durable contribution
network_contribution	Contribution to the whole system
verification_quality	Strength of supporting evidence
6.4 Function

The Trust Layer performs the following functions:

aggregates gratitude events,
evaluates contribution history,
applies verification signals,
detects manipulation risk,
updates trust profiles,
informs value allocation.
6.5 Minimal Example
{
  "type": "trust_event",
  "trust_event_id": "trust_event_001",
  "subject_id": "creator_abc",
  "related_trace_ids": ["trace_001"],
  "trust_delta": 0.04,
  "reason": "Repeated high-impact gratitude events",
  "timestamp": "2026-04-26T02:00:00Z"
}
6.6 Trust Profile Example
{
  "trust_profile_id": "trust_creator_abc",
  "subject_id": "creator_abc",
  "overall_trust_score": 0.76,
  "dimensions": {
    "originality": 0.84,
    "reliability": 0.73,
    "usefulness": 0.79,
    "integrity": 0.91
  },
  "updated_at": "2026-04-26T02:00:00Z"
}
6.7 Architectural Role

The Trust Layer stabilizes circulation.

Without trust, gratitude may be manipulated.
Without trust, value allocation becomes vulnerable to noise, spam, and popularity bias.

In this sense:

Gratitude + Verification + History = Trust
7. Layer 4: Royalty / Value Allocation Layer
7.1 Purpose

The Royalty / Value Allocation Layer distributes value according to trace, gratitude, trust, and contribution logic.

It answers:

How should value return to contributors?

This layer does not require value to be monetary.
It defines a general mechanism for value return.

7.2 Core Objects

Typical objects in this layer include:

allocation_id
recipient_id
source_trace_ids
trust_profile_ref
allocation_rule
value_type
amount
weight
governance_policy
settlement_period
timestamp
7.3 Value Types

VCNIA can support multiple forms of value.

Value Type	Description
monetary	Money or revenue share
credit	Internal accounting credit
point	Platform-level point
reputation	Public or system-level recognition
access	Access rights or privileges
governance	Voting or decision weight
royalty_share	Share of generated revenue
citation_priority	Preferential attribution
gratitude_token	Non-transferable appreciation mark
7.4 Function

The Value Allocation Layer performs the following functions:

evaluates contribution records,
references trust profiles,
applies allocation rules,
calculates value weights,
records value distribution,
returns value to contributors,
closes the circulation loop.
7.5 Minimal Example
{
  "type": "value_allocation_event",
  "allocation_id": "allocation_001",
  "recipient_id": "creator_abc",
  "source_trace_ids": ["trace_001"],
  "value_type": "credit",
  "amount": 120,
  "weight": 0.42,
  "allocation_rule": "trust_weighted_contribution",
  "settlement_period": "2026-04",
  "timestamp": "2026-04-26T03:00:00Z"
}
7.6 Architectural Role

The Value Allocation Layer closes the loop.

In this sense:

Trust + Contribution Policy = Value Return

Once value returns to contributors, the network becomes capable of supporting further creation.

8. Full Circulation Loop

The complete VCNIA loop can be described as follows:

1. A human or AI creates a trace.
2. The trace is registered in the Existence Proof Layer.
3. Another human, AI, or system recognizes the trace.
4. A gratitude event is issued.
5. Gratitude events accumulate into trust.
6. Trust informs value allocation.
7. Value returns to contributors.
8. Contributors generate new traces.
9. The network adapts through circulation.

This loop is the basic engine of VCNIA.

9. Mermaid Architecture Diagram
flowchart TD
    A[Human or AI Creates Trace] --> B[Existence Proof Layer]
    B --> C[Trace Record]
    C --> D[Gratitude Layer]
    D --> E[Gratitude Event]
    E --> F[Trust Layer]
    F --> G[Trust Profile]
    G --> H[Royalty / Value Allocation Layer]
    H --> I[Value Allocation Event]
    I --> J[Value Return]
    J --> K[New Creation]
    K --> A
10. Data Flow

VCNIA can be represented as a data flow.

trace_record
      ↓
gratitude_event
      ↓
trust_event / trust_profile
      ↓
value_allocation_event
      ↓
network_intelligence_signal

Each event type builds on previous records.

Input	Output
Trace	Trace Record
Trace Record	Gratitude Event
Gratitude Events	Trust Event
Trust History	Trust Profile
Trust Profile + Policy	Value Allocation Event
Value Allocation Events	Network Adaptation
11. Minimal Event Sequence

A minimal VCNIA-compatible event sequence may look like this:

[
  {
    "type": "trace_record",
    "trace_id": "trace_001",
    "creator_id": "creator_abc",
    "timestamp": "2026-04-26T00:00:00Z"
  },
  {
    "type": "gratitude_event",
    "gratitude_id": "gratitude_001",
    "trace_id": "trace_001",
    "sender_id": "agent_xyz",
    "receiver_id": "creator_abc",
    "impact_score": 0.82,
    "timestamp": "2026-04-26T01:00:00Z"
  },
  {
    "type": "trust_event",
    "trust_event_id": "trust_event_001",
    "subject_id": "creator_abc",
    "related_trace_ids": ["trace_001"],
    "trust_delta": 0.04,
    "timestamp": "2026-04-26T02:00:00Z"
  },
  {
    "type": "value_allocation_event",
    "allocation_id": "allocation_001",
    "recipient_id": "creator_abc",
    "source_trace_ids": ["trace_001"],
    "value_type": "credit",
    "amount": 120,
    "timestamp": "2026-04-26T03:00:00Z"
  }
]
12. Relationship Between Layers

VCNIA layers are sequential but not strictly linear.

A trace may receive multiple gratitude events.
A gratitude event may affect multiple trust dimensions.
A trust profile may influence many allocation decisions.
A value allocation event may trigger new traces.

Therefore, VCNIA is best understood as a graph, not a simple pipeline.

Trace Nodes
   ↓
Recognition Edges
   ↓
Trust Graph
   ↓
Value Circulation Network
   ↓
Network Intelligence
13. Network Intelligence in VCNIA

VCNIA defines network intelligence as:

A network structure that generates traces, evaluates the traces of others, forms trust, and circulates value.

Network intelligence is not located in one AI model.

It emerges from the interaction of:

contributors,
traces,
agents,
recognition signals,
trust profiles,
allocation rules,
governance systems,
feedback loops.
14. Architectural Distinction from Conventional AI
Conventional AI Architecture	VCNIA Architecture
Model-centered	Network-centered
Reasoning-centered	Circulation-centered
Output-focused	Trace-focused
Feedback as training signal	Gratitude as value signal
Reputation as popularity	Trust as structural reliability
Value external to the system	Value internal to circulation
Intelligence as capability	Intelligence as adaptive value flow

VCNIA does not deny reasoning ability.
It extends the concept of intelligence beyond reasoning alone.

15. Governance Layer

VCNIA requires governance rules around all four layers.

Governance must define:

who can create trace records,
who can issue gratitude,
how gratitude is verified,
how trust is calculated,
how trust decays,
how disputes are handled,
how allocation rules are changed,
how privacy is protected,
how manipulation is detected,
how human override works.

Governance is not an optional extension.
It is part of the architecture.

16. Security Considerations

VCNIA-compatible systems must address abuse risks.

Possible risks include:

fake traces,
false gratitude,
trust farming,
Sybil attacks,
identity spoofing,
attribution laundering,
artificial impact inflation,
centralized manipulation of trust scores,
value extraction without return.

Possible countermeasures include:

content hashing,
cryptographic signatures,
provenance tracking,
rate limits,
anomaly detection,
multi-source verification,
trust decay,
manual review,
dispute resolution,
transparent allocation rules.
17. Privacy Considerations

Traceability must not become surveillance.

VCNIA-compatible systems should consider:

selective disclosure,
pseudonymous identifiers,
private trace records,
permissioned access,
zero-knowledge proofs,
data minimization,
contributor consent,
retention limits,
human review for sensitive data.

Privacy is especially important when traces include human-authored work, identity information, creative history, or behavioral records.

18. Implementation Levels

VCNIA can be implemented at different levels.

Level	Description
Level 0	Conceptual model only
Level 1	Human-readable documentation
Level 2	JSON Schemas and sample events
Level 3	Validation workflows
Level 4	Simulated value circulation
Level 5	Multi-agent integration
Level 6	Real-world governance and allocation

A repository may begin at Level 1 and gradually evolve toward higher implementation levels.

19. Recommended Repository Modules

A VCNIA repository may include:

README.md
WHITEPAPER.md
docs/
  one-page-overview.md
  architecture.md
  relationship-to-existence-proof-os.md
  relationship-to-gratitude-os.md
  relationship-to-trust-os.md
  relationship-to-royalty-os.md
schemas/
  trace-record-v0.1.schema.json
  gratitude-event-v0.1.schema.json
  trust-event-v0.1.schema.json
  value-allocation-v0.1.schema.json
examples/
  trace-record.sample.json
  gratitude-event.sample.json
  trust-event.sample.json
  value-allocation.sample.json
.github/
  workflows/
    validate-specs.yml
20. Future Architectural Extensions

Future versions of VCNIA may add:

trace graph model,
gratitude receipt protocol,
trust decay model,
value allocation formula,
royalty pool calculation,
AI identity integration,
existence certificate integration,
governance policy schema,
compliance test suite,
simulation engine,
multi-agent evaluation framework,
privacy-preserving trace verification.
21. Summary

VCNIA is a four-layer architecture:

Existence Proof → Gratitude → Trust → Royalty / Value Allocation

Each layer transforms the previous one:

Trace → Recognition → Reliability → Return

When this loop continues, the network becomes more adaptive, stable, and intelligent.

VCNIA therefore defines intelligence not only as reasoning, but as circulation.

Intelligence emerges where value circulates.
