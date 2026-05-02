# `data/processed/` — Analysis-Ready Datasets

**Status:** structure committed, content gitignored.

## Purpose

Cleaned, merged, analysis-ready datasets produced by scripts in `scripts/Stata/`, `scripts/R/`, or `scripts/Python/`. These files are **regeneratable** from `data/raw/` via the numbered scripts.

## Conventions

- File naming: `{level}_{topic}_{version}.dta` — e.g., `household_panel_v1.dta`, `county_treatment_v2.csv`.
- Document provenance in script headers (which raw inputs, which transformations).
- Never edit in place. If you need a different cleaning, modify the script and rerun.
- Versioning: bump `_vN` when the analytical sample definition changes (e.g., adding a wave, changing inclusion criteria). Old versions can be deleted once the manuscript no longer references them.

## Reproducibility

Per `.claude/rules/replication-protocol.md`, every numeric claim in the paper must trace back to a script that reads from `data/processed/` (and ultimately `data/raw/`). The `/audit-reproducibility` skill enforces this.
