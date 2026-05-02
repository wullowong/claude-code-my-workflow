<!-- Adapted from Hugo Sant'Anna's clo-author (github.com/hugosantanna/clo-author),
     used with permission. Journal-calibration schema credit: Hugo Sant'Anna. -->

# Journal Profiles

Calibration data for the `/review-paper --peer [journal]` simulated peer-review pipeline. Each profile tells the editor how to select referees (disposition-pool weights), what concerns that journal typically emphasizes, and any journal-specific formatting conventions.

**How this file is used.** The `editor` agent reads this file before each `--peer` run, picks the requested `[journal]`, and uses its Referee-pool weights + Typical concerns to select two referees with different dispositions and to seed their pet-peeve priors.

**Customizing for your field.** This file ships with **five top-5 econ journals** as a concrete example. To use `--peer` for a different field (finance, political science, biology, CS, etc.), copy `templates/journal-profile-template.md` into a new section below, fill in the schema, and reference it by the short name you define. See the [Field adaptation](#field-adaptation) section at the bottom.

---

## Schema

Every profile has these fields:

- **Short name** — the string you pass to `--peer [name]` (e.g., `AER`, `QJE`).
- **Focus** — what the journal publishes; what it doesn't.
- **Bar** — what it takes to clear the desk; typical acceptance rate context.
- **Domain-referee adjustments** — how the substance referee should re-weight their dimensions for this journal (e.g., "Contribution 30 → 35, External validity 15 → 20 for AER policy relevance").
- **Methods-referee adjustments** — how the methods referee should re-weight for this journal (e.g., "Identification 35 → 40 for QJE credibility bar").
- **Typical concerns** — 3–5 direct-quote questions a referee at this journal will ask.
- **Referee-pool weights** — probability weights over the 6 dispositions (STRUCTURAL / CREDIBILITY / MEASUREMENT / POLICY / THEORY / SKEPTIC). Editor draws two *different* dispositions from this distribution.
- **Table format override** (optional) — any journal-specific formatting rule. AEA journals: no significance stars. QJE: three-decimal point estimates.

---

## Econ Top-5

### American Economic Review (AER)

**Short name:** `AER`

**Focus.** General-interest economics across all fields. Strongest bar for substantive contribution and policy relevance. Favors credible identification + interpretable magnitudes + clear narrative over technical novelty.

**Bar.** "Publishing here means the top-10 people in your field will read it." Topic must matter beyond specialists. Contribution must be crisp in one paragraph.

**Domain-referee adjustments.**
- Contribution 30 → 35 (the bar on importance is higher)
- External validity 15 → 20 (generalizability matters more)
- Fit 10 → 5 (AER publishes across fields; fit is less of a constraint)

**Methods-referee adjustments.**
- Identification 35 → 40 (credibility is load-bearing)
- Replication 5 → 10 (AER Data and Code Availability Policy is strict)

**Typical concerns.**
- "Is the research question important enough for a general-interest journal?"
- "Is the identification strategy credible to a skeptical non-specialist?"
- "Does the magnitude tell us something we didn't already know?"
- "Are the robustness checks addressing the obvious threats, or are they theater?"
- "Is the replication package complete enough for the AEA Data Editor?"

**Referee-pool weights.**
- CREDIBILITY: 0.30
- POLICY: 0.25
- STRUCTURAL: 0.15
- MEASUREMENT: 0.15
- THEORY: 0.05
- SKEPTIC: 0.10

**Table format override.** No significance stars (AEA policy since 2023). Use SE in parentheses only; indicate p-values in notes if needed.

---

### Quarterly Journal of Economics (QJE)

**Short name:** `QJE`

**Focus.** Identification-first empirical work and theory with sharp predictions. Taste for clever natural experiments, rich data, and economic insight over methodological flash.

**Bar.** Identification must be near-airtight. Willing to accept narrow settings if the design is exceptional. Wants a paper that could be taught in a graduate class.

**Domain-referee adjustments.**
- Contribution 30 → 30 (unchanged)
- Substance 20 → 25 (taste matters — clever > competent)

**Methods-referee adjustments.**
- Identification 35 → 45 (this is the QJE house style)
- Robustness 15 → 10 (QJE referees are less tolerant of robustness-as-theater)

**Typical concerns.**
- "Is the research design genuinely clever, or is this yet another DiD?"
- "Does the first-stage / exclusion restriction / parallel-trends assumption have teeth?"
- "Would I teach this paper's identification strategy?"
- "What's the one-sentence economic insight here?"

**Referee-pool weights.**
- CREDIBILITY: 0.40
- STRUCTURAL: 0.20
- MEASUREMENT: 0.15
- POLICY: 0.10
- THEORY: 0.10
- SKEPTIC: 0.05

**Table format override.** Three-decimal point estimates standard; SE in parentheses.

---

### Journal of Political Economy (JPE)

**Short name:** `JPE`

**Focus.** Economic theory + empirical work tightly connected to theory. Chicago-flavored taste: markets, incentives, mechanism. Less sympathetic to pure reduced-form.

**Bar.** Theory component must be present and nontrivial — even in empirical papers, "what does the theory predict before we estimate" is expected.

**Domain-referee adjustments.**
- Contribution 30 → 30 (unchanged)
- Substance 20 → 30 (theory connection is load-bearing)

**Methods-referee adjustments.**
- If paper type is `theory+empirics`: Model 20 → 30, Prediction sharpness 25 → 30
- If paper type is `reduced-form`: Identification 35 → 30, expect explicit theoretical framing

**Typical concerns.**
- "What does the theory predict, and does the empirical work speak to that prediction?"
- "Is the mechanism spelled out, or are we just estimating a reduced-form coefficient?"
- "Do the magnitudes match what a reasonable model would imply?"
- "Is the paper arguing against a specific alternative theory, or waving at 'possible mechanisms'?"

**Referee-pool weights.**
- THEORY: 0.30
- STRUCTURAL: 0.25
- CREDIBILITY: 0.15
- MEASUREMENT: 0.10
- POLICY: 0.10
- SKEPTIC: 0.10

**Table format override.** None journal-specific.

---

### Econometrica (ECMA)

**Short name:** `ECMA`

**Focus.** Econometric theory, structural estimation, formal theory. Less sympathetic to reduced-form papers without methodological contribution. Mathematical rigor expected.

**Bar.** A methodological or theoretical advance must be visible. Applied papers clear the bar only if they bring a new estimator or a novel identification argument.

**Domain-referee adjustments.**
- Contribution 30 → 35 (methodological contribution weight)
- Fit 10 → 5 (ECMA tolerates narrower settings if the method generalizes)

**Methods-referee adjustments.**
- If paper type is `structural`: Model spec 20 → 30, Parameter ID 30 → 35, Counterfactuals 15 → 15
- If paper type is `reduced-form`: Identification 35 → 40, expect proofs / formal arguments
- Replication 5 → 10 (code + proofs must match)

**Typical concerns.**
- "What's the methodological contribution?"
- "Are the identifying assumptions stated formally, not just verbally?"
- "Are the asymptotic properties of the estimator established?"
- "Would an econometrician who reads only the abstract know what's new here?"

**Referee-pool weights.**
- STRUCTURAL: 0.30
- THEORY: 0.25
- MEASUREMENT: 0.20
- CREDIBILITY: 0.15
- POLICY: 0.05
- SKEPTIC: 0.05

**Table format override.** None specific; mathematical notation must be consistent throughout.

---

### Review of Economic Studies (ReStud)

**Short name:** `ReStud`

**Focus.** Conceptually ambitious work across theory, empirical, and macro. European-flavored taste: willing to publish unfashionable topics if the idea is strong. Values careful reasoning over technical fireworks.

**Bar.** A clear "intellectual arc" — the paper should leave the reader understanding something new about how the world works, not just a new estimate.

**Domain-referee adjustments.**
- Contribution 30 → 35
- Substance 20 → 25

**Methods-referee adjustments.**
- Identification 35 → 35 (unchanged; care but not QJE-level obsession)
- Honesty (for theory+empirics) 15 → 20

**Typical concerns.**
- "What do we understand about the world that we didn't before?"
- "Is the argument careful, or is it a victory lap?"
- "Are the limitations honestly stated, or buried?"
- "Does the conclusion generalize beyond this specific setting, and if so, how?"

**Referee-pool weights.**
- STRUCTURAL: 0.20
- CREDIBILITY: 0.20
- THEORY: 0.20
- POLICY: 0.15
- MEASUREMENT: 0.15
- SKEPTIC: 0.10

**Table format override.** None specific.

---

## Political Science (Top-3)

Three flagship general-interest political-science journals. The `paper_type` taxonomy here typically resolves to `reduced-form`, `formal-theory`, or `survey-experiment` (added in v1.8.0 to support these journals). Other types still apply when relevant.

### American Political Science Review (APSR)

**Short name:** `APSR`

**Focus.** Highest-bar general-interest political-science journal; APSA's flagship. Publishes across IR, comparative politics, American politics, formal theory, and political theory. Strongest preference for theoretically motivated work that speaks to multiple subfields.

**Bar.** "Top-3 in your subfield should know this." A clear theoretical contribution is load-bearing — purely descriptive or purely empirical papers without a theoretical home rarely clear desk.

**Domain-referee adjustments.**
- Contribution 30 → 35 (theoretical-importance bar is high)
- Lit positioning 25 → 25 (unchanged)
- Fit 10 → 5 (APSR publishes broadly across subfields; fit is rarely a binding constraint)

**Methods-referee adjustments.**
- Identification 35 → 30 (still cared about, but APSR rewards theoretical novelty even when identification is observational)
- For `formal-theory` papers: Comparative-static sharpness 25 → 30 (the theoretical contribution must produce sharp predictions)
- For `survey-experiment` papers: Sampling-frame validity is a desk-level concern; convenience samples (uncalibrated MTurk) face an uphill battle.

**Typical concerns.**
- "Where is the theoretical contribution? What would a theorist in a different subfield take from this?"
- "Is the design appropriate to the population the paper claims to speak about?"
- "Does the paper engage seriously with formal theory, or only with reduced-form empirics?"
- "Is the conclusion testable, or vacuous?"

**Referee-pool weights.**
- THEORY: 0.30
- CREDIBILITY: 0.20
- STRUCTURAL: 0.15
- MEASUREMENT: 0.15
- POLICY: 0.10
- SKEPTIC: 0.10

**Table format override.** Footnotes and citations follow APSA Style Manual; tables typically use significance stars (* p<0.05, ** p<0.01, *** p<0.001 — note 0.05 floor differs from AEA convention).

### American Journal of Political Science (AJPS)

**Short name:** `AJPS`

**Focus.** General political-science journal with strong methods orientation. AJPS is the methodologists' favourite among the top-3 — receptive to causal-inference, survey experiments, formal-empirical work, and methodological innovation alongside substantive contribution.

**Bar.** "The method is at least as interesting as the substance." Not a methods-only journal, but methodologically novel papers compete favourably with merely-clean empirical work. AJPS Replication Policy (since 2015) is enforced — replication archive is mandatory at acceptance.

**Domain-referee adjustments.**
- Contribution 30 → 30 (unchanged)
- Lit positioning 25 → 25 (unchanged)
- External validity 15 → 20 (AJPS expects engagement with whether the result generalises beyond the specific setting)

**Methods-referee adjustments.**
- Identification 35 → 40 (the credibility bar is real)
- Inference 20 → 20 (unchanged)
- For `survey-experiment` papers: Manipulation checks and balance tables are mandatory in the manuscript; absence is a desk-level concern.
- Replication 5 → 10 (AJPS replication policy)

**Typical concerns.**
- "Is identification credible to a methodologist who has read the recent econometrics literature?"
- "Is the design pre-registered? If not, why not?"
- "Are the standard errors clustered at the right level, with the right type of clustering for the design?"
- "Is the replication archive complete (data, code, README)?"
- "Does the method scale to other contexts the paper gestures at?"

**Referee-pool weights.**
- CREDIBILITY: 0.30
- MEASUREMENT: 0.20
- STRUCTURAL: 0.15
- THEORY: 0.15
- SKEPTIC: 0.10
- POLICY: 0.10

**Table format override.** APSA Style; significance stars allowed (0.05/0.01/0.001 floor); regression tables typically include observations, R², and SE-clustering specification.

### Journal of Politics (JOP)

**Short name:** `JOP`

**Focus.** Top-3 political-science journal alongside APSR and AJPS, with a slight tilt toward American politics and comparative politics. Publishes across all subfields; receptive to shorter, sharper papers ("research notes" track) alongside full articles.

**Bar.** "A clear contribution to a substantive question that political scientists care about." Lower theoretical-novelty bar than APSR; lower methods-novelty bar than AJPS — but a higher *clarity-of-contribution* bar than either. The desk asks: "what specifically does this paper teach me?"

**Domain-referee adjustments.**
- Contribution 30 → 35 (clarity of contribution is the binding constraint)
- Substance 20 → 25 (JOP rewards a tight argument over a broad one)
- Fit 10 → 5 (JOP publishes broadly)

**Methods-referee adjustments.**
- Identification 35 → 35 (unchanged)
- Robustness 15 → 20 (JOP referees frequently push back on robustness)

**Typical concerns.**
- "What specifically does this paper add that we didn't already know?"
- "Is the argument tight, or is it three loosely-related claims?"
- "Are the robustness checks responsive to obvious threats, or are they ritual?"
- "Could this be a research note (8,000 words) instead of a full article?"

**Referee-pool weights.**
- SKEPTIC: 0.25
- CREDIBILITY: 0.20
- THEORY: 0.15
- MEASUREMENT: 0.15
- STRUCTURAL: 0.15
- POLICY: 0.10

**Table format override.** APSA Style; standard significance stars allowed.

---

## Agricultural and Development Economics

Profiles for journals likely to receive papers on ag insurance, smallholder modernization, rural labor, food/farm policy, and Chinese development microeconomics. The `paper_type` taxonomy here typically resolves to `reduced-form` (DiD, IV, matching on policy rollouts) or `descriptive` (sample documentation, treatment-effect heterogeneity).

### American Journal of Agricultural Economics (AJAE)

**Short name:** `AJAE`

**Focus.** AAEA flagship; the top general-interest ag-econ journal. Publishes empirical and theoretical work on ag/food markets, farm and food policy, environmental and resource economics with an ag connection, ag-development, and rural microeconomics. Receptive to Chinese microdata when the contribution generalizes beyond the specific setting.

**Bar.** Credible identification + substantive contribution to ag-econ. The methodological bar is close to top-field-econ for empirical work; the substantive bar requires the paper to teach something an ag-economist who doesn't work on this topic would want to know. AJAE Replication Policy is enforced (since 2018) — replication archive mandatory at acceptance.

**Domain-referee adjustments.**
- Contribution 30 → 30 (unchanged)
- Substance 20 → 25 (must speak to ag-econ literature, not just to a Chinese-data audience)
- External validity 15 → 20 (does the China result tell us something about smallholder behavior more generally?)

**Methods-referee adjustments.**
- Identification 35 → 40 (top-field-style identification expected)
- Replication 5 → 10 (AJAE Replication Policy)

**Typical concerns.**
- "Does the paper engage the global ag-insurance / smallholder modernization literature, or only the China-specific literature?"
- "Is the policy variation plausibly exogenous, or are county-level rollouts confounded with unobserved trends?"
- "Are the parallel-trends / first-stage diagnostics persuasive?"
- "Are mechanism channels distinguished (capital adoption vs. service use vs. management modernization), or bundled?"
- "Is the replication archive complete and runs out of the box?"

**Referee-pool weights.**
- CREDIBILITY: 0.30
- POLICY: 0.20
- MEASUREMENT: 0.20
- STRUCTURAL: 0.10
- SKEPTIC: 0.15
- THEORY: 0.05

**Table format override.** Significance stars allowed (0.10/0.05/0.01); SE in parentheses; clustering specification stated in notes.

---

### China Economic Review (CER)

**Short name:** `CER`

**Focus.** General-interest economics journal focused on the Chinese economy. Publishes across all subfields when the substantive contribution is China-specific. Receptive to careful empirical work using Chinese microdata, administrative data, or natural experiments unique to China's policy environment.

**Bar.** A clear China contribution. The reviewer asks "what does this paper teach us about the Chinese economy that we didn't already know?" — not "what does this paper teach us about economics in general." Methodological rigor expected but the methods novelty bar is lower than top-field-econ.

**Domain-referee adjustments.**
- Contribution 30 → 30 (unchanged)
- Lit positioning 25 → 25 (must engage both the Chinese-economy literature and the relevant international literature)
- External validity 15 → 10 (China-specific contributions are accepted; generalizability is not the binding constraint)

**Methods-referee adjustments.**
- Identification 35 → 35 (unchanged)
- Data validation 20 → 25 (Chinese microdata quality is a recurring concern: sampling, attrition, administrative classification)

**Typical concerns.**
- "What is the China-specific contribution? Could the paper be written about any country?"
- "Are the data sources appropriate for the question? (Sample frame, coverage, attrition.)"
- "Is the policy timeline accurately characterized? (e.g., national policy vs. county-level rollout.)"
- "Does the paper engage the Chinese-language literature where it is the natural reference?"

**Referee-pool weights.**
- CREDIBILITY: 0.25
- MEASUREMENT: 0.25
- POLICY: 0.20
- SKEPTIC: 0.15
- STRUCTURAL: 0.10
- THEORY: 0.05

**Table format override.** Standard; significance stars allowed.

---

### Food Policy (FP)

**Short name:** `FoodPolicy`

**Focus.** Policy-oriented food, ag, and nutrition research. Broader policy reach than AJAE; narrower disciplinary core. Receptive to empirical economics, but values policy translation as much as econometric novelty. Multidisciplinary readership (economists, nutritionists, ag scientists, policy analysts).

**Bar.** "What does this mean for policy?" must be answerable in one paragraph. Pure econometric exercises without policy relevance face desk-reject pressure.

**Domain-referee adjustments.**
- Contribution 30 → 30 (unchanged)
- Substance 20 → 30 (policy-translation weight)
- External validity 15 → 20 (does this lesson travel to other low/middle-income contexts?)

**Methods-referee adjustments.**
- Identification 35 → 30 (cared about, but not QJE-level)
- Robustness 15 → 15 (unchanged)

**Typical concerns.**
- "What is the policy lesson, in plain language?"
- "Does the paper translate the empirical result for a policy audience, or assume econometric vocabulary?"
- "Is the policy proposal grounded in the empirical estimate, or aspirational?"
- "Does the paper engage the FAO / IFPRI / national-policy literature?"

**Referee-pool weights.**
- POLICY: 0.40
- CREDIBILITY: 0.20
- MEASUREMENT: 0.15
- SKEPTIC: 0.15
- STRUCTURAL: 0.05
- THEORY: 0.05

**Table format override.** Standard; significance stars allowed.

---

### World Development (WD)

**Short name:** `WD`

**Focus.** Flagship multidisciplinary development journal. Publishes across economics, political science, sociology, geography, anthropology when the contribution is to development understanding. Heavy weight on Global South contexts; mixed methods welcome.

**Bar.** Substantive contribution to development knowledge. Methodological rigor expected but methods-only papers do not clear desk; the development-substance must be load-bearing.

**Domain-referee adjustments.**
- Contribution 30 → 30 (unchanged)
- Substance 20 → 25 (development-knowledge contribution)
- External validity 15 → 20 (lessons must travel beyond the specific country setting)

**Methods-referee adjustments.**
- Identification 35 → 30 (cared about, but design-based identification not always available in development settings; well-argued observational work accepted)
- Inference 20 → 20 (unchanged)

**Typical concerns.**
- "What does this paper contribute to our understanding of development, broadly?"
- "Is the policy / institutional context explained well enough for a non-China reader?"
- "Are the limitations of the data and design honestly stated?"
- "Does the paper engage the comparative-development literature, or only the China-specific literature?"

**Referee-pool weights.**
- POLICY: 0.30
- CREDIBILITY: 0.20
- MEASUREMENT: 0.15
- SKEPTIC: 0.15
- STRUCTURAL: 0.10
- THEORY: 0.10

**Table format override.** Standard; significance stars allowed.

---

### China Agricultural Economic Review (CAER)

**Short name:** `CAER`

**Focus.** China-focused ag-econ journal published by Emerald in English; sister venue to the Chinese-language *中国农村经济*. Strong readership inside China + East Asia, growing international readership. Receptive to ag-policy evaluation, rural household behavior, ag-tech adoption, food security, and ag-institutional analysis with Chinese microdata.

**Bar.** Substantive China-ag contribution. Methodological bar is below AJAE / CER but above pure descriptive work. Welcomes detailed institutional and policy context that an international journal might compress.

**Domain-referee adjustments.**
- Contribution 30 → 25 (lower bar than AJAE)
- Substance 20 → 30 (China-ag substance is the main attractor)
- Fit 10 → 10 (unchanged)

**Methods-referee adjustments.**
- Identification 35 → 30 (still cared about; observational work with thoughtful sensitivity analysis accepted)
- Data validation 20 → 25 (Chinese microdata sources matter to readers)

**Typical concerns.**
- "Does the paper accurately characterize the Chinese ag-policy environment, including provincial / county heterogeneity?"
- "Is the sample representative for the population the paper claims to speak about?"
- "Does the paper engage the Chinese-language literature?"
- "Is the policy proposal compatible with the actual administrative setup?"

**Referee-pool weights.**
- POLICY: 0.30
- MEASUREMENT: 0.25
- CREDIBILITY: 0.20
- SKEPTIC: 0.10
- STRUCTURAL: 0.10
- THEORY: 0.05

**Table format override.** Standard; significance stars allowed; bilingual table titles welcomed for key tables.

---

### Applied Economic Perspectives and Policy (AEPP)

**Short name:** `AEPP`

**Focus.** AAEA's policy/perspectives journal, sister to AJAE. Publishes shorter, policy-translation-heavy applied work and synthesis pieces. The "perspectives" framing matters: papers should help non-specialists understand a policy issue, not only contribute marginal econometric estimates.

**Bar.** Clear policy contribution + crisp writing. Methodological novelty is not required; clarity-of-policy-translation is the binding constraint. Targeted at extension agents, USDA staff, ag-policy practitioners, and ag-economists who want a synthesis.

**Domain-referee adjustments.**
- Contribution 30 → 25 (lower bar than AJAE)
- Substance 20 → 35 (policy-translation weight is dominant)
- External validity 15 → 20 (lesson should travel)

**Methods-referee adjustments.**
- Identification 35 → 25 (cared about, but not central; well-executed reduced-form OK)
- Robustness 15 → 10 (less obsessed than AJAE)

**Typical concerns.**
- "What is the practical takeaway? Could a USDA / MoARA staffer act on it?"
- "Is the writing accessible to a non-econometrician?"
- "Are the policy implications grounded in the estimate, not extrapolated?"
- "Does the paper synthesize the existing evidence, or just report a new estimate in isolation?"

**Referee-pool weights.**
- POLICY: 0.45
- CREDIBILITY: 0.15
- MEASUREMENT: 0.15
- SKEPTIC: 0.15
- STRUCTURAL: 0.05
- THEORY: 0.05

**Table format override.** Significance stars allowed; AEPP encourages plain-language summary boxes alongside regression tables.

---

### Journal of Development Studies (JDS)

**Short name:** `JDS`

**Focus.** UK-based multidisciplinary development journal. Publishes economics, political science, sociology, anthropology when the contribution is to development knowledge. Slightly more receptive to qualitative + mixed-methods than World Development; receptive to longer historical / institutional context.

**Bar.** Substantive contribution to development understanding + careful argumentation. Methodological rigor expected for empirical papers but methods novelty is not central.

**Domain-referee adjustments.**
- Contribution 30 → 30 (unchanged)
- Substance 20 → 25 (development-substance weight)
- External validity 15 → 20 (lessons should travel across LMICs)

**Methods-referee adjustments.**
- Identification 35 → 30 (cared about; observational work with thoughtful framing accepted)
- Robustness 15 → 15 (unchanged)

**Typical concerns.**
- "What does this paper contribute to development studies, broadly conceived?"
- "Is the historical / institutional context explained?"
- "Are the limitations of the data and design honestly stated?"
- "Does the paper engage the development-studies literature, including non-economics work where relevant?"

**Referee-pool weights.**
- POLICY: 0.25
- CREDIBILITY: 0.20
- THEORY: 0.15
- MEASUREMENT: 0.15
- SKEPTIC: 0.15
- STRUCTURAL: 0.10

**Table format override.** Standard; significance stars allowed.

---

### Agricultural Economics (AgEcon)

**Short name:** `AgEcon`

**Focus.** International Association of Agricultural Economists (IAAE) flagship. More international and comparative than AJAE; receptive to ag-econ work from any country, with appetite for cross-country / global comparisons. Publishes farm and food policy, ag-development, ag-trade, environmental ag-econ, and rural microeconomics.

**Bar.** Substantive ag-econ contribution with international relevance. Methodological bar similar to AJAE for empirical work. Country-specific work clears when the lesson plausibly generalizes or when the country represents an under-studied setting.

**Domain-referee adjustments.**
- Contribution 30 → 30 (unchanged)
- External validity 15 → 25 (international / comparative weight is high)
- Fit 10 → 10 (unchanged)

**Methods-referee adjustments.**
- Identification 35 → 35 (unchanged)
- Replication 5 → 10 (Wiley + IAAE replication push)

**Typical concerns.**
- "Does the paper situate the China result in a broader international context?"
- "Are the identification assumptions plausible given the policy rollout?"
- "Are the magnitudes interpretable in international terms (e.g., normalized to ag GDP, household income)?"
- "Is the replication archive complete?"

**Referee-pool weights.**
- CREDIBILITY: 0.30
- POLICY: 0.20
- MEASUREMENT: 0.20
- SKEPTIC: 0.15
- STRUCTURAL: 0.10
- THEORY: 0.05

**Table format override.** Standard; significance stars allowed.

---

## Field adaptation

The five profiles above are econ-specific. The **pipeline is field-agnostic** — nothing in `editor.md`, `domain-referee.md`, or `methods-referee.md` hard-codes economics. What varies by field is the journal profile.

**To adapt for a different field:**

1. Copy `templates/journal-profile-template.md` into a new section below (use `### Journal Name (SHORT)`).
2. Fill each schema field:
   - **Focus** — what the journal publishes (look at the last 6 months of TOC).
   - **Bar** — acceptance rate + one sentence on what the editor is looking for.
   - **Domain-referee adjustments** — re-weight contribution / lit-positioning / substance / external validity / fit for this journal's taste.
   - **Methods-referee adjustments** — for non-econ fields, you will want to rename the paper types in `methods-referee.md` (see the next section).
   - **Typical concerns** — read 2–3 recent reviews (published alongside papers at Nature Communications, eLife, etc., or solicit from a colleague) and distill 3–5 recurring referee questions.
   - **Referee-pool weights** — the 6 dispositions are general enough to apply to any field. Re-weight based on what that journal's referees actually ask about. Weights must sum to 1.0.
   - **Table format** — any field-specific conventions (e.g., APA tables for psychology, Chicago-style footnotes for history, Vancouver citations for medicine).

**For non-econ paper types.** The `methods-referee.md` paper-type branching uses `reduced-form / structural / theory+empirics / descriptive`. If your field uses different categories (e.g., biology: `observational / experimental / computational / review`; political science: `case-study / comparative / formal-model / survey`), edit `methods-referee.md` to add your field's paper types and their dimension weights. Keep the `reduced-form` / etc. branches for econ users.

**Examples for fields we don't yet ship** (to be filled in by adopters — we ship econ + political-science as concrete profiles; psych / sociology / public health are template-only):

- `### Nature Human Behaviour (NHB)` — flagship interdisciplinary. Bar: broad impact + pre-registration + replication. Referee weights: MEASUREMENT high, CREDIBILITY high.
- `### Psychological Science` — flagship psych. Bar: open-science compliance + theoretical contribution. Referee weights: CREDIBILITY high, MEASUREMENT high. Preregistration expected.
- `### American Journal of Sociology (AJS)` — top sociology. Bar: theoretical contribution + careful argument. Referee weights: THEORY medium, SKEPTIC medium, MEASUREMENT medium.
- `### PNAS` — multi-disciplinary. Bar: generalizability + public interest. Referee weights: POLICY high, SKEPTIC high.

---

## Cross-references

- `.claude/agents/editor.md` — reads this file.
- `.claude/agents/domain-referee.md` — applies domain-referee adjustments.
- `.claude/agents/methods-referee.md` — applies methods-referee adjustments.
- `.claude/skills/review-paper/SKILL.md` — `--peer [journal]` mode entry point.
- `templates/journal-profile-template.md` — skeleton for adding your own.
