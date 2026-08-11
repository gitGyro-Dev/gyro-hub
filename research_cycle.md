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

Adopted 2026-08-10, after external critical review of the Gyro Logic Jxiv publication (`10.51094/jxiv.5641`) exposed the value of an explicit, repeatable review step between `GitHub Documentation` and `Paper / Release`. Refined 2026-08-11 to add a strict role boundary between critique and revision and a formal disposition classification step before revision.

```text
GitHub Documentation (ideas/<topic>.md)
↓
Independent critical review (critique only, no edits to the reviewed note)
  ├─ Claude Code / Claude — reads the repository directly in-session; may write and commit a critique file to reviews/
  └─ Gemini — re-imports the repository independently for a second, uncorrelated pass
↓
ChatGPT disposition classification for each criticism
  ├─ valid
  ├─ partially valid
  ├─ misunderstanding
  ├─ needs verification
  └─ future work
↓
Check whether the criticism duplicates or substantially overlaps with an already recorded criticism
↓
Disposition record committed under reviews/ or the project-equivalent review location
↓
ChatGPT revises and commits the reviewed ideas/<topic>.md only after classification
↓
Independent re-review of the revised note
↓
repeat: classification record → revised note → re-review
↓
Paper / Release
```

This gate exists to reduce single-model bias and self-confirmation in theory development.

- Review content is never accepted automatically merely because an external AI produced it.
- Agreement between reviewers is not treated as proof of validity.
- Disagreement between reviewers is preserved, not averaged away.
- Duplicate or substantially overlapping criticisms are identified during disposition so repeated wording is not mistaken for independent evidence.
- Factual criticisms (missing citations, prior-work overlap, dates) are independently verified before being accepted.

### Disposition classification

ChatGPT classifies each material criticism before any source revision is made.

- `valid` — the criticism identifies a real problem that should be corrected or clarified in the current revision.
- `partially valid` — the criticism identifies a real issue, but only part of the claim or proposed remedy is accepted.
- `misunderstanding` — the criticism is based primarily on a misreading, scope mismatch, or conflict with an already explicit definition; the source may still be clarified if the misunderstanding is likely to recur.
- `needs verification` — the criticism depends on factual, mathematical, bibliographic, implementation, or prior-work claims that must be checked before deciding disposition.
- `future work` — the criticism is useful but extends beyond the scope of the current note or revision and should be preserved as a later research task rather than forced into the current text.

Disposition is a judgment step, not a voting mechanism. Multiple reviewers making the same criticism does not automatically change its classification. Existing review records should be checked for duplicates, near-duplicates, and previously resolved issues before a new criticism is treated as novel.

### Role boundary: critique versus revision

**Claude (and Gemini) may critique but must never edit the reviewed `ideas/<topic>.md` note, or any paper/submission material, on the project owner's behalf.** Editing and committing the revision itself is exclusively ChatGPT's role. This keeps Claude's critical distance from the text intact for the next review pass, and produces a genuine mutual check: ChatGPT proposes the fix, Claude (and Gemini) re-examine it independently, and the project owner reviews both sides.

Reference implementation: `gyrologic/reviews/review_workflow.md`, `gyrologic/reviews/critical_review_prompt.md`, `gyrologic/reviews/review_record_template.md`.

For major public manuscripts, the same principle extends to a structured **Pre-publication Multi-AI Critical Review Gate** (internal consistency, adversarial/skeptical, mathematical, literature, and blind-concept review roles) run before submission — see `gyrologic/project_cycle/2026-08-10_external_critical_review_followup.md`.

### Initial trial record

Gyro Logic is the first project applying the disposition workflow in active operation.

- Initial target: `ideas/readable_semantics_v1.md`
- Claude Round 3 disposition record: `reviews/readable_semantics_v1_claude_round3_disposition_20260811.md`
- Operational sequence: `classification record → revised note → re-review`

This initial trial is used to validate the workflow in practice before broader automation or further process expansion.

### Human checkpoint

Claude is authorized to write a critical review of an `ideas/<topic>.md` note and commit it directly to `reviews/` without asking first — critique and commit of a *review file* are both in scope. Committing a change to the *reviewed note itself* is out of scope for Claude, always.

The human checkpoint required by `gyrologic/reviews/README.md` ("a criticism should be checked against the actual source document before being accepted") is satisfied by the project owner reading and confirming the review **in chat**, and this confirmation may happen after the commit already exists in git history — it is not a precondition for the review artifact being created. Confirmed 2026-08-11.

## Principle

The goal of Gyro Hub is to make this cycle visible, maintainable, and eventually automatable.
