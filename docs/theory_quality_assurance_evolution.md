# Theory Quality Assurance Evolution

## Purpose

This note records a future direction for improving the quality assurance process used when developing theories, mathematical formulations, PoCs, and prototypes with generative AI.

The intent is **not** to introduce a complete mandatory process immediately.

Instead, the process should be improved incrementally as actual review experience accumulates.

---

## Background

Generative AI can contribute to many different forms of project output, including:

- theory and conceptual models
- definitions and structured arguments
- mathematical formulations
- PoCs
- prototype implementations
- documentation and papers

However, the quality of these outputs cannot be guaranteed merely because multiple AI systems agree with them.

A useful long-term direction is therefore to combine:

- multiple AI reviews
- human judgment
- mathematical verification
- executable tests
- PoC results
- prototype behavior
- external review

into a staged quality assurance process.

---

## Core Principle

The target is not:

> AI says the result is correct.

The target is:

> The result has passed several independent forms of verification appropriate to its maturity level.

Multiple AI reviews should therefore be treated as **independent criticism sources**, not as a majority vote.

Agreement between AI systems increases confidence only weakly if they rely on similar assumptions, knowledge, or reasoning patterns.

The more important question is whether different reviewers can expose:

- contradictions
- missing assumptions
- ambiguous definitions
- counterexamples
- conflicts with known work
- unverifiable claims
- implementation failures

---

## Long-Term Verification Flow

A possible future structure is:

```text
Idea / Observation
      ↓
Theory / Definitions
      ↓
Theory Review
      ↓
Mathematical Formulation
      ↓
Mathematical Review
      ↓
PoC
      ↓
Empirical / Behavioral Review
      ↓
Prototype
      ↓
Engineering Review
      ↓
External Review / Publication / Real-world Evaluation
```

This should initially be understood as a **direction**, not as a rigid lifecycle.

Projects may move backward, skip stages temporarily, or remain at a conceptual stage for long periods.

---

## Candidate Gates

### Gate 1 — Theory

Possible future checks:

- core terms are defined or intentionally left open
- definitions do not obviously contradict each other
- assumptions are distinguishable from conclusions
- claims are scoped
- unresolved questions are recorded
- major counterexamples have been explored
- multiple AI reviewers have examined different aspects
- the human operator confirms that the result still represents the intended idea

The human check is especially important because an internally coherent rewrite can still distort the original concept.

---

### Gate 2 — Mathematics

Possible future checks:

- mathematical objects correspond to theoretical concepts
- symbols and domains are defined
- transformations are valid
- equations do not introduce claims absent from the theory
- assumptions required by the mathematics are explicit
- counterexamples and edge cases are tested
- calculations or proofs are independently checked where possible
- multiple AI systems review different failure modes
- human review confirms semantic correspondence between theory and mathematics

The goal is not merely to produce equations, but to prevent **formal-looking notation from creating false confidence**.

---

### Gate 3 — PoC

Possible future checks:

- the PoC tests a clearly stated claim or mechanism
- expected behavior is defined before evaluation
- failure conditions are visible
- results can be reproduced
- observed results are separated from interpretation
- implementation artifacts are reviewable
- automated tests are added where useful
- multiple AI systems review logic, test design, and edge cases
- human review confirms that the PoC actually tests the intended theory

A successful PoC should increase confidence only in the specific claims it actually tests.

---

### Gate 4 — Prototype

Possible future checks:

- unit tests
- integration tests
- static analysis
- security review where relevant
- reproducible execution
- error and boundary behavior
- documentation of unsupported cases
- comparison between implementation behavior and theoretical expectations
- multiple AI reviews with differentiated roles
- human review of release readiness

At this stage, executable verification becomes increasingly important and should carry more weight than AI agreement alone.

---

## Role Separation for Multiple AI Reviews

Avoid asking every AI only:

> Is this correct?

Instead, assign different review roles.

Examples:

### Reviewer A — Internal Consistency

Focus on:

- definition conflicts
- circular reasoning
- hidden assumptions
- terminology drift

### Reviewer B — Adversarial / Counterexample

Focus on:

- counterexamples
- edge cases
- situations where the claim fails
- overly broad conclusions

### Reviewer C — Existing Knowledge / Alternative Explanation

Focus on:

- overlap with existing concepts
- possible prior art
- alternative interpretations
- whether novelty is overstated

### Reviewer D — Formal / Implementation Correspondence

Focus on:

- whether equations or code still represent the theory
- whether implementation introduces additional assumptions
- whether test results support the stated claim

These roles are examples and should be adapted rather than fixed permanently.

---

## Human Role

Human review is not simply another vote.

The human operator should retain responsibility for:

- deciding what question is actually being investigated
- deciding which definitions are intentional
- distinguishing correction from unwanted conceptual replacement
- deciding review priorities
- judging whether a criticism requires modification
- determining when further review has diminishing value
- deciding when an artifact is mature enough for the next stage

This is particularly important in theory development because repeated AI review can otherwise create endless correction loops or gradually replace the original idea with a more conventional one.

---

## Avoiding Endless Review Loops

A quality process must also define when to stop revising.

Future review rules should therefore distinguish at least:

- critical contradiction
- material but local issue
- interpretation difference
- needs verification
- future work
- stylistic preference

Not every valid observation must block progression.

A review cycle should be allowed to close when remaining items no longer threaten the current artifact's stated scope.

This is important to prevent quality assurance from becoming an endless optimization process.

---

## Incremental Adoption Strategy

Do not introduce all gates at once.

A practical evolution path is:

### Stage 0 — Record only

- store review comments
- classify major issues
- record why changes were accepted or rejected

### Stage 1 — Multiple AI Review

- use more than one AI where useful
- assign differentiated review roles
- avoid majority voting

### Stage 2 — Lightweight Gate Criteria

- define a small number of blocking conditions
- distinguish blocking issues from future work
- allow explicit Gate PASS / PASS WITH NOTES / HOLD

### Stage 3 — Formal Verification Links

- connect theory claims to equations
- connect equations to PoC tests
- connect PoC expectations to observed results

### Stage 4 — Engineering QA Integration

- automated tests
- CI
- static analysis
- reproducibility checks
- release criteria

### Stage 5 — External Validation

- peer review
- public criticism
- independent reproduction
- real-world usage feedback

These stages describe increasing maturity, not mandatory project phases.

---

## Improvement Policy

This document should itself evolve through use.

When actual operation reveals problems, update the process rather than forcing work to conform to an unsuitable rule.

Useful observations to record include:

- reviews that produced meaningful corrections
- reviews that repeatedly generated low-value comments
- cases where multiple AI systems made the same mistake
- cases where human judgment overruled AI consensus
- cases where formalization exposed a theoretical flaw
- cases where PoC behavior contradicted expectations
- cases where a gate blocked progress unnecessarily
- cases where a missing gate allowed a defect to propagate

The quality assurance process should therefore be treated as an evolving engineering artifact.

---

## Initial Operating Rule

For now:

1. Continue using multiple AI systems for important theory reviews where practical.
2. Prefer differentiated review roles over simple agreement checks.
3. Keep the human operator as the final decision-maker.
4. Record unresolved items instead of forcing every issue to be solved immediately.
5. Introduce mathematical, PoC, and prototype gates gradually as those artifacts mature.
6. Treat future Gate definitions as quality aids, not as rigid bureaucracy.

---

## Future Work

Potential additions:

- standardized review role prompts
- review issue classification schema
- Gate PASS / PASS WITH NOTES / HOLD criteria
- traceability from theory claim → equation → PoC → prototype test
- confidence / evidence notation
- review convergence criteria
- external-review integration
- automation in gyro-dev-tools / GitHub Actions

These should be added only when operational experience justifies them.
