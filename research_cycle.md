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

Adopted 2026-08-10, after external critical review of the Gyro Logic Jxiv publication (`10.51094/jxiv.5641`) exposed the value of an explicit, repeatable review step between `GitHub Documentation` and `Paper / Release`. Refined 2026-08-11 to add a strict role boundary between critique and revision.

```text
GitHub Documentation (ideas/<topic>.md)
↓
Independent critical review (critique only, no edits to the reviewed note)
  ├─ Claude — reads the repository directly in-session; writes and commits a critique file to reviews/
  └─ Gemini — re-imports the repository independently for a second, uncorrelated pass
↓
Review record (accept / partial / reject / verify / defer per criticism)
↓
ChatGPT reads the critique, drafts a revision, and commits the revised ideas/<topic>.md
↓
Claude re-reads the revised note and writes a follow-up critique if anything remains open
↓
repeat until the revision is substantial enough to warrant a version bump (e.g. v0 → v1 → v2)
↓
Paper / Release
```

This gate exists to reduce single-model bias and self-confirmation in theory development.

- Agreement between reviewers is not treated as proof of validity.
- Disagreement between reviewers is preserved, not averaged away.
- Factual criticisms (missing citations, prior-work overlap, dates) are verified independently before being accepted.

### Role boundary: critique versus revision

**Claude (and Gemini) may critique but must never edit the reviewed `ideas/<topic>.md` note, or any paper/submission material, on the project owner's behalf.** Editing and committing the revision itself is exclusively ChatGPT's role. This keeps Claude's critical distance from the text intact for the next review pass, and produces a genuine mutual check: ChatGPT proposes the fix, Claude (and Gemini) re-examine it independently, and the project owner reviews both sides.

Reference implementation: `gyrologic/reviews/review_workflow.md`, `gyrologic/reviews/critical_review_prompt.md`, `gyrologic/reviews/review_record_template.md`.

For major public manuscripts, the same principle extends to a structured **Pre-publication Multi-AI Critical Review Gate** (internal consistency, adversarial/skeptical, mathematical, literature, and blind-concept review roles) run before submission — see `gyrologic/project_cycle/2026-08-10_external_critical_review_followup.md`.

### Human checkpoint

Claude is authorized to write a critical review of an `ideas/<topic>.md` note and commit it directly to `reviews/` without asking first — critique and commit of a *review file* are both in scope. Committing a change to the *reviewed note itself* is out of scope for Claude, always.

The human checkpoint required by `gyrologic/reviews/README.md` ("a criticism should be checked against the actual source document before being accepted") is satisfied by the project owner reading and confirming the review **in chat**, and this confirmation may happen after the commit already exists in git history — it is not a precondition for the review artifact being created. Confirmed 2026-08-11.

## Principle

The goal of Gyro Hub is to make this cycle visible, maintainable, and eventually automatable.
