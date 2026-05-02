# CLAUDE.MD -- Academic Project Development with Claude Code

<!-- HOW TO USE: Replace [BRACKETED PLACEHOLDERS] with your project info.
     Customize Beamer environments and CSS classes for your theme.
     Keep this file under ~150 lines — Claude loads it every session.
     See the guide at docs/workflow-guide.html for full documentation. -->

**Project:** Agricultural Insurance and Smallholder Labor Upgrading in China
**Institution:** [INSTITUTION — please fill in]
**Branch:** main

> **Project type — empirical research paper.** Chinese microdata → Stata + R + Python scripts → regression tables → drafts in LaTeX (primary) and Word, plus a conference slide deck. Not a lecture course. The slides infrastructure stays available but is secondary; data analysis and the manuscript are the main objects.

---

## Core Principles

- **Plan first** -- enter plan mode before non-trivial tasks; save plans to `quality_reports/plans/`
- **Verify after** -- compile/render and confirm output at the end of every task
- **Single source of truth** -- LaTeX manuscript is the authoritative draft; Word version + conference slides derive from it
- **Quality gates** -- nothing ships below 80/100
- **[LEARN] tags** -- when corrected, save `[LEARN:category] wrong → right` to [MEMORY.md](MEMORY.md)

Cross-session context lives in [MEMORY.md](MEMORY.md); past plans, specs, and session logs are in [quality_reports/](quality_reports/).

---

## Folder Structure

```
agri-insurance-labor-china/
├── CLAUDE.MD                    # This file
├── MEMORY.md                    # Cross-session [LEARN] entries
├── .claude/                     # Rules, skills, agents, hooks, references
├── data/
│   ├── raw/                     # Original Chinese microdata (gitignored)
│   └── processed/               # Analysis-ready datasets (gitignored)
├── scripts/
│   ├── Stata/                   # Stata .do files (numbered: 01_clean.do …)
│   ├── R/                       # R scripts; outputs land in scripts/R/_outputs/
│   └── Python/                  # Python scripts (auxiliary)
├── manuscript/                  # LaTeX paper + Word draft + final tables/figures
├── Bibliography_base.bib        # Centralized bibliography (BibTeX)
├── Figures/                     # Figures for paper and slides
├── quality_reports/             # Plans, specs, session logs, decisions
├── explorations/                # Research sandbox
├── templates/                   # Session log, requirements spec templates
└── master_supporting_docs/      # Reference papers and prior slides

# Conference slide deck (secondary; activated when a venue is selected)
├── Slides/    Quarto/    Preambles/header.tex    docs/
```

---

## Commands

```bash
# --- Data analysis (primary) ---
stata -b do scripts/Stata/01_clean.do          # Stata
Rscript scripts/R/01_clean.R                    # R (outputs → scripts/R/_outputs/)
python scripts/Python/01_clean.py               # Python

# --- LaTeX manuscript (3-pass XeLaTeX + bibtex) ---
cd manuscript && TEXINPUTS=../Preambles:$TEXINPUTS xelatex -interaction=nonstopmode paper.tex
BIBINPUTS=..:$BIBINPUTS bibtex paper
TEXINPUTS=../Preambles:$TEXINPUTS xelatex -interaction=nonstopmode paper.tex
TEXINPUTS=../Preambles:$TEXINPUTS xelatex -interaction=nonstopmode paper.tex

# --- Conference slides (secondary) ---
# Same Beamer compile from Slides/. Quarto deploy:
./scripts/sync_to_docs.sh LectureN

# --- Quality / consistency utilities ---
python scripts/quality_score.py Quarto/file.qmd     # Quality score (slides)
./scripts/check-palette-sync.sh                     # LaTeX ↔ SCSS color parity
./scripts/check-surface-sync.sh                     # Doc surface counts in sync
```

**Palette contract:** color names in `Preambles/header.tex` must match SCSS variables in `Quarto/theme-template.scss`. See [`Preambles/README.md`](Preambles/README.md).

---

## Quality Thresholds (advisory)

| Score | Checkpoint | Meaning |
|-------|------|---------|
| 80 | Commit | Good enough to save |
| 90 | PR | Ready for deployment |
| 95 | Excellence | Aspirational |

Enforced by `/commit` (halts + asks for override); not enforced by a git pre-commit hook.

---

## Skills Quick Reference

| Command | What It Does |
|---------|-------------|
| `/compile-latex [file]` | 3-pass XeLaTeX + bibtex |
| `/deploy [LectureN]` | Render Quarto + sync to docs/ |
| `/extract-tikz [LectureN]` | TikZ → PDF → SVG |
| `/new-diagram [snippet] [output.tex]` | Scaffold a TikZ diagram from the gallery with prevention + review |
| `/proofread [file]` | Grammar/typo/overflow review |
| `/visual-audit [file]` | Slide layout audit |
| `/pedagogy-review [file]` | Narrative, notation, pacing review |
| `/review-r [file]` | R code quality review |
| `/qa-quarto [LectureN]` | Adversarial Quarto vs Beamer QA |
| `/slide-excellence [file]` | Combined multi-agent review |
| `/translate-to-quarto [file]` | Beamer → Quarto translation |
| `/validate-bib` | Cross-reference citations |
| `/devils-advocate` | Challenge slide design |
| `/create-lecture` | Full lecture creation |
| `/commit [msg]` | Stage, commit, PR, merge |
| `/lit-review [topic]` | Literature search + synthesis |
| `/research-ideation [topic]` | Research questions + strategies |
| `/interview-me [topic]` | Interactive research interview |
| `/review-paper [file]` | Manuscript review (single-pass / `--adversarial` / `--peer <journal>` simulated pipeline) |
| `/respond-to-referees [report] [manuscript]` | R&R cross-reference + response draft |
| `/data-analysis [dataset]` | End-to-end R analysis |
| `/audit-reproducibility [paper]` | Enforce replication tolerance thresholds on paper ↔ code |
| `/learn [skill-name]` | Extract discovery into persistent skill |
| `/context-status` | Show session health + context usage |
| `/deep-audit` | Repository-wide consistency audit |
| `/permission-check` | Diagnose permission layers when prompts fire unexpectedly |
| `/seven-pass-review` | Seven-pass adversarial manuscript review (parallel forked subagents) |
| `/verify-claims [file]` | Chain-of-Verification fact-check (forked verifier, fresh context) |
| `/checkpoint [topic]` | Save a structured state snapshot (active plan, decisions, file pointers, next actions) before stopping or handing off |
| `/preregister [--style osf|aspredicted|aea-rct]` | Draft a preregistration document (OSF / AsPredicted / AEA RCT Registry) from a research spec |

---

<!-- CUSTOMIZE: Add Beamer environments / Quarto CSS classes when you start the conference deck. -->

## Beamer Custom Environments

| Environment | Effect | Use Case |
| --- | --- | --- |
| _(none yet — populate when conference deck is started)_ | | |

## Quarto CSS Classes

| Class | Effect | Use Case |
| --- | --- | --- |
| _(none yet — populate when conference deck is started)_ | | |

---

## Current Project State

| Artifact | Path | Status |
| --- | --- | --- |
| Manuscript (LaTeX) | `manuscript/paper.tex` | Not started |
| Manuscript (Word) | `manuscript/paper.docx` | Not started |
| Conference deck | `Slides/`, `Quarto/` | HelloWorld demo only |
| Stata pipeline | `scripts/Stata/` | Empty scaffold |
| R pipeline | `scripts/R/` | Empty scaffold |
| Python utilities | `scripts/Python/` | Empty scaffold |
| Bibliography | `Bibliography_base.bib` | Seed entries (anchor papers) |
