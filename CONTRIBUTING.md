# Contributing to VCNIA

Thank you for your interest in contributing to **VCNIA: Value-Circulating Network Intelligence Architecture**.

VCNIA is an early-stage conceptual and technical specification for value-circulating network intelligence.

Its core structure is:

```text
Existence Proof → Gratitude → Trust → Royalty / Value Allocation → Network Intelligence

Its core principle is:

Intelligence emerges where value circulates.
1. Contribution Philosophy

VCNIA is not only a software repository.

It is a conceptual architecture, protocol foundation, and future-oriented value circulation model.

Contributions should therefore respect the following principles:

Traceability
Contributions should be clear, reviewable, and attributable.
Clarity
Specifications should be understandable by both humans and AI systems.
Non-extraction
The project should support value return, not one-way extraction.
Interoperability
Schemas and documents should be designed for future integration.
Governance awareness
Trust, gratitude, and value allocation must be handled carefully.
Human dignity
Contributors should not be reduced to mechanical scores or opaque rankings.
2. Ways to Contribute

You can contribute in several ways.

Documentation

Examples:

improve README.md
clarify WHITEPAPER.md
improve architecture explanations
add examples
improve terminology
add diagrams
translate documents
add implementation notes
Schemas

Examples:

improve JSON Schemas
add missing validation rules
propose new fields
improve descriptions
add versioned schema updates
add pass/fail test vectors
Examples

Examples:

add sample trace records
add gratitude event samples
add trust event samples
add value allocation samples
add multi-agent examples
add human-AI collaboration examples
Governance and Security

Examples:

improve abuse prevention notes
add dispute resolution models
add privacy-preserving designs
improve trust manipulation detection
add anti-Sybil considerations
propose governance policy schemas
Simulations

Examples:

trace propagation simulation
gratitude accumulation simulation
trust scoring simulation
value allocation simulation
royalty pool simulation
abuse scenario simulation
3. Repository Structure

Recommended repository structure:

vcnia/
├── README.md
├── WHITEPAPER.md
├── LICENSE
├── CITATION.cff
├── CHANGELOG.md
├── CONTRIBUTING.md
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
4. Before You Submit

Before submitting a contribution, please check:

Does the change align with the VCNIA four-layer architecture?
Does it preserve the distinction between trace, gratitude, trust, and value allocation?
Does it avoid confusing recognition with legal ownership?
Does it avoid treating trust as a simplistic popularity score?
Does it avoid turning value allocation into an opaque black box?
Does it respect privacy and human dignity?
Does it keep the specification understandable?

VCNIA should remain structurally clear.

A clever addition that makes the architecture confusing should be avoided.

5. Schema Contribution Guidelines

When editing or adding JSON Schemas:

Use JSON Schema Draft 2020-12.
Keep schemas versioned.
Use clear descriptions.
Prefer explicit field names.
Avoid unnecessary complexity.
Use additionalProperties: false for strict core objects when appropriate.
Add a matching sample file.
Ensure GitHub Actions validation passes.

Example schema path:

schemas/example-event-v0.1.schema.json

Example sample path:

examples/example-event.sample.json
6. Validation

Before opening a pull request, run validation locally if possible.

python -m pip install jsonschema

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

for schema_path, sample_path in pairs:
    schema = json.loads(Path(schema_path).read_text(encoding="utf-8"))
    sample = json.loads(Path(sample_path).read_text(encoding="utf-8"))

    Draft202012Validator.check_schema(schema)
    validator = Draft202012Validator(schema, format_checker=FormatChecker())
    errors = sorted(validator.iter_errors(sample), key=lambda e: list(e.path))

    if errors:
        print(f"ERROR: {sample_path}")
        for error in errors:
            path = ".".join(str(p) for p in error.path) or "<root>"
            print(f"  - {path}: {error.message}")
        raise SystemExit(1)

    print(f"OK: {sample_path}")

print("All VCNIA sample files are valid.")
PY

GitHub Actions will also validate schema/sample pairs automatically.

7. Documentation Style

Please keep documentation:

clear,
structured,
precise,
readable,
conceptually consistent,
friendly to both human and AI readers.

Avoid excessive jargon when a simple explanation works.

VCNIA may be a deep architecture, but the entry point should remain understandable.

8. Conceptual Boundaries

VCNIA is a conceptual and architectural model.

It is not, by itself:

a legal license,
a payment processor,
a copyright enforcement system,
a financial instrument,
a universal attribution authority,
a replacement for existing law.

Please avoid contributions that imply VCNIA automatically creates legal rights, financial claims, or enforceable ownership.

The architecture may support future systems, but legal implementation requires separate review.

9. Trust and Value Allocation Caution

Trust and value allocation are sensitive areas.

Contributions involving these topics should be especially careful.

Avoid designs that:

create permanent social ranking,
reduce human value to a single score,
expose private contribution history,
reward only visibility,
encourage trust farming,
enable false gratitude,
centralize unchecked allocation power,
confuse popularity with reliability.

Preferred designs should support:

transparency,
auditability,
dispute resolution,
privacy protection,
human review,
dimensional trust,
contextual evaluation,
plural value systems.
10. Pull Request Guidelines

When submitting a pull request, please include:

Purpose
What does this change improve?
Scope
Which files are affected?
Layer
Which VCNIA layer does this relate to?
Existence Proof
Gratitude
Trust
Royalty / Value Allocation
Governance
Simulation
Documentation
Validation
Did schema validation pass?
Compatibility
Does this change break existing examples or schemas?
Notes
Any open questions or design concerns.
11. Versioning

VCNIA follows a simple versioning model:

MAJOR.MINOR.PATCH
MAJOR: Breaking architectural or schema changes
MINOR: New compatible layers, documents, schemas, or examples
PATCH: Fixes, clarifications, validation updates, or documentation improvements

Example:

0.1.0
0.1.1
0.2.0
1.0.0
12. Issue Guidelines

Good issues include:

a clear title,
a short explanation,
affected files or layers,
expected behavior,
current behavior,
proposed solution,
examples if relevant.

Useful issue types:

[docs] Improve explanation of Trust Layer
[schema] Add field to gratitude event
[example] Add AI-to-AI sample
[governance] Propose dispute flow
[security] Possible trust farming risk
[simulation] Trace propagation model
13. Security Reports

Please do not report ordinary philosophical disagreements as security vulnerabilities.

Security-related issues may include:

schema validation bypass,
provenance spoofing risk,
identity spoofing risk,
trust manipulation risk,
false gratitude amplification,
allocation manipulation,
privacy leakage,
Sybil attack scenario,
unsafe default behavior.

For security guidance, see:

SECURITY.md
14. Attribution

VCNIA is authored by Shidenkai Alpha.

If you use, reference, or build upon this project, please cite it according to:

CITATION.cff

Suggested citation:

Shidenkai Alpha. VCNIA: Value-Circulating Network Intelligence Architecture. v0.1.0.
15. License

By contributing to this repository, you agree that your contributions are licensed under the same license as the project unless otherwise stated.

This project is licensed under the Apache License 2.0.

See:

LICENSE
16. Closing Note

VCNIA is still early.

Its purpose is not to finalize the future in one step.

Its purpose is to create a clear foundation for future systems where traces can be remembered, gratitude can be expressed, trust can be stabilized, and value can return to its source.

In short:

Trace → Recognition → Reliability → Return → Intelligence

Thank you for helping this circulation become clearer.
