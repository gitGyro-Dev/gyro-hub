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
- non-AI mathematical / formal verification
- executable tests
- PoC results
- prototype behavior
- external review

into a staged quality assurance process.

---

## Core Principle

The target is not:

> AI says the result is correct.

Nor is the target:

> This process proves that the theory is ultimately true.

The practical target is closer to:

> At the current stage, no blocking contradiction or decisive counterevidence is known within the stated scope, and the artifact has enough supporting verification to be worth using, testing, or advancing further.

The result should therefore be treated as **provisionally usable**, not as finally proven.

Multiple AI reviews should be treated as **diverse criticism sources**, not as a majority vote and not as fully independent validators.

Even when different vendors or model families are used, AI systems may share:

- similar training-data biases
- common conventional assumptions
- similar reasoning shortcuts
- common omissions caused by the prompt or artifact itself

Therefore, agreement among multiple AI systems is only weak evidence unless the reviews are intentionally diversified and supported by non-AI checks where possible.

The more important question is whether different review methods can expose:

- contradictions
- missing assumptions
- ambiguous definitions
- counterexamples
- conflicts with known work
- unverifiable claims
- implementation failures

---

## What "Correct" Means in This Process

Theory quality should not be reduced to a single binary notion of correctness.

At least four different senses should be distinguished.

### 1. Logical / Internal Correctness

Questions include:

- Are the definitions mutually consistent?
- Do conclusions follow from stated assumptions?
- Are hidden assumptions or circular arguments present?
- Does terminology remain stable?

This is comparatively close to a closed verification problem.

### 2. Mathematical / Formal Correctness

Questions include:

- Are equations and transformations valid?
- Are symbols, domains, and assumptions defined?
- Can a formal claim be checked mechanically?
- Does the mathematics still represent the intended theory?

Formal verification can strengthen confidence here when the claim is actually formalizable.

### 3. Empirical / External Validity

Questions include:

- Does the theory correspond to observed phenomena?
- Does it survive relevant counterexamples?
- Does a PoC or experiment behave as predicted?
- Does external evidence support or contradict it?

This usually cannot be settled by AI review alone.

A successful review or experiment should be interpreted as evidence that the theory has **not yet been decisively refuted within the tested scope**, not as proof of universal truth.

### 4. Practical / Operational Usefulness

Questions include:

- Does the theory help explain or organize the target problem?
- Does it lead to useful predictions, designs, or implementations?
- Does applying it repeatedly produce meaningful results?
- Is it more useful than available alternatives for the intended scope?

This is not identical to truth, but it matters strongly for whether further development is justified.

These dimensions should not be collapsed into one status.

---

## Provisional Usability Principle

For practical operation, the project does not need to claim ultimate correctness.

A theory, formulation, or design may be considered **worth using or advancing** when:

- no unresolved critical contradiction is known within the current scope
- no decisive counterexample or contradictory evidence is known within the current scope
- important assumptions and limitations are explicit
- relevant criticism has been attempted from multiple directions
- available mathematical, empirical, or implementation evidence is consistent with the current claims
- unresolved issues are recorded rather than hidden
- the human operator judges that further use, testing, or development is justified

This status is provisional and may change when new evidence, criticism, or implementation behavior appears.

The process therefore aims to maintain an evolving evidence state rather than to issue a permanent declaration of truth.

---

## Two Verification Axes

Theory-related review should explicitly separate two different questions.

### Internal Consistency

Does the artifact cohere on its own terms?

Examples:

- definitions do not conflict
- claims follow from stated assumptions
- terminology does not drift
- circular reasoning is avoided
- equations correspond to the stated theory

AI review can contribute strongly here, especially when roles are differentiated.

### External Validity

Does the artifact adequately correspond to existing knowledge, observation, experiment, implementation behavior, or the real-world phenomenon it claims to explain?

Examples:

- compatibility or conflict with prior work
- empirical evidence
- reproducible PoC behavior
- prototype behavior under realistic conditions
- external peer criticism
- independent reproduction

AI alone cannot establish external validity. External validity requires evidence or verification that is not merely another generative judgment.

The distinction should remain visible throughout the lifecycle so that an internally coherent theory is not mistaken for an externally validated one.

---

## Long-Term Verification Flow

A possible future structure is:

```text
Idea / Observation
      ↓
Theory / Definitions
      ↓
Theory Review
  ├─ Internal Consistency Review
  └─ External Validity Questions / Evidence Status
      ↓
Mathematical Formulation
      ↓
Mathematical Review
  ├─ AI Review
  └─ Non-AI Formal / Symbolic Verification where applicable
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
      ↓
Updated evidence / limitations / new questions
      ↺
```

This should initially be understood as a **direction**, not as a rigid lifecycle.

Projects may move backward, skip stages temporarily, remain at a conceptual stage for long periods, or re-enter an earlier stage after new evidence appears.

---

## Candidate Gates

The purpose of a Gate is **not to certify truth**.

A Gate answers a narrower operational question:

> Is the artifact sufficiently coherent, checked, and evidenced for the next intended use at its current maturity level?

### Gate 1 — Theory

Possible future checks:

#### Internal consistency

- core terms are defined or intentionally left open
- definitions do not obviously contradict each other
- assumptions are distinguishable from conclusions
- claims are scoped
- unresolved questions are recorded
- major counterexamples have been explored
- multiple AI reviewers have examined different failure modes
- the human operator confirms that the result still represents the intended idea

#### External validity status

- relevant existing work has been searched where appropriate
- similarities and conflicts with known concepts are recorded
- claims that still lack evidence are explicitly marked as hypotheses, open questions, or future verification targets
- no AI consensus is treated as empirical confirmation

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

Where applicable, use **non-AI external checkers** in addition to AI review.

Possible examples include:

- symbolic algebra / simplification tools such as SymPy
- numerical cross-checks
- property-based testing of mathematical invariants
- theorem provers or proof assistants such as Lean
- other domain-specific formal verification tools

These tools should not be introduced merely for appearance. They are useful only when the mathematical claim can actually be represented and checked by them.

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

This is one of the first stages where external validity can receive direct evidence from behavior rather than only argument.

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

### Reviewer C — Existing Knowledge / Supporting Evidence

Focus on:

- related existing concepts
- supporting prior work
- terminology already used in the field
- evidence that may strengthen the claim

### Reviewer D — Existing Knowledge / Competing Explanation

Focus on:

- conflicting prior work
- alternative explanations
- possible prior art
- whether novelty is overstated

### Reviewer E — Formal / Implementation Correspondence

Focus on:

- whether equations or code still represent the theory
- whether implementation introduces additional assumptions
- whether test results support the stated claim

Using explicitly opposed or asymmetric roles is preferred over simply asking several models the same neutral question.

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
- deciding whether the current evidence is sufficient to justify continued use or development

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

### Candidate stopping rule

A review cycle may close when all of the following are true:

1. No unresolved **critical contradiction** remains within the current scope.
2. No known decisive counterexample or contradictory evidence blocks the current intended use.
3. Material local issues are either fixed or explicitly documented with a reason for deferral.
4. At least one adversarial / counterexample-oriented review has been performed for important claims.
5. Remaining items are classified as interpretation differences, needs verification, future work, or stylistic preferences.
6. The human operator confirms that additional review is unlikely to materially change the artifact at the current maturity level.

Do **not** use arbitrary numeric rules such as "N failed counterexample searches means the theory is correct." Repeated failure to find a counterexample may increase practical confidence, but it is not proof unless the search space and verification method justify that conclusion.

Gate outcomes can later be standardized as:

- **PASS** — no blocking issue remains for the current intended use and scope
- **PASS WITH NOTES** — progression or use is allowed, but unresolved non-blocking items are recorded
- **HOLD** — at least one blocking contradiction, counterexample, or evidence gap remains

These labels indicate operational readiness, not permanent truth status.

This is important to prevent quality assurance from becoming an endless optimization process.

---

## Evidence-oriented Status Language

Where possible, avoid labels such as:

- proven theory
- completely correct
- validated once and for all

Prefer statements such as:

- no critical contradiction is currently known within the stated scope
- no decisive counterexample has been identified in the checks performed so far
- current PoC results are consistent with the stated mechanism
- the current formulation has passed the listed mathematical checks
- the prototype behaves consistently with the current theory under the tested conditions
- unresolved limitations and future verification items remain

This language records **what has actually been checked**, making later reassessment easier.

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
- assign differentiated and, where useful, adversarial review roles
- avoid majority voting
- record cases where multiple AI systems converge on the same error or assumption

### Stage 2 — Lightweight Gate Criteria

- define a small number of blocking conditions
- distinguish blocking issues from future work
- separate internal consistency status from external validity status
- allow explicit Gate PASS / PASS WITH NOTES / HOLD
- treat Gate status as provisional usability, not truth certification

### Stage 3 — Formal Verification Links

- connect theory claims to equations
- connect equations to PoC tests
- connect PoC expectations to observed results
- introduce symbolic, numerical, or proof-assistant checks where they add real verification value

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
- update the theory, evidence status, or scope when new findings appear

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
- cases where non-AI formal tools confirmed or rejected a mathematical claim
- cases where PoC behavior contradicted expectations
- cases where a gate blocked progress unnecessarily
- cases where a missing gate allowed a defect to propagate
- cases where an internally consistent result later failed external validation
- cases where a previously usable theory required revision after new evidence appeared

The quality assurance process should therefore be treated as an evolving engineering artifact.

---

## Initial Operating Rule

For now:

1. Continue using multiple AI systems for important theory reviews where practical.
2. Prefer differentiated and adversarial review roles over simple agreement checks.
3. Treat multiple AI reviewers as correlated sources, not as independent proof.
4. Keep the human operator as the final decision-maker.
5. Separate **internal consistency** from **external validity / evidence status** in review notes where useful.
6. Record unresolved items instead of forcing every issue to be solved immediately.
7. Introduce mathematical, PoC, and prototype gates gradually as those artifacts mature.
8. Introduce non-AI formal or symbolic checks only where they genuinely fit the claim being tested.
9. Close a review cycle once no blocking contradiction or decisive counterevidence remains and the remaining items are explicitly classified.
10. Treat Gate outcomes as provisional readiness for the next use, not as certification of ultimate truth.
11. Update theory, scope, and evidence status when new criticism, experiments, implementations, or external reviews produce materially new information.
12. Treat future Gate definitions as quality aids, not as rigid bureaucracy.

---

## Future Work

Potential additions:

- standardized review role prompts
- review issue classification schema
- Gate PASS / PASS WITH NOTES / HOLD criteria
- separate internal-consistency and external-validity status fields
- traceability from theory claim → equation → PoC → prototype test
- confidence / evidence notation
- review convergence / stopping criteria
- formal verification candidates by artifact type
- external-review integration
- evidence-history / theory-revision log
- automation in gyro-dev-tools / GitHub Actions

These should be added only when operational experience justifies them.
