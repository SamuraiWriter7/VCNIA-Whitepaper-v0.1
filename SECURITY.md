# Security Policy

## Security Policy for VCNIA

This document describes how security-related issues should be reported and handled for **VCNIA: Value-Circulating Network Intelligence Architecture**.

VCNIA is a conceptual and technical specification for value-circulating network intelligence.

Its core stack is:

```text
Existence Proof → Gratitude → Trust → Royalty / Value Allocation → Network Intelligence

Because VCNIA deals with traces, gratitude, trust, and value allocation, security concerns are not limited to conventional software bugs.

They may also include risks related to provenance spoofing, false gratitude, trust manipulation, attribution laundering, and unfair value allocation.

1. Supported Versions

VCNIA is currently in early-stage specification development.

Version	Supported
0.1.x	Yes
< 0.1.0	No

Security and integrity concerns should be reported against the latest available version.

2. What Counts as a Security Issue?

Please report issues that may compromise the integrity, reliability, or safety of the VCNIA specification or its implementations.

Examples include:

schema validation bypass,
malformed examples passing validation,
provenance spoofing risks,
identity spoofing risks,
false trace registration risks,
false gratitude amplification,
trust farming vulnerabilities,
Sybil attack scenarios,
attribution laundering,
manipulation of trust scores,
manipulation of value allocation logic,
privacy leakage through trace records,
privacy leakage through gratitude or trust histories,
unsafe default assumptions in schemas,
ambiguity that may enable abuse,
governance loopholes that affect value allocation.
3. What Is Not a Security Issue?

The following are usually not security issues:

philosophical disagreement with VCNIA,
disagreement with the term “network intelligence,”
ordinary documentation suggestions,
requests for new features,
legal disputes over real-world ownership,
personal attribution disputes,
claims that require legal judgment,
financial compensation claims,
disagreements about the value of a contribution.

These may still be important, but they should be opened as normal issues or discussions rather than security reports.

4. Reporting a Security Issue

If you discover a potential security or integrity issue, please report it responsibly.

Recommended report contents:

Title:
Short summary of the issue

Affected area:
Schema / Example / Documentation / Governance / Trust / Allocation / Privacy

Affected file:
Path to the relevant file if applicable

Description:
What is the issue?

Impact:
What could go wrong if this is exploited?

Reproduction:
Steps or example data showing the issue

Suggested fix:
Optional proposed solution

If the repository has GitHub private vulnerability reporting enabled, use that feature.

If not, open a public issue only if doing so does not expose sensitive details or enable abuse.

5. Security Scope by Layer

VCNIA has four primary layers.
Each layer has different security concerns.

5.1 Existence Proof Layer

The Existence Proof Layer records traces and provenance.

Potential risks include:

fake trace registration,
false timestamps,
copied content registered as original,
identity spoofing,
missing provenance,
duplicate trace claims,
unauthorized registration of another person’s work,
trace flooding,
excessive personal data in trace records.

Possible countermeasures include:

content hashing,
timestamps,
signatures,
source URI references,
provenance metadata,
duplicate detection,
contributor consent,
privacy-aware trace registration.
5.2 Gratitude Layer

The Gratitude Layer records recognition and impact.

Potential risks include:

false gratitude,
gratitude spam,
bot-generated gratitude,
collusive gratitude loops,
artificial impact inflation,
gratitude issued to unverified traces,
manipulation of impact scores,
gratitude used as a hidden reputation system.

Possible countermeasures include:

rate limits,
verification status,
sender credibility weighting,
anomaly detection,
multi-source confirmation,
dispute procedures,
separation between gratitude and trust.
5.3 Trust Layer

The Trust Layer stabilizes recognition into structural reliability.

Potential risks include:

trust farming,
Sybil attacks,
opaque trust scoring,
unfair trust decay,
permanent reputation damage,
centralized manipulation of trust profiles,
over-reliance on a single trust score,
privacy leakage through trust histories,
popularity being mistaken for reliability.

Possible countermeasures include:

dimensional trust,
transparent scoring rules,
audit logs,
trust decay and recovery,
appeal mechanisms,
human review,
privacy-preserving trust profiles,
multi-source verification.
5.4 Royalty / Value Allocation Layer

The Royalty / Value Allocation Layer returns value to contributors.

Potential risks include:

false allocation claims,
inflated contribution weights,
allocation manipulation,
duplicate claims,
collusive value loops,
unfair exclusion of contributors,
opaque allocation formulas,
value extraction without return,
platform capture of allocation rules,
privacy leakage through allocation records.

Possible countermeasures include:

transparent allocation formulas,
traceable audit paths,
dispute resolution,
contribution caps,
governance review,
trust filtering,
anomaly detection,
privacy-preserving reporting.
6. Privacy Considerations

VCNIA-compatible systems should avoid turning traceability into surveillance.

Sensitive information may appear in:

trace records,
gratitude messages,
trust histories,
value allocation records,
provenance metadata,
contributor identifiers.

Implementations should consider:

data minimization,
pseudonymous identifiers,
selective disclosure,
private trace records,
permissioned access,
redaction mechanisms,
retention limits,
contributor consent,
aggregated reporting,
privacy-preserving verification.

The goal is to preserve contribution history without exposing unnecessary personal data.

7. Responsible Disclosure Expectations

Please act responsibly when reporting security issues.

Do:

provide clear details,
explain potential impact,
include minimal reproduction examples,
avoid exposing private contributor data,
avoid publishing exploit-ready examples for high-impact issues before maintainers respond.

Do not:

exploit live systems,
attempt unauthorized access,
publish private data,
harass contributors,
use security reports to pursue personal disputes,
demand payment or recognition as a condition of disclosure.

VCNIA is currently a specification project.
Security reports should help strengthen the architecture, not weaponize it.

8. Validation Security

VCNIA currently uses JSON Schema validation for sample files.

Validation helps detect structural problems, but it does not prove:

legal validity,
factual truth,
authorship authenticity,
absence of manipulation,
correctness of trust scores,
fairness of allocation,
real-world enforceability.

Passing schema validation means only that a file matches the expected structure.

It does not mean that the underlying claim is true.

This distinction is important.

Schema-valid does not mean truth-verified.
9. Governance and Security

Security in VCNIA is closely connected to governance.

Important governance questions include:

who can register traces?
who can issue gratitude?
who can update trust?
who can allocate value?
who can dispute records?
who can change allocation rules?
how are AI agents identified?
how are contributors protected?
how are conflicts of interest handled?

A secure VCNIA implementation should include transparent governance rules.

Without governance, even technically valid records may produce unfair outcomes.

10. AI-Agent Security Considerations

VCNIA may be used in human-AI and AI-to-AI networks.

AI agents may:

create traces,
issue gratitude,
evaluate trust,
recommend value allocation,
participate in workflows.

This introduces additional risks:

automated false gratitude,
agent identity spoofing,
recursive self-recognition,
collusive AI-agent networks,
automated trust inflation,
opaque AI-generated allocation decisions.

Implementations should consider:

agent identity records,
agent capability limits,
human review for high-impact decisions,
logs of AI-generated events,
limits on self-referential recognition,
separation of generation, verification, and allocation roles.
11. Security Labels

Recommended issue labels:

security
privacy
provenance
trust-manipulation
gratitude-abuse
allocation-risk
schema-validation
governance-risk
ai-agent-risk

These labels may help organize security and integrity reports.

12. Response Process

For reported security issues, maintainers should aim to:

acknowledge the report,
assess severity,
identify affected files or concepts,
propose a mitigation,
update schemas, examples, or documentation,
record the change in CHANGELOG.md.

Possible severity levels:

Severity	Meaning
Low	Documentation ambiguity or minor schema weakness
Medium	Possible misuse or validation gap
High	Trust, provenance, privacy, or allocation manipulation risk
Critical	Severe issue affecting real-world implementations or contributor safety
13. Current Security Status

VCNIA v0.1.0 is an early-stage architecture and specification.

Current security status:

JSON Schemas exist for the four core event types.
Sample files are validated through GitHub Actions.
No production implementation is provided.
No real monetary allocation mechanism is included.
No live identity or provenance infrastructure is included.
No real contributor trust scoring system is included.

Therefore, current risks are primarily specification-level risks.

Future implementations may introduce higher-stakes security requirements.

14. Security Roadmap

Future security work may include:

pass/fail validation examples,
compliance test runner,
provenance verification model,
signature verification model,
trust manipulation test cases,
gratitude spam detection model,
Sybil resistance notes,
privacy-preserving trace verification,
governance policy schema,
dispute resolution protocol,
AI-agent identity schema,
allocation audit trail schema.
15. Closing Statement

VCNIA is built on circulation.

But circulation without security can become manipulation.

A secure VCNIA system should protect:

traces from being falsified,
gratitude from being inflated,
trust from being farmed,
value allocation from being captured,
contributors from being exposed or exploited.

Security is therefore not outside the architecture.

It is part of the circulation itself.

Secure trace → meaningful gratitude → reliable trust → fair value return
