# Schema Usage

## Schema Usage for VCNIA

This document explains how to use the JSON Schemas included in **VCNIA: Value-Circulating Network Intelligence Architecture**.

VCNIA defines a four-layer value circulation stack:

```text
Existence Proof → Gratitude → Trust → Royalty / Value Allocation → Network Intelligence

The current v0.1 schema set validates the four core event types used in this stack.

1. Purpose

The purpose of the VCNIA schemas is to provide machine-readable structures for recording:

trace existence,
gratitude and recognition,
trust updates,
value allocation events.

These schemas allow implementations to check whether records follow the expected structure.

Important distinction:

Schema-valid does not mean truth-verified.

Schema validation confirms structure.
It does not prove authorship, ownership, legal status, factual truth, or fairness.

2. Current Schema Files

VCNIA v0.1 includes the following JSON Schemas:

schemas/trace-record-v0.1.schema.json
schemas/gratitude-event-v0.1.schema.json
schemas/trust-event-v0.1.schema.json
schemas/value-allocation-v0.1.schema.json

Each schema corresponds to one layer of the VCNIA stack.

Layer	Schema	Event Type
Existence Proof	trace-record-v0.1.schema.json	trace_record
Gratitude	gratitude-event-v0.1.schema.json	gratitude_event
Trust	trust-event-v0.1.schema.json	trust_event
Royalty / Value Allocation	value-allocation-v0.1.schema.json	value_allocation_event
3. Current Sample Files

VCNIA v0.1 includes the following sample files:

examples/trace-record.sample.json
examples/gratitude-event.sample.json
examples/trust-event.sample.json
examples/value-allocation.sample.json

Each sample file is designed to validate against its corresponding schema.

Sample	Schema
examples/trace-record.sample.json	schemas/trace-record-v0.1.schema.json
examples/gratitude-event.sample.json	schemas/gratitude-event-v0.1.schema.json
examples/trust-event.sample.json	schemas/trust-event-v0.1.schema.json
examples/value-allocation.sample.json	schemas/value-allocation-v0.1.schema.json
4. Validation Flow

The basic validation flow is:

Schema file + Sample file → JSON Schema validator → Pass / Fail

Example:

schemas/trace-record-v0.1.schema.json
        +
examples/trace-record.sample.json
        ↓
Validation result

If the sample follows the schema, validation passes.

If required fields are missing, field types are incorrect, IDs do not match patterns, or values fall outside allowed ranges, validation fails.

5. Install Dependencies

VCNIA schema validation can be performed with Python.

Install the required package:

python -m pip install jsonschema

The repository GitHub Actions workflow uses:

jsonschema

No special runtime is required beyond Python and the JSON Schema validator.

6. Local Validation Command

Run the following command from the repository root:

python - <<'PY'
import json
from pathlib import Path
from jsonschema import Draft202012Validator, FormatChecker

pairs = [
    ("schemas/trace-record-v0.1.schema.json", "examples/trace-record.sample.json"),
    ("schemas/gratitude-event-v0.1.schema.json", "examples/gratitude-event.sample.json"),
    ("schemas/trust-event-v0.1.schema.json", "examples/trust-event.sample.json"),
    ("schemas/value-allocation-v0.1.schema.json", "examples/value-allocation.sample.json"),
]

failed = False

for schema_path, sample_path in pairs:
    print(f"\n=== Validating {sample_path} ===")
    print(f"Schema: {schema_path}")

    schema = json.loads(Path(schema_path).read_text(encoding="utf-8"))
    sample = json.loads(Path(sample_path).read_text(encoding="utf-8"))

    Draft202012Validator.check_schema(schema)

    validator = Draft202012Validator(
        schema,
        format_checker=FormatChecker()
    )

    errors = sorted(
        validator.iter_errors(sample),
        key=lambda e: list(e.path)
    )

    if errors:
        failed = True
        print("ERROR: sample is invalid.")
        for error in errors:
            path = ".".join(str(p) for p in error.path) or "<root>"
            print(f"  - Path: {path}")
            print(f"    Message: {error.message}")
    else:
        print("OK: sample is valid.")

if failed:
    raise SystemExit(1)

print("\nAll VCNIA sample files are valid.")
PY

Expected successful output:

OK: sample is valid.
OK: sample is valid.
OK: sample is valid.
OK: sample is valid.

All VCNIA sample files are valid.
7. GitHub Actions Validation

This repository includes an automated validation workflow:

.github/workflows/validate-specs.yml

The workflow runs when changes are made to:

schemas/**
examples/**
.github/workflows/validate-specs.yml

It validates all current schema/sample pairs.

If validation succeeds, GitHub Actions will show a green check.

If validation fails, the workflow output will show the failing file, path, and error message.

8. Expected Repository Structure

The validation workflow expects this structure:

vcnia/
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

If a file is renamed or moved, update the validation workflow accordingly.

9. Schema Design Rules

VCNIA v0.1 schemas follow these design rules:

Use JSON Schema Draft 2020-12.
Keep core event objects strict with additionalProperties: false.
Use stable event type constants such as trace_record.
Use predictable ID patterns.
Use ISO 8601 date-time strings for timestamps.
Use normalized scores where possible.
Keep metadata flexible through metadata.
Separate trace, gratitude, trust, and allocation layers.
Avoid mixing legal claims into schema validation.
Treat verification status as a field, not as guaranteed truth.
10. Event Type Constants

Each schema requires a fixed type value.

Schema	Required type
Trace Record	trace_record
Gratitude Event	gratitude_event
Trust Event	trust_event
Value Allocation Event	value_allocation_event

Example:

{
  "type": "trace_record"
}

If the type value is incorrect, validation fails.

11. ID Patterns

VCNIA v0.1 uses simple prefix-based IDs.

Object	Pattern	Example
Trace ID	trace_*	trace_vcnia_001
Gratitude ID	gratitude_*	gratitude_vcnia_001
Trust Event ID	trust_event_*	trust_event_vcnia_001
Allocation ID	allocation_*	allocation_vcnia_001

These patterns are used to make records easy to inspect and link.

12. Timestamps

All timestamps should use ISO 8601 date-time format.

Example:

{
  "timestamp": "2026-04-26T00:00:00Z"
}

Recommended format:

YYYY-MM-DDTHH:MM:SSZ
13. Verification Status

Several schemas include verification_status.

Current allowed values include:

unverified
self_attested
system_verified
human_verified
multi_source_verified
disputed
rejected

Important:

verification_status is a claim about review state.
It is not proof of truth by itself.

For example, self_attested means the issuer has asserted the record.
It does not mean independent verification has occurred.

14. Risk Flags

Trust and value allocation records may include risk_flags.

Examples include:

none
possible_spam
possible_sybil_attack
possible_trust_farming
possible_false_gratitude
possible_identity_spoofing
possible_attribution_laundering
possible_collusion
possible_manipulation
disputed_claim
other

Risk flags are warning signals.

They do not automatically prove abuse, but they help governance systems detect potential issues.

15. Metadata

Most schemas include a flexible metadata object.

Example:

{
  "metadata": {
    "status": "sample",
    "license": "to-be-defined",
    "notes": "Example metadata."
  }
}

The metadata field is intended for implementation-specific information.

Use it carefully.

Do not place high-stakes core logic only inside metadata if that logic should be validated by the schema.

16. Context

Most schemas also include a flexible context object.

Example:

{
  "context": {
    "project": "vcnia",
    "layer": "existence-proof",
    "document": "WHITEPAPER.md",
    "version": "0.1.0"
  }
}

The context field helps describe where and why a record was created.

17. Common Validation Errors
Missing required field

Example:

'type' is a required property

Fix:

{
  "type": "trace_record"
}
Wrong event type

Example:

'trace' was expected to be equal to constant 'trace_record'

Fix:

{
  "type": "trace_record"
}
Invalid ID pattern

Example:

'vcnia_001' does not match '^trace_[A-Za-z0-9._-]+$'

Fix:

{
  "trace_id": "trace_vcnia_001"
}
Invalid timestamp

Example:

'2026/04/26' is not a 'date-time'

Fix:

{
  "timestamp": "2026-04-26T00:00:00Z"
}
Additional properties not allowed

Example:

Additional properties are not allowed

This happens when a field is not defined in the schema.

Fix options:

Remove the unsupported field.
Move implementation-specific data into metadata.
Update the schema if the field should become part of the standard.
18. Adding a New Schema

When adding a new schema:

Place it under schemas/.
Use a versioned filename.
Add a matching sample under examples/.
Add the schema/sample pair to .github/workflows/validate-specs.yml.
Update README.md if the schema is part of the public stack.
Update CHANGELOG.md.

Recommended naming:

schemas/example-event-v0.1.schema.json
examples/example-event.sample.json
19. Adding a New Field

When adding a new field to an existing schema:

Decide whether the field is required or optional.
Add a clear description.
Define the type strictly.
Add enum values if the field has limited options.
Update sample files.
Run validation.
Record the change in CHANGELOG.md.

If the change breaks existing valid examples, consider whether the version should be updated.

20. Versioning Guidance

VCNIA uses a simple versioning model:

MAJOR.MINOR.PATCH
MAJOR: Breaking architectural or schema changes
MINOR: New compatible layers, documents, schemas, or examples
PATCH: Fixes, clarifications, validation updates, or documentation improvements

Example:

0.1.0
0.1.1
0.2.0
1.0.0

Schema filenames should remain versioned.

Example:

trace-record-v0.1.schema.json
trace-record-v0.2.schema.json
21. Recommended Validation Policy

For VCNIA-compatible repositories:

Every schema should have at least one valid sample.
Every sample should be validated in CI.
Invalid examples should be stored separately if added later.
Validation errors should be visible in CI logs.
Schema changes should update examples.
Governance-sensitive fields should be documented.
Trust and allocation schemas should be reviewed carefully before release.
22. What Validation Does Not Prove

Schema validation does not prove:

the trace really existed,
the creator is authentic,
the provenance is true,
the gratitude is sincere,
the trust score is fair,
the allocation amount is justified,
the record is legally enforceable,
the implementation is secure.

Validation is structural.

Governance, verification, audit, and legal review are separate layers.

23. Minimal Validation Interpretation

A valid VCNIA record means:

This record follows the expected structure for its event type.

It does not mean:

This record is true, fair, legal, final, or payable.

This distinction should be preserved in all implementations.

24. Future Schema Extensions

Future VCNIA schema work may include:

trust-profile-v0.1.schema.json
governance-policy-v0.1.schema.json
dispute-record-v0.1.schema.json
audit-record-v0.1.schema.json
verification-event-v0.1.schema.json
agent-identity-v0.1.schema.json
royalty-pool-v0.1.schema.json
network-intelligence-signal-v0.1.schema.json

These should be added gradually as the architecture matures.

25. Summary

VCNIA schemas provide a validation-ready structure for the four core event types:

trace_record
gratitude_event
trust_event
value_allocation_event

Together, they support the basic circulation loop:

Trace → Recognition → Reliability → Return

A green validation result means the records are structurally valid.

It does not mean they are legally valid, factually true, or ethically sufficient.

In VCNIA:

Schemas define structure.
Governance defines process.
Verification supports trust.
Implementation carries responsibility.
