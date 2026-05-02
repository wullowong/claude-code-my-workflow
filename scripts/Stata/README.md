# `scripts/Stata/` — Stata Pipeline

Primary statistical software for this project. Scripts run on `data/raw/` → `data/processed/` → tables/figures.

## Naming convention

Numbered, lower-case, kebab-case, single verb in name:

```
00_run_all.do          # master script: runs 01..N in order
01_load.do             # read raw data, light typing
02_clean.do            # filter, recode, merge across sources
03_construct.do        # build analytic variables (treatment, controls, outcomes)
04_describe.do         # summary statistics, balance tables
05_estimate.do         # main regressions (DiD / FE / IV / matching)
06_robustness.do       # alternative samples, specifications, placebo tests
07_tables.do           # esttab / estout to LaTeX → manuscript/tables/
08_figures.do          # publication graphs → manuscript/figures/
```

## Outputs

- `_outputs/` (gitignored): intermediate logs, `.ster` estimates, `.tex` tables before being copied into `manuscript/`.
- Final tables/figures used by the paper land in `manuscript/tables/` and `manuscript/figures/`.

## Header template (copy into every .do file)

```stata
*------------------------------------------------------------------------------
* Script: 0X_name.do
* Purpose: [one-line purpose]
* Inputs:  data/processed/INPUT.dta
* Outputs: data/processed/OUTPUT.dta  (or scripts/Stata/_outputs/...)
* Author:  [name]
* Created: YYYY-MM-DD
*------------------------------------------------------------------------------
version 17
clear all
set more off
*------------------------------------------------------------------------------
```

## Reproducibility

Run the entire pipeline from scratch with `do scripts/Stata/00_run_all.do`. Any deviation from "load → clean → analyze → output" should be documented in `MEMORY.md`.
