# Dashboard

> Current overview of the Gyro Ecosystem and Gyro Project Cycle.

Dashboard is a display layer of Gyro Hub. It summarizes the current position of the project, while source information remains in GitHub, papers, releases, Google Drive, NotebookLM, X, and other external sources.

```text
Dashboard = current position
Weekly    = weekly flow
Roadmap   = future direction
```

---

## Ecosystem Status

| Project | Version / Track | Status | Next |
|---|---|---|---|
| Gyro Logic | v3.0 | Released | Theory expansion / Boundary refinement |
| GyroOS | v4.0 | In Design | Runtime architecture / Boundary-aware runtime |
| GyroAuth | v2.0 | PoC Available / Publication Track | Paper and application refinement |
| Gyro Developer Tools | In Development | Active | Dashboard generation command design |
| Gyro Hub | v0.1 | Project Cycle Setup | Data-driven dashboard preparation |

---

## Current Focus

- Gyro Project Cycle
- Research Lifecycle
- Artifact Lifecycle
- Project Hub structure
- Data directory
- Root dashboard aggregation
- Weekly operations
- Developer Toolkit dashboard generation design

---

## Project Cycle

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

See: [Research Cycle](research_cycle.md)

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

Root `dashboard.json` is the aggregated display-ready summary.

`data/*.json` contains structured working data that can later be generated or synchronized by Gyro Developer Tools.

---

## Latest Releases / Publications

- Gyro Logic v3.0
- GyroOS v3.1
- GyroAuth v2.0.0
- Gyro Logic Jxiv English DOI: 10.51094/jxiv.4159
- Gyro Logic Jxiv Japanese DOI: 10.51094/jxiv.4597
- Gyro Logic Zenodo v2.4 DOI: 10.5281/zenodo.19674375

---

## Hub Pages

| Page | Status |
|---|---|
| README.md | Active |
| README_jp.md | Added |
| projects.md | Active |
| papers.md | Active |
| roadmap.md | Active |
| dashboard.md | Active |
| dashboard.json | Manual v0.2 |
| research_cycle.md | Added |
| artifacts.md | Added |
| weekly.md | Added |
| links.md | Added |

---

## Data Files

| File | Status |
|---|---|
| data/README.md | Added |
| data/projects.json | Added |
| data/publications.json | Added |
| data/artifacts.json | Added |
| data/roadmap.json | Added |
| data/links.json | Added |
| data/weekly_index.json | Updated |

---

## Weekly Reports

| Week | Report | Status |
|---|---|---|
| 2026-W27 | [Gyro Weekly 2026-W27](weekly/2026-W27.md) | Created |
| 2026-W28 | [Weekly Template](weekly/_template.md) | Planned |

---

## Developer Toolkit Integration

Dashboard generation command design:

- Repository: `gitGyro-Dev/gyro-dev-tools`
- Design: `docs/gyro_dashboard_generation.md`
- Proposed command: `python tools/gyro/dashboard.py --repo gyro-hub`

---

## Next Actions

1. Implement local dashboard generation prototype in Gyro Developer Tools.
2. Generate root `dashboard.json` from `data/*.json`.
3. Generate `dashboard.md` from root `dashboard.json`.
4. Continue weekly reports.
5. Refine artifact tracking schema.

---

This page should eventually be generated automatically from `dashboard.json` and `data/*.json` by Gyro Developer Tools / Gyro Commands.
