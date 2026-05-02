# Project Memory — Agricultural Insurance and Smallholder Labor Upgrading in China

Cross-session learnings for this specific project.
When the user corrects me or confirms a non-obvious choice worked, append a `[LEARN:category]` entry below.

> **Format:** `[LEARN:category] short rule. **Why:** the reason. **How to apply:** when this kicks in.`
> Recent entries go at the bottom of each section. Keep this file under ~150 lines.

> **Note:** the original template's 24 [LEARN] entries (about template development, dogfooding, drift prevention) are archived locally at `MEMORY.template-archive.md` (gitignored). Reference them when designing new template infrastructure; ignore them for project work.

---

## User Profile & Working Style

[LEARN:user] Project owner is leading an empirical research project on policy-based agricultural insurance and smallholder labor structure upgrading in China. Conference paper target. Empirical methods on Chinese microdata; bilingual EN/ZH context. **How to apply:** assume sophistication on Chinese ag-policy context (PAY since 2007, premium subsidy structure, county pilots) and on standard empirical-econ identification. Don't over-explain basics; do flag when a method is weak for this setting.

[LEARN:feedback] User prefers structured, precise, and rigorous collaboration over fast turnaround — even if it takes more time. **Why:** stated in onboarding session 2026-05-01. **How to apply:** ask clarifying questions before acting on ambiguous requests; explain reasoning; surface trade-offs; don't optimize for speed at the cost of correctness.

[LEARN:feedback] Visual outputs (figures, tables, diagrams) must be polished and publication-ready — no draft figures shipped. **Why:** stated in onboarding 2026-05-01. **How to apply:** apply this to every figure-producing task — set proper labels, units, sources, captions, fonts, colors; check overflow; never present a "rough" version as the final.

[LEARN:feedback] First few sessions: check in more often than usual so user can learn how the workflow operates. **Why:** stated in onboarding 2026-05-01. **How to apply:** after each phase of a multi-phase task, surface intermediate state in 1-2 sentences before continuing. Phase out as user gets fluent.

---

## Project Context

[LEARN:project] Outputs: LaTeX manuscript (primary) + Word draft + conference slide deck. **Why:** answer to onboarding question 2026-05-01. **How to apply:** when generating analysis outputs (tables, figures), produce LaTeX-compatible versions first; Word renders are derivative.

[LEARN:project] Statistical stack: Stata (primary) + R + Python (auxiliary). Scripts live under `scripts/Stata/`, `scripts/R/`, `scripts/Python/`. Numbered convention (`01_clean.do`, `02_construct.do`, `03_analyze.do`). **Why:** answer to onboarding 2026-05-01. **How to apply:** propose Stata first for econometric estimation; use R for tidyverse cleaning + ggplot figures (since `/review-r` and `/audit-reproducibility` are R-aware); reserve Python for web-scraping or text processing tasks.

[LEARN:project] Pre-staged target journals (calibration data in `.claude/references/journal-profiles.md`): AJAE, China Economic Review, Food Policy, World Development, China Agricultural Economic Review, AEPP, Journal of Development Studies, Agricultural Economics. **Why:** answer to onboarding 2026-05-01. **How to apply:** these are valid arguments to `/review-paper --peer [journal]`; if the user names a journal outside this list, prompt to add a profile before simulating.

---

## Domain Conventions

<!-- Append entries as we discover them. Examples that may emerge:
     [LEARN:terminology] Use "smallholder" not "small farmer" in EN copy.
     [LEARN:data] Variable convention: county_id is 6-digit GB/T 2260 code.
     [LEARN:identification] Treatment variable: 1[county receives policy in year t]. -->

---

## Workflow Decisions Made

<!-- Append decisions here. Format: date — decision — short rationale.
     Examples:
     2026-05-15 — using CFPS over CHIP — better farm labor variables
     2026-06-01 — DiD with Callaway-SantAnna estimator — staggered adoption -->

---
