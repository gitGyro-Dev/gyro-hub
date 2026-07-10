# Dashboard

> Current overview of the Gyro Ecosystem and Gyro Project Cycle.

```text
Dashboard = current position
Weekly    = weekly flow
Roadmap   = future direction
```

---

## Ecosystem Status

| Project | Version / Track | Status | Next |
|---|---|---|---|
| Gyro Logic | v3.1 | In Progress | Paper, figures, Jxiv preparation, release planning |
| GyroOS | v4.0 | No change / In Design | Runtime architecture / Boundary-aware runtime |
| GyroAuth | v2.0 | No change / PoC Available | Paper and application refinement |
| Gyro Developer Tools | In Development | Issue #2 opened | Document consistency and synchronization checks |
| Gyro Hub | v0.1 | Project Cycle Active | Continue weekly and dashboard reflection |

---

## Current Focus

- Gyro Logic v3.1
- Core Definition Refinement
- Boundary Integration
- Boundary State Integration
- Paper preparation
- Jxiv preparation
- Release v3.1 planning
- Document consistency tooling

---

## Gyro Logic v3.1 Progress

### Completed

- Core Definitions
- README
- README Japanese
- Boundary
- Boundary State
- Documentation Index

### In Progress

- Paper English
- Paper Japanese
- Figures
- Jxiv preparation
- Release notes

### Document Relationship

```text
Core Definitions
↓
Boundary
↓
Boundary State
```

The invariant core remains:

```text
Structure → Slice → Stability
```

---

## Data Relationship

```text
data/projects.json
+ data/publications.json
+ data/artifacts.json
+ data/roadmap.json
+ data/links.json
+ data/weekly_index.json
↓
dashboard.json
↓
dashboard.md
```

---

## Weekly Reports

| Week | Report | Status |
|---|---|---|
| 2026-W27 | [Gyro Weekly 2026-W27](weekly/2026-W27.md) | Created |
| 2026-W28 | [Gyro Weekly 2026-W28](weekly/2026-W28.md) | Created |

---

## Developer Toolkit Integration

- Dashboard generator: `tools/gyro/dashboard.py`
- Dashboard generation design: `docs/gyro_dashboard_generation.md`
- Document consistency proposal: `gyro-dev-tools` Issue #2

Candidate functions:

- Core Definitions-based consistency checks
- README / paper / docs synchronization checks
- `docs_index` automatic generation
- Document dependency visualization
- Release checklist generation

---

## Next Actions

1. Continue Gyro Logic v3.1 paper work.
2. Prepare Jxiv submission.
3. Prepare X communication.
4. Plan Gyro Logic v3.1 release.
5. Evaluate Developer Toolkit Issue #2.
6. Confirm final repository paths for v3.1 paper files.

---

This page reflects the latest accepted Project Cycle Update.
