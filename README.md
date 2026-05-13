# Unified Agency Architecture (UAA)

Execution authority does not exist by default.

Unified Agency Architecture (UAA) is a formal authority-governance architecture for adaptive execution systems.

UAA externalizes execution authority from capability generation through:

- admissibility evaluation
- execution-boundary enforcement
- deterministic allow/block semantics
- monotone boundary constraints
- append-only auditability
- replay-resistant authorization validation

Under UAA, a computational action is not permitted to produce side effects unless admissibility validation succeeds at a required execution boundary.

---

## Governance Model

UAA defines governance semantics for systems in which:

- capability does not inherently imply authority
- execution permission must be externally validated
- authorization is verified immediately before effectuation
- invalid or replayed authorization produces zero execution effect
- boundary violations fail closed
- denial outcomes are first-class audit events

The architecture is model-agnostic and execution-surface agnostic.

UAA applies to:

- autonomous systems
- financial systems
- distributed systems
- orchestration environments
- AI agents
- infrastructure runtimes
- governed execution systems

---

## Reference Surface

This repository provides a constrained executable reference surface demonstrating:

- per-attempt authorization validation
- execution-boundary enforcement
- replay rejection
- deterministic allow/block semantics
- boundary mismatch rejection
- append-only auditability semantics

The reference implementation is intentionally minimal and is designed to demonstrate governance invariants rather than production deployment infrastructure.

---

## Repository Structure

audit/      -> auditability semantics
boundary/   -> execution-boundary definitions
core/       -> foundational invariants
formal/     -> formal execution semantics and conformance mappings
examples/   -> constrained executable reference demonstrations

---

## Demo Execution

Run demo:

python .\examples\demo.py

Run validation suite:

python .\examples\test_demo.py

---

## Expected Validation Output

[PASS] no artifact - no authorization artifact
[PASS] invalid artifact - invalid authorization artifact
[PASS] valid execution - action permitted
[PASS] replay - replay detected
[PASS] boundary mismatch - boundary mismatch

ALL TESTS PASSED

If any validation output differs, enforcement behavior is not functioning as defined.

---

## Relationship to EIP

Unified Agency Architecture (UAA) defines governance authority architecture.

Execution Integrity Protocol (EIP) extends UAA through:

- execution-time continuity verification
- runtime-bound authorization validation
- canonical runtime state verification
- deterministic execution integrity enforcement

---

## Contact

governance@unifiedagencyarchitecture.org

Official reference:

https://unifiedagencyarchitecture.org/
