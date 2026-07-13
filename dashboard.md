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
| Gyro Logic | v3.1 | In Progress / Release Candidate Draft | Final review, figures, release notes, release decision |
| GyroOS | v4.0 | No change / In Design | Runtime architecture / Boundary-aware runtime |
| GyroAuth | v2.0 / Applied Research | Jxiv English and Japanese publications completed / PoC available | DOI resolution recheck, real-world dataset evaluation |
| Gyro Developer Tools | In Development | Publication automation candidates added | DOI checks and publication synchronization |
| Gyro Hub | v0.1 | Project Cycle Active | Continue weekly, dashboard, and release review operations |

---

## Recent Publications

### GyroAuth Applied Research — English

**Trajectory-Based Vulnerability Response: A GyroAuth Applied Model for Post-Login Security Monitoring**

- Jxiv: Published
- DOI: [10.51094/jxiv.5416](https://doi.org/10.51094/jxiv.5416)

### GyroAuth Applied Research — Japanese

**Trajectoryに基づく脆弱性対応：ログイン後セキュリティ監視のためのGyroAuth応用モデル**

- Jxiv: Published
- DOI: [10.51094/jxiv.5440](https://doi.org/10.51094/jxiv.5440)

DOI resolution may lag behind Jxiv publication. The DOI metadata is registered as confirmed, while link resolution remains subject to recheck.

---

## Current Focus

- Gyro Logic v3.1 release review
- GyroAuth Trajectory-Based Vulnerability Response publication reflection
- English/Japanese publication linkage
- DOI resolution recheck
- Real-world dataset evaluation planning
- DOI and publication synchronization tooling

---

## GyroAuth Applied Model

```text
Boundary / Negative Definition
↓
Trajectory Detection
↓
Stability Response
```

Central proposition:

```text
valid events != stable trajectory
```

Individually valid events may still form an unstable or impermissible post-login operation Trajectory.

### Publication and PoC Status

| Item | Status |
|---|---|
| Conceptual model | Completed |
| Minimal PoC | Completed |
| English Jxiv publication | Completed |
| Japanese Jxiv publication | Completed |
| Real-world dataset evaluation | Future work |
| Production integration | Future work |

---

## Gyro Logic v3.1 Progress

### Completed

- Core Definitions
- README
- README Japanese
- Boundary
- Boundary State
- Documentation Index
- Release Candidate rc1

### In Progress

- Paper final review
- Figures decision
- Release notes
- Jxiv preparation
- Release decision

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
| 2026-W29 | [Gyro Weekly 2026-W29](weekly/2026-W29.md) | Created |

---

## Developer Toolkit Integration

- Dashboard generator: `tools/gyro/dashboard.py`
- Dashboard generation design: `docs/gyro_dashboard_generation.md`
- Document consistency proposal: `gyro-dev-tools` Issue #2

Publication automation candidates:

- DOI publication verification
- Jxiv DOI resolution-state checks
- Publications JSON synchronization
- English/Japanese publication linkage
- Translation DOI linkage
- Weekly publication reflection
- X publication-status tracking

---

## Next Actions

1. Recheck DOI resolution for `10.51094/jxiv.5416` and `10.51094/jxiv.5440`.
2. Continue Gyro Logic v3.1 release review.
3. Record Japanese publication communication when posted.
4. Evaluate real-world datasets for the GyroAuth applied model.
5. Evaluate DOI and publication synchronization tooling.

---

This page reflects the latest accepted Project Cycle Update.
