# `manuscript/` — Paper Drafts and Final Outputs

Authoritative location for the paper's writing artifacts.

## Layout

```
manuscript/
├── paper.tex                 # LaTeX source (primary draft — single source of truth)
├── paper.docx                # Word version (derived from paper.tex; for non-LaTeX co-authors / venues)
├── tables/                   # Final tables (.tex from Stata/R esttab/stargazer)
├── figures/                  # Final figures (.pdf preferred; .png OK)
└── appendix.tex              # Supplementary results, robustness, supporting derivations
```

## Workflow

1. LaTeX is the **single source of truth**. Edit `paper.tex` for content; render with `xelatex` (3-pass + bibtex; see CLAUDE.md "Commands").
2. **Tables and figures are not edited here** — they're produced by `scripts/Stata/` or `scripts/R/` and copied (or `\input{}`'d) into the LaTeX. Edit the upstream script, rerun, copy.
3. The Word version is generated from the LaTeX when needed (Pandoc: `pandoc paper.tex -o paper.docx --bibliography=../Bibliography_base.bib`). Do not hand-edit `paper.docx` — the LaTeX is canonical.
4. The conference slide deck lives in `Slides/` (Beamer) and `Quarto/` (RevealJS), not here. It references the same figures from `manuscript/figures/`.

## Reproducibility contract

Per `.claude/rules/replication-protocol.md`, every numeric claim in `paper.tex` must trace back to a script under `scripts/` that produces that number. `/audit-reproducibility` enforces this before submission.

## Submission checklist (apply before each version of the paper goes out)

- [ ] All tables/figures regenerated from the latest pipeline (no stale outputs).
- [ ] `Bibliography_base.bib` validated (`/validate-bib`).
- [ ] `/review-paper` single-pass review clean.
- [ ] `/audit-reproducibility` PASS on all referenced numeric claims.
- [ ] `/verify-claims` clean (no hallucinated citations or fabricated facts).
- [ ] Word version rendered fresh from current LaTeX.
