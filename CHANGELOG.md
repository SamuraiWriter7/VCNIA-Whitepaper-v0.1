# Changelog

All notable changes to this project will be documented in this file.

This project follows a simple versioning model:

```text
MAJOR.MINOR.PATCH

MAJOR: Breaking architectural or schema changes
MINOR: New compatible layers, documents, schemas, or examples
PATCH: Fixes, clarifications, validation updates, or documentation improvements
[0.1.0] - 2026-04-27
Added
Initial release of VCNIA: Value-Circulating Network Intelligence Architecture
Added WHITEPAPER.md
Added README.md
Added LICENSE using Apache License 2.0
Added CITATION.cff
Added one-page overview:
docs/one-page-overview.md
Added architecture document:
docs/architecture.md
Added relationship documents for the four-layer Value Circulation OS Stack:
docs/relationship-to-existence-proof-os.md
docs/relationship-to-gratitude-os.md
docs/relationship-to-trust-os.md
docs/relationship-to-royalty-os.md
Added Schemas
Added JSON Schema for Trace Record:
schemas/trace-record-v0.1.schema.json
Added JSON Schema for Gratitude Event:
schemas/gratitude-event-v0.1.schema.json
Added JSON Schema for Trust Event:
schemas/trust-event-v0.1.schema.json
Added JSON Schema for Value Allocation Event:
schemas/value-allocation-v0.1.schema.json
Added Examples
Added sample Trace Record:
examples/trace-record.sample.json
Added sample Gratitude Event:
examples/gratitude-event.sample.json
Added sample Trust Event:
examples/trust-event.sample.json
Added sample Value Allocation Event:
examples/value-allocation.sample.json
Added Validation
Added GitHub Actions workflow:
.github/workflows/validate-specs.yml
Added automated validation for all v0.1 JSON Schemas and sample files
Confirmed that all initial schema samples pass validation
Defined
Defined the core VCNIA stack:
Existence Proof → Gratitude → Trust → Royalty / Value Allocation → Network Intelligence
Defined VCNIA’s core principle:
Intelligence emerges where value circulates.
Defined the four-layer architecture:
Existence Proof Layer
Gratitude Layer
Trust Layer
Royalty / Value Allocation Layer
Notes

This release establishes the initial conceptual, architectural, and validation-ready foundation of VCNIA.

VCNIA v0.1.0 should be understood as an early-stage specification foundation, not a production implementation.

[Unreleased]
Planned
Add CONTRIBUTING.md
Add SECURITY.md
Add NOTICE
Add docs/glossary.md
Add docs/legal-status.md
Add docs/governance-principles.md
Add schema usage documentation
Add pass/fail validation examples
Add compliance test runner
Add trust profile schema
Add governance policy schema
Add royalty pool simulation
Add multi-agent value circulation simulation
Add privacy-preserving trace verification design
