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
| GyroAuth | v2.0 / Publications | Primary and applied English/Japanese Jxiv publications completed / PoC available | Publication maintenance, real-world evaluation, production integration |
| Gyro Developer Tools | In Development | Publication automation candidates added | DOI checks, duplicate checks, translation linkage, publication synchronization |
| Gyro Hub | v0.1 | Project Cycle Active | Continue weekly, dashboard, and release review operations |

---

## Recent Publications

### GyroAuth Primary Paper — English

**GyroAuth: Authentication as Stability-Based Selection over State Convergence**

- Jxiv: Published
- Role: Primary manuscript
- DOI: [10.51094/jxiv.4600](https://doi.org/10.51094/jxiv.4600)

### GyroAuth Primary Paper — Japanese

**GyroAuth：状態収束に対する安定性に基づく認証**

- Jxiv: Published
- Role: Japanese translation
- DOI: [10.51094/jxiv.5341](https://doi.org/10.51094/jxiv.5341)

### GyroAuth Applied Research — English

**Trajectory-Based Vulnerability Response: A GyroAuth Applied Model for Post-Login Security Monitoring**

- Jxiv: Published
- DOI: [10.51094/jxiv.5416](https://doi.org/10.51094/jxiv.5416)

### GyroAuth Applied Research — Japanese

**Trajectoryに基づく脆弱性対応：ログイン後セキュリティ監視のためのGyroAuth応用モデル**

- Jxiv: Published
- DOI: [10.51094/jxiv.5440](https://doi.org/10.51094/jxiv.5440)

---

## Current Focus

- Gyro Logic v3.1 release review
- GyroAuth primary publication reflection
- GyroAuth applied publication reflection
- English/Japanese publication linkage
- Publication duplicate and missing-DOI checks
- Real-world dataset and production integration planning

---

## GyroAuth Position

```text
Gyro Logic
↓
GyroOS
↓
GyroAuth
```

Primary formulation:

```text
Authentication = Stability-based Selection over State Convergence
```

Applied extension:

```text
Boundary / Negative Definition
↓
Trajectory Detection
↓
Stability Response
```

Central applied proposition:

```text
valid events != stable trajectory
```

### Publication and PoC Status

| Item | Status |
|---|---|
| Primary English Jxiv publication | Completed |
| Primary Japanese Jxiv publication | Completed |
| Applied conceptual model | Completed |
| Applied minimal PoC | Completed |
| Applied English Jxiv publication | Completed |
| Applied Japanese Jxiv publication | Completed |
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
| 2026-W29 | [Gyro Weekly 2026-W29](weekly/2026-W29.md) | Updated |

---

## Developer Toolkit Integration

- Dashboard generator: `tools/gyro/dashboard.py`
- Dashboard generation design: `docs/gyro_dashboard_generation.md`
- Document consistency proposal: `gyro-dev-tools` Issue #2
- DOI/publication synchronization proposal: `gyro-dev-tools` Issue #3

Publication automation candidates:

- DOI publication verification
- Jxiv DOI resolution-state checks
- Publications JSON synchronization
- English/Japanese publication linkage
- Translation DOI linkage
- Publication duplicate and missing-DOI checks
- Weekly publication reflection
- X publication-status tracking

---

## Next Actions

1. Continue Gyro Logic v3.1 release review.
2. Maintain GyroAuth English/Japanese publication linkage.
3. Record X publication communication when available.
4. Evaluate real-world datasets and production integration boundaries.
5. Evaluate DOI, duplicate, and publication synchronization tooling.

---

This page reflects the latest accepted Project Cycle Update.
