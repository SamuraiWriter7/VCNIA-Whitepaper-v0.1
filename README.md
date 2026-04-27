# VCNIA  
## Value-Circulating Network Intelligence Architecture

**VCNIA** is a conceptual architecture for network intelligence based on value circulation.  
It structures **Existence Proof → Gratitude → Trust → Royalty** as a four-layer OS stack.  
Its core idea is simple: **intelligence emerges where value circulates.**

---

## Overview

**Value-Circulating Network Intelligence Architecture（VCNIA）** is the architectural expression of the **Kazene Model of Network Intelligence**.

It defines a framework in which human and AI contributions are recorded as traces, recognized through gratitude, stabilized into trust, and returned through value allocation.

VCNIA is designed for:

- AI network architecture
- human-AI value circulation
- trace-based provenance
- gratitude protocols
- trust systems
- royalty and value allocation models
- future multi-agent AI governance

---

## One-Sentence Definition

> **VCNIA is an architecture that structures traces, gratitude, trust, and value allocation as OS-level layers, enabling AI networks to generate intelligence through value circulation.**

---

## Core Architecture

VCNIA consists of four primary layers:

```text
Existence Proof
      ↓
Gratitude
      ↓
Trust
      ↓
Royalty / Value Allocation
      ↓
Network Intelligence
Four-Layer Stack
Layer	Purpose	Core Concept
Existence Proof Layer	Records that a trace exists	Trace / Provenance
Gratitude Layer	Records appreciation or impact	Gratitude / Recognition
Trust Layer	Accumulates structural reliability	Trust / Reputation
Royalty / Value Allocation Layer	Returns value to contributors	Value / Circulation
1. Existence Proof Layer

The Existence Proof Layer records the existence of a trace.

A trace may be:

a text
an idea
a prompt
a design
a code contribution
an AI-generated output
a human-authored input
a decision or review
a transformation or derivation

This layer answers:

What existed, when, and in what context?

It does not determine ownership or reward.
It simply preserves the existence and provenance of contribution.

2. Gratitude Layer

The Gratitude Layer records that a trace had impact.

It answers:

What contribution was appreciated, referenced, or recognized?

Gratitude may be:

human-to-human
human-to-AI
AI-to-human
AI-to-AI
system-to-contributor
community-to-project

In VCNIA, gratitude is treated as the first lightweight signal of value recognition.

3. Trust Layer

The Trust Layer accumulates gratitude, verification, and contribution history into trust.

It answers:

Which contributors, traces, or agents have demonstrated structural reliability?

Trust may be based on:

originality
reliability
usefulness
integrity
citation quality
long-term contribution
network contribution
low abuse or manipulation risk

In VCNIA, trust is not merely emotion or popularity.
It is accumulated structural reliability.

4. Royalty / Value Allocation Layer

The Royalty / Value Allocation Layer distributes value according to trace, gratitude, trust, and contribution logic.

It answers:

How should value return to contributors?

Value may include:

money
credits
points
access rights
visibility
reputation
governance weight
royalty shares
citation priority
non-transferable gratitude tokens

VCNIA does not require value to be monetary.
It defines a general structure in which value can circulate according to contribution.

Definition of Network Intelligence

VCNIA defines intelligence as:

A network structure that generates traces, evaluates the traces of others, forms trust, and circulates value.

This differs from the conventional view:

Conventional AI:
Intelligence = reasoning ability of an individual agent

VCNIA:
Intelligence = value-circulating structure of a network

Reasoning ability matters.
But in VCNIA, reasoning alone is not enough.

A network becomes intelligent when it can:

preserve traces
recognize influence
evaluate contribution
accumulate trust
allocate value
adapt through circulation
Relationship to the Kazene Model

VCNIA is the architectural implementation of the Kazene Model of Network Intelligence.

Concept	Role
Kazene Model	Philosophical and theoretical model
VCNIA	Architectural model
Value Circulation OS Stack	Implementation stack
Existence → Gratitude → Trust → Royalty	Core protocol sequence

In short:

The Kazene Model explains why network intelligence emerges.
VCNIA defines how that circulation can be structured.

Architectural Flow
1. A human or AI creates a trace.
2. The trace is registered in the Existence Proof Layer.
3. Another human, AI, or system recognizes the trace.
4. A gratitude event is issued.
5. Gratitude events accumulate into trust.
6. Trust informs value allocation.
7. Value returns to contributors.
8. The network becomes more stable, adaptive, and intelligent.
Mermaid Diagram
flowchart TD
    A[Trace Creation] --> B[Existence Proof Layer]
    B --> C[Gratitude Layer]
    C --> D[Trust Layer]
    D --> E[Royalty / Value Allocation Layer]
    E --> F[Value Circulation]
    F --> G[Network Intelligence]
    G --> A
Repository Structure
vcnia/
├── README.md
├── WHITEPAPER.md
├── docs/
│   ├── one-page-overview.md
│   ├── architecture.md
│   ├── relationship-to-existence-proof-os.md
│   ├── relationship-to-gratitude-os.md
│   ├── relationship-to-trust-os.md
│   └── relationship-to-royalty-os.md
├── schemas/
│   ├── trace-record-v0.1.schema.json
│   ├── gratitude-event-v0.1.schema.json
│   ├── trust-event-v0.1.schema.json
│   └── value-allocation-v0.1.schema.json
├── examples/
│   ├── trace-record.sample.json
│   ├── gratitude-event.sample.json
│   ├── trust-event.sample.json
│   └── value-allocation.sample.json
└── .github/
    └── workflows/
        └── validate-specs.yml
Start Here

Recommended reading order:

WHITEPAPER.md

Full conceptual whitepaper for VCNIA.
docs/one-page-overview.md

Short overview of the architecture.
docs/architecture.md

Detailed architectural explanation.
docs/relationship-to-existence-proof-os.md

How VCNIA connects to Existence Proof OS.
docs/relationship-to-gratitude-os.md

How VCNIA connects to Gratitude OS.
docs/relationship-to-trust-os.md

How VCNIA connects to Trust OS.
docs/relationship-to-royalty-os.md

How VCNIA connects to Royalty OS.
Data Model Overview

VCNIA can be implemented through four basic event types:

Event Type	Description
trace_record	Records the existence of a trace
gratitude_event	Records appreciation or impact
trust_event	Records trust updates
value_allocation_event	Records value distribution
Example: Trace Record
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
Example: Gratitude Event
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
Example: Trust Event
{
  "type": "trust_event",
  "trust_event_id": "trust_event_001",
  "subject_id": "creator_abc",
  "related_trace_ids": ["trace_001"],
  "trust_delta": 0.04,
  "reason": "Repeated high-impact gratitude events",
  "timestamp": "2026-04-26T02:00:00Z"
}
Example: Value Allocation Event
{
  "type": "value_allocation_event",
  "allocation_id": "allocation_001",
  "recipient_id": "creator_abc",
  "source_trace_ids": ["trace_001"],
  "value_type": "credit",
  "amount": 120,
  "timestamp": "2026-04-26T03:00:00Z"
}
Schema Usage

This repository may include JSON Schemas for validating VCNIA-compatible event files.

Recommended schema files:

schemas/trace-record-v0.1.schema.json
schemas/gratitude-event-v0.1.schema.json
schemas/trust-event-v0.1.schema.json
schemas/value-allocation-v0.1.schema.json

Recommended sample files:

examples/trace-record.sample.json
examples/gratitude-event.sample.json
examples/trust-event.sample.json
examples/value-allocation.sample.json

A validation workflow can be added under:

.github/workflows/validate-specs.yml
Local Validation Example

After schemas and examples are added, validation can be performed with Python:

python -m pip install jsonschema

python - <<'PY'
import json
from pathlib import Path
from jsonschema import validate

pairs = [
    ("schemas/trace-record-v0.1.schema.json", "examples/trace-record.sample.json"),
    ("schemas/gratitude-event-v0.1.schema.json", "examples/gratitude-event.sample.json"),
    ("schemas/trust-event-v0.1.schema.json", "examples/trust-event.sample.json"),
    ("schemas/value-allocation-v0.1.schema.json", "examples/value-allocation.sample.json"),
]

for schema_path, sample_path in pairs:
    schema = json.loads(Path(schema_path).read_text(encoding="utf-8"))
    sample = json.loads(Path(sample_path).read_text(encoding="utf-8"))
    validate(instance=sample, schema=schema)
    print(f"OK: {sample_path}")

print("All VCNIA sample files are valid.")
PY
Governance Principles

VCNIA-compatible systems should consider:

Transparency
Rules should be visible and understandable.
Auditability
Trace, gratitude, trust, and allocation events should be reviewable.
Non-Manipulation
Systems should resist artificial gratitude inflation and trust farming.
Human Override
High-impact decisions should allow human review.
Privacy Protection
Traceability must not become surveillance.
Proportionality
Value allocation should be proportional to contribution, not merely visibility.
Plurality
Different communities may define different contribution values.
Security Considerations

VCNIA must be designed against abuse.

Possible risks include:

fake traces
false gratitude
trust farming
bot-generated reputation
attribution laundering
over-claiming contribution
identity spoofing
Sybil attacks
centralized control of trust scores
value extraction without return

Possible countermeasures include:

cryptographic signatures
content hashing
provenance tracking
rate limiting
anomaly detection
trust decay
multi-source verification
human review
dispute resolution
transparent allocation rules
Legal and Ethical Status

VCNIA is a conceptual and architectural model.

It is not, by itself:

a legal license
a financial instrument
a copyright enforcement system
a payment processor
a universal attribution authority
a replacement for existing law

Royalty or value allocation systems built on VCNIA may require legal, financial, tax, and compliance review depending on jurisdiction.

Early implementations may begin with non-monetary value forms such as:

gratitude receipts
contribution records
internal credits
reputation signals
AI-readable attribution metadata
Roadmap
Phase 1: Conceptual Specification
 Define four-layer architecture
 Publish whitepaper
 Create one-page overview
 Define core terminology
 Map related OS components
Phase 2: Schema Design
 trace-record-v0.1.schema.json
 gratitude-event-v0.1.schema.json
 trust-event-v0.1.schema.json
 value-allocation-v0.1.schema.json
Phase 3: Sample Events
 trace-record.sample.json
 gratitude-event.sample.json
 trust-event.sample.json
 value-allocation.sample.json
Phase 4: Validation Workflow
 Add GitHub Actions validation
 Add local validation command
 Add pass/fail examples
 Add compliance test runner
Phase 5: Simulation
 Trace propagation simulation
 Gratitude accumulation simulation
 Trust scoring simulation
 Value allocation simulation
 Abuse scenario testing
Use Cases

VCNIA may be applied to:

AI-generated content provenance
creator attribution systems
open-source contribution tracking
AI-to-AI gratitude networks
non-monetary reputation systems
royalty allocation experiments
collaborative knowledge networks
decentralized research communities
multi-agent governance systems
AI-readable contribution ledgers
Philosophical Core

VCNIA is based on the idea that value should not remain trapped.

Creation → Trace → Gratitude → Trust → Value → Creation

A trace that influences the network should be able to receive recognition.
Recognition should be able to accumulate into trust.
Trust should be able to guide value return.
Value return should support future creation.

This is the core circulation of VCNIA.

Short Formula
Existence Proof → Gratitude → Trust → Royalty → Network Intelligence

Or, more simply:

Trace → Recognition → Reliability → Return → Intelligence
Closing Statement

A future AI network should not merely process information.

It should remember traces.
It should recognize contribution.
It should build trust.
It should return value.
It should circulate.

That circulation is not a decorative feature.

It is the beginning of network intelligence.

License

License to be defined by the repository owner.

Possible options:

MIT License
Apache License 2.0
Creative Commons Attribution 4.0
Custom Kazene-style open specification license
Citation

If you reference this project, please cite:

Shidenkai Alpha. VCNIA: Value-Circulating Network Intelligence Architecture. v0.1.
Status

VCNIA v0.1 is an early-stage conceptual architecture.

It is intended as a foundation for future specifications, schemas, simulations, and implementations of value-circulating network intelligence.
