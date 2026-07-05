# Data

This directory contains machine-readable data for Gyro Hub.

The files in this directory are intended to become generated outputs from Gyro Developer Tools / Gyro Commands.

## Purpose

```text
Gyro Developer Tools / Gyro Commands
↓
data/*.json
↓
dashboard.json
↓
dashboard.md / GitHub Pages / Web Dashboard / GyroOS Dashboard
```

## Initial Files

| File | Purpose |
|---|---|
| `projects.json` | Project status and repository metadata |
| `publications.json` | Papers, DOI, Zenodo, Jxiv, and release information |
| `artifacts.json` | Artifact lifecycle tracking |
| `weekly_index.json` | Weekly report index |

## Principle

The data directory is not the source of truth yet. It is the structured working layer that will eventually be generated from GitHub, publications, releases, and other external sources.
