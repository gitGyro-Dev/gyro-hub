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
| Gyro Developer Tools | In Development | Active | CLI / Toolkit / JSON generation |
| Gyro Hub | v0.1 | Project Cycle Setup | Hub pages and dashboard schema |

---

## Current Focus

- Gyro Project Cycle
- Research Lifecycle
- Artifact Lifecycle
- Project Hub structure
- Dashboard JSON structure
- Developer Toolkit integration
- Weekly operations

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
| projects.md | Active |
| papers.md | Active |
| roadmap.md | Active |
| dashboard.md | Active |
| dashboard.json | Manual v0.1 |
| research_cycle.md | Added |
| artifacts.md | Added |
| weekly.md | Added |
| links.md | Added |

---

## Next Actions

1. Expand `dashboard.json` into a stable initial schema.
2. Add `data/` directory when automated generation begins.
3. Connect Gyro Developer Tools to dashboard JSON generation.
4. Create first weekly report under `weekly/`.
5. Add publication sync flow for Jxiv / Zenodo / DOI.

---

This page should eventually be generated automatically from `dashboard.json` by Gyro Developer Tools / Gyro Commands.
