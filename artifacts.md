# Artifact Lifecycle

Gyro Hub manages research by artifact maturity, not only by repository or publication medium.

An artifact may begin as a rough idea and gradually become a note, PoC, document, paper, release, or feedback source.

## Lifecycle

```text
Idea
↓
Note
↓
PoC
↓
Documentation
↓
Paper
↓
Release
↓
Feedback
↓
Revision / Next Idea
```

## Stages

### Idea

An early concept, question, or hypothesis.

Examples:

- Boundary-aware runtime
- Negative definition
- Trajectory vulnerability response
- Gyro Research Cycle

### Note

A structured record of the idea.

Examples:

- Brainstorm logs
- Google Drive notes
- Thread handover prompts
- Concept sketches

### PoC

An executable or demonstrable prototype.

Examples:

- Stability timeline demo
- GyroAuth FastAPI PoC
- Dashboard JSON generator
- GitHub automation script

### Documentation

A stable explanation in GitHub docs or README files.

Examples:

- Concept docs
- API docs
- Architecture notes
- Roadmap entries

### Paper

A mature research output.

Examples:

- Jxiv preprint
- Zenodo release
- DOI-linked publication

### Release

A versioned public output.

Examples:

- GitHub Release
- Zenodo version
- Published paper version

### Feedback

Signals that return to the research cycle.

Examples:

- GitHub Issues
- X replies
- Review comments
- PoC observations
- External discussion

## Artifact Record Model

A future `artifacts.json` can track artifacts using this kind of structure:

```json
{
  "name": "Boundary-aware Runtime",
  "layer": "GyroOS",
  "stage": "Documentation",
  "status": "Active",
  "source": "GitHub docs",
  "next": "PoC design",
  "related_project": "gyroos",
  "related_paper": "Future"
}
```

## Principle

Project Hub should show where each artifact is in the lifecycle, what its next action is, and which source currently owns the latest version.
