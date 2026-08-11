# Gyro Research Cycle

Gyro Project is not only a set of papers or repositories. It is a research platform designed to continuously grow ideas from early hypotheses into documented, implemented, published, and refined artifacts.

## Core Cycle

```text
Brainstorm
↓
Hypothesis / Idea
↓
X / Communication
↓
GitHub Documentation
↓
PoC / Prototype
↓
Paper / Release
↓
Feedback
↓
Refinement
↓
Brainstorm
```

This cycle is the operating model of the Gyro ecosystem.

## Roles

### Brainstorm

Brainstorming is the place for early theoretical exploration.

- Concepts
- Questions
- Hypotheses
- Future directions
- Unfinished ideas

Brainstorming does not require immediate completion.

### X / Communication

X is used to share intermediate research signals.

- Ideas
- Questions
- PoC notes
- Runtime concepts
- Boundary concepts
- Research process updates

X is not limited to finished work.

### GitHub

GitHub is the place where the latest version of the research is grown.

- README
- Docs
- PoC
- Examples
- Roadmap
- Issues
- Discussions
- Releases

GitHub is treated as the working source of truth for active research.

### PoC / Prototype

PoC work translates a concept into executable or inspectable behavior.

- Runtime experiments
- API examples
- Stability demonstrations
- Authentication flows
- Dashboard generation

### Paper / Release

Papers and releases are mature outputs.

- Jxiv
- Zenodo
- DOI
- GitHub Releases

They represent stabilized results rather than every intermediate change.

### Feedback

Feedback returns external and internal signals into the research cycle.

- GitHub Issues
- GitHub Discussions
- X replies
- PoC results
- Review comments
- User observations

### Refinement

Refinement transforms feedback into the next iteration of the research.

- Clarification
- Re-slicing
- Documentation update
- PoC update
- New artifact
- New paper candidate

## Extended Cycle with Operations

```text
Brainstorm
↓
X / Communication
↓
GitHub
↓
PoC / Prototype
↓
Paper / Release
↓
Operations
↓
Feedback
↓
Refinement
↓
Brainstorm
```

Operations include repository updates, release management, DOI tracking, dashboard generation, Google Drive archiving, NotebookLM synchronization, and weekly reporting.

## Multi-AI Critical Review Gate

Adopted 2026-08-10, after external critical review of the Gyro Logic Jxiv publication (`10.51094/jxiv.5641`) exposed the value of an explicit, repeatable review step between `GitHub Documentation` and `Paper / Release`.

```text
GitHub Documentation (ideas/<topic>.md)
↓
Independent critical review
  ├─ Claude — reads the repository directly in-session; may commit revisions
  └─ Gemini — re-imports the repository independently for a second, uncorrelated pass
↓
Review record (accept / partial / reject / verify / defer per criticism)
↓
Refinement with ChatGPT
↓
Paper / Release
```

This gate exists to reduce single-model bias and self-confirmation in theory development.

- Agreement between reviewers is not treated as proof of validity.
- Disagreement between reviewers is preserved, not averaged away.
- Factual criticisms (missing citations, prior-work overlap, dates) are verified independently before being accepted.

Reference implementation: `gyrologic/reviews/review_workflow.md`, `gyrologic/reviews/critical_review_prompt.md`, `gyrologic/reviews/review_record_template.md`.

For major public manuscripts, the same principle extends to a structured **Pre-publication Multi-AI Critical Review Gate** (internal consistency, adversarial/skeptical, mathematical, literature, and blind-concept review roles) run before submission — see `gyrologic/project_cycle/2026-08-10_external_critical_review_followup.md`.

### Human checkpoint

Claude is authorized to write a critical review of an `ideas/<topic>.md` note and commit it directly to `reviews/` without asking first — critique and commit are both in scope, not just extraction/summary.

The human checkpoint required by `gyrologic/reviews/README.md` ("a criticism should be checked against the actual source document before being accepted") is satisfied by the project owner reading and confirming the review **in chat**, and this confirmation may happen after the commit already exists in git history — it is not a precondition for the review artifact being created. Confirmed 2026-08-11.

## Principle

The goal of Gyro Hub is to make this cycle visible, maintainable, and eventually automatable.
