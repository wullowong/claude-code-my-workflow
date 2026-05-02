# `data/raw/` — Original Microdata

**Status:** structure committed, content gitignored.

## Purpose

Original, immutable microdata files as received from the source. **Never edited in place** — all transformations happen in `scripts/` and write to `data/processed/`.

## Conventions

- One subdirectory per data source: `data/raw/CFPS/`, `data/raw/RCRE/`, `data/raw/CHIP/`, `data/raw/MOA_county/`, etc.
- Include a `SOURCE.md` in each subdirectory recording: provider, version/wave, download date, access conditions, licensing.
- Acceptable formats: `.dta` (Stata), `.sav` (SPSS), `.csv`, `.xlsx`, `.parquet`, raw `.txt` from administrative dumps.
- **Never commit raw microdata to git.** The `.gitignore` enforces this.

## Candidate Chinese microdata sources

For this project's research question (ag insurance × smallholder labor structure):

- **CFPS** — China Family Panel Studies (Peking U.) — household labor allocation, ag income
- **CHIP** — Chinese Household Income Project — rural household income, labor structure
- **RCRE** — Rural Fixed Observation Point Survey (MOA) — village-level panel, ag operations
- **CHARLS** — China Health and Retirement Longitudinal Study — older rural population
- **MOA county-level data** — administrative ag insurance coverage, premium subsidy data
- **China Statistical Yearbook on Agriculture** — county/province aggregates

When data lands here, append it to `MEMORY.md` under "Workflow Decisions Made" with the reason for picking that source.
