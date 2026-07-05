# Gyro Hub

> The official gateway to the Gyro Ecosystem and Gyro Project Cycle.

[日本語版はこちら](README_jp.md)

Gyro Hub is the public and operational entry point for the Gyro project.

Gyro is a research and development ecosystem exploring how stable behavior emerges from structured observation rather than exact matching.

Instead of asking:

> Are these two things identical?

Gyro asks:

> Does the structure remain stable despite deviation?

---

## Gyro Project Cycle

Gyro Hub is not only a dashboard or a repository index. It exists to connect and operate the full Gyro research cycle.

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

This cycle is the operating model for growing Gyro from theory into runtime, application, publication, feedback, and further research.

---

## Gyro Ecosystem

```text
                 Gyro Hub
                     |
   +-----------------+-----------------+
   |                 |                 |
Gyro Logic       GyroOS          GyroAuth
   |                 |                 |
   +-----------------+-----------------+
                     |
         Gyro Developer Tools
                     |
 Papers • DOI • Releases • Demos • X • Feedback
```

---

## Core Projects

| Project | Role | Repository |
|---------|------|------------|
| Gyro Logic | Theoretical foundation | [gitGyro-Dev/gyrologic](https://github.com/gitGyro-Dev/gyrologic) |
| GyroOS | Runtime architecture | [gitGyro-Dev/gyroos](https://github.com/gitGyro-Dev/gyroos) |
| GyroAuth | Stability-based authentication | [gitGyro-Dev/gyroauth](https://github.com/gitGyro-Dev/gyroauth) |
| Gyro Developer Tools | GitHub operation and development toolkit | [gitGyro-Dev/gyro-dev-tools](https://github.com/gitGyro-Dev/gyro-dev-tools) |
| Gyro Hub | Project Hub and ecosystem entry point | [gitGyro-Dev/gyro-hub](https://github.com/gitGyro-Dev/gyro-hub) |

---

## Project Layers

| Layer | Project | Description |
|-------|---------|-------------|
| Theory | Gyro Logic | Defines the conceptual and mathematical foundation of Gyro. |
| Runtime | GyroOS | Implements Gyro concepts as runtime architecture. |
| Application | GyroAuth | Applies stability-based selection to authentication. |
| Development | Gyro Developer Tools | Provides tooling for GitHub operations, releases, and development workflows. |
| Hub | Gyro Hub | Connects the ecosystem as the public entry point and project-cycle dashboard. |

---

## Hub Pages

| Page | Purpose |
|---|---|
| [Projects](projects.md) | Project overview |
| [Papers](papers.md) | Publications, DOI, and research outputs |
| [Roadmap](roadmap.md) | Development and research direction |
| [Dashboard](dashboard.md) | Current ecosystem status |
| [Research Cycle](research_cycle.md) | Gyro Project Cycle operating model |
| [Artifacts](artifacts.md) | Artifact lifecycle and maturity tracking |
| [Weekly](weekly.md) | Weekly operating report structure |
| [Links](links.md) | External ecosystem entry points |

---

## Data and Dashboard Direction

Gyro Hub separates data from display.

```text
Gyro Developer Tools / Gyro Commands
↓
dashboard.json
├─ dashboard.md
├─ GitHub Pages
├─ Web Dashboard
└─ GyroOS Dashboard
```

Principles:

- Dashboard is a display layer, not a source of truth.
- GitHub is the working source of truth for active research.
- Papers and DOI are mature public outputs.
- Google Drive is storage and archive.
- NotebookLM is a knowledge hub.
- X is used for intermediate research communication.

---

## Current Status

| Project | Status |
|---------|--------|
| Gyro Logic | Released |
| GyroOS | In Design |
| GyroAuth | PoC Available / Publication Track |
| Gyro Developer Tools | In Development |
| Gyro Hub | Project Cycle Setup |

---

Gyro Hub connects theory, runtime, applications, research operations, publications, and feedback into a continuously growing research platform.
