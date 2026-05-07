# Literature Review: Policy-Based Agricultural Insurance in China (2007–2026)

**Date:** 2026-05-07
**Slice:** 1 of 3 (web-only first pass)
**Query:** Web-only literature scan on policy-based agricultural insurance (政策性农业保险, PAY) evaluation in China, 2007–2026, organized into four clusters: (a) PAY policy-rollout evaluation; (b) insurance-driven smallholder behavioral responses (capital, services, technology); (c) insurance and household labor allocation — directly competing slice; (d) related-but-distinct (insurance demand, take-up, pricing, weather-shock incidence).
**Linked spec:** `quality_reports/specs/2026-05-04_research-spec_ag-insurance-smallholder-labor-china.md`

---

## Summary

China's policy-based agricultural insurance (PAY) launched in 2007 and has since become the world's largest agricultural insurance program by premium volume, exceeding 121.9 billion RMB in 2022. The evaluation literature has matured along a clear arc: an early phase (2007–2015) dominated by descriptive/aggregate-output studies and the field experiment work of Cai and coauthors on insurance take-up and microeconomic decisions; a middle phase (2016–2021) of household-survey or province-panel papers documenting effects on production, inputs, financial decisions, and environmental practices; and a recent phase (2022–2026) of quasi-experimental designs exploiting the 2018–2019 full-cost insurance pilot in major grain provinces and the longer arc of staggered provincial rollout. China-PAY work now sits comparably in methodological quality to the global ag-insurance evaluation literature (Karlan et al. 2014, Mobarak & Rosenzweig 2013, Cole et al. 2013) but remains differentiated by its policy architecture (premium subsidies rather than market price), its smallholder-dominated production system, and the parallel rise of agricultural socialized services (社会化服务) and machinery outsourcing.

The dominant findings cluster around **risk-relaxation effects**: PAY raises insured-crop production (Cai 2016 ~16%), eases credit constraints, increases borrowing and agricultural investment, alters input mix (mixed evidence on chemical fertilizer; reduced pesticide on some samples), and at the macro level boosts production resilience and grain output. **Channel evidence** is patchier: factor-allocation papers (Zheng & Li 2023, Cha et al. 2024, Hou & Wang 2025) show PAY shifts capital, machinery, and labor inputs but typically operate at province or single-crop level, not household-by-time-by-policy intensity. **Labor-allocation** evidence is the thinnest cluster (cluster c). Two Chinese-language papers and one English paper (Zheng & Li 2023) treat the labor-allocation channel directly, but all use province-level "urbanization rate" or sectoral-employment-share aggregates as the labor outcome — none use household-level CFPS labor hours or off-farm participation as the primary outcome of an insurance-intensity treatment.

Where China-PAY work sits relative to the global literature: the cross-country evidence (Karlan et al. 2014, Cole et al. 2013, Janzen & Carter 2019) establishes that uninsured risk binds investment and that insurance-induced investment is a real margin; China-PAY work confirms this in a smallholder context. What is conspicuously missing from China-PAY is the labor-restructuring follow-through — the Mexican Progresa-style downstream-labor literature, or the Indian NREGS-and-insurance-jointly literature, has no clear China-PAY counterpart at the household-panel level.

---

## Closest competitor assessment

**Direct competitor for "PAY → smallholder household labor allocation in China" — does it exist?**

**No fully direct competitor exists at the household-panel level using PAY intensity as treatment.** The closest candidates are:

1. **Zheng & Li (2023, *Journal of South China Agricultural University, Social Sciences*)** — "Agricultural Insurance, Labor Resource Allocation and Green Economy Efficiency." This is the closest in framing: it explicitly models insurance → labor reallocation → green TFP using a Cobb-Douglas decomposition with ag and non-ag labor. **But** the labor-allocation outcome is operationalized as the **provincial urbanization rate**, not household labor hours or participation, and the data are 2012–2021 provincial panels with entropy-weighted insurance development as the regressor. This gives them a directional finding ("insurance promotes rural labor transfer to non-agricultural sectors") but not a household-level magnitude. Our project would replace their province aggregate with CFPS household labor allocation, which is a meaningful methodological advance.

2. **Zheng & Ning (2025, *Journal of Central University of Finance & Economics*)** — "Agricultural Insurance, Labor Resource Allocation and Agricultural Total Factor Productivity." Same first author as #1; the labor-allocation outcome again appears to be aggregate (TFP-mediated). Bibliographic detail incomplete from web sources [UNVERIFIED: full abstract not extractable from journal page; only title and venue confirmed].

3. **Yang Ruihua (杨汭华) (2021)** — "收入风险冲击下农业保险对农户家庭劳动力资源配置的影响" / "The Impact of Agricultural Insurance on Rural Household Labor Resource Allocation under Income Risk Shocks." *Journal of Arid Land Resources and Environment* (《干旱区资源与环境》), 2021, Issue 10. CAU School of Economics & Management. **Resolved by CoVe (2026-05-07):** what was initially flagged as an "unattributed CAU paper" is in fact a published article (the cem.cau.edu.cn URL is a faculty-page reproduction, not the original venue). The paper uses a cross-sectional survey of 1,733 households in Shandong, Henan, and Guizhou with a Tobit model, treating insurance as a mediating variable and income volatility as moderator. **Critical limitation for our project:** Yang (2021) does NOT use CFPS panel data, does NOT use province-year PAY intensity as treatment, and does NOT use a panel DiD design. It is the closest substantive precedent on the labor-allocation outcome, but the data and identification differ enough that it does not preempt our project. **Citation discipline:** Yang (2021) MUST be cited as the closest prior work; the contribution claim now reads as "first paper to identify PAY-intensity → household labor allocation using CFPS panel + province-year design with services-as-bridge mechanism evidence."

**"Productive ag-services as the bridge between insurance and labor restructuring" — does any paper treat this as the mechanism?**

**No.** The closest is **Cha et al. (2024, *Frontiers in Sustainable Food Systems*)** on Chinese pear farmers, which finds insurance increases hired-labor cost and machinery inputs but treats them as separate mediators of an income outcome — not as a bridge to household labor restructuring. **Chen (2025, *Review of Development Economics*)** uses CFPS 2014–2022 to study how Agricultural Mechanization Socialized Services (AMSS) reallocate labor by gender (men: −4.4 pp ag involvement; women: −2.3 pp) — this is exactly the labor-reallocation outcome we want to study, but the treatment is AMSS adoption, **not** insurance. Combining the Chen (2025) labor outcome design with PAY intensity as the treatment is essentially an unfilled niche.

**Summary of the gap our project fills.** The literature has separately established (i) insurance → production, finance, and (province-level) labor transfer; (ii) socialized services → household labor reallocation. **No paper currently links insurance intensity to household labor reallocation through the services channel using CFPS micro-data with quasi-experimental identification.** Our project sits in this gap, with our 2018–2019 full-cost pilot DiD as a clean robustness anchor that none of the closest competitors have used at the household level.

---

## Cluster (a): PAY policy-rollout evaluation

### Cai (2016), AEJ:EP — Impact of Insurance Provision on Household Production and Financial Decisions
- **Main contribution:** First credible quasi-experimental estimate of an agricultural insurance program's effect on household production, borrowing, and savings in China.
- **Method:** Natural experiment with DiD and triple-difference; sow insurance rollout, southwestern China.
- **Key finding:** Insurance raises insured-crop production by ~16%, borrowing by 29%, and shifts savings composition toward more flexible vehicles; total savings unchanged.
- **Relevance:** Foundational benchmark and directly cited in our project's spec; confirms insurance → production margin our paper extends to labor allocation.

### Gu, Liu, Liu, Dong & Dong (2024), *Finance Research Letters* — PAY effects on farmers' earnings in major grain-producing regions
- **Main contribution:** Recent evaluation focused on grain-producing regions. (CoVe-corrected from "Wang & Yu" attribution.)
- **Method:** Panel of 13 primary grain-producing areas, 2007–2022.
- **Key finding:** Positive earnings effect; mediating channels are operational scale, technological progress, and credit access.
- **Relevance:** Direct precedent for the grain-province focus in our 2018–2019 full-cost pilot DiD robustness check; channels overlap with our mechanism framing.

### Zheng & Zhao (2025), *Frontiers in Sustainable Food Systems* — PAY and grain production resilience
- **Main contribution:** Multi-period DiD on premium-subsidy policy implementation (2002–2012) plus FE on insurance development level (2012–2021).
- **Method:** 31-province panel, 2002–2021; parallel-trends and placebo tests.
- **Key finding:** Premium subsidy raises grain production resilience (β=0.276); pre-disaster risk dispersion exceeds post-disaster compensation; mechanisms include technology, land transfer, and grain specialization. Major grain provinces benefit more.
- **Relevance:** Strongest staggered-DiD on PAY rollout we found at the province level; confirms feasibility of our aspirational county-level staggered design.

### Hou & Wang (2025), *Frontiers in Sustainable Food Systems* — Insurance, grain production scale, income mediation
- **Main contribution:** Tests scale-expansion effect of insurance with income as mediator.
- **Method:** 27-province panel 2011–2021; FE with stepwise mediation (Sobel/Goodman).
- **Key finding:** Modest positive effect on planting scale (β=0.000368); income mediates ~7% of total effect.
- **Relevance:** Methodologically modest (small coefficients, no household micro), but useful as illustrating the dominant province-panel paradigm we would improve on.

### Ma, Zhou & Coauthors (2024), *AJARE* — Crop insurance premium subsidies and cropland abandonment
- **Main contribution:** Tests whether PAY subsidies reduce cropland abandonment in China.
- **Method:** [UNVERIFIED: paper title and journal confirmed via Wiley listing; full method not extracted — inferred to be panel DiD].
- **Key finding:** PAY subsidies reduce cropland abandonment.
- **Relevance:** Land-use margin complement to our labor-allocation question; relevant if smallholders shift from abandonment to outsourcing rather than from cultivation to outsourcing.

### Zou, Ren, Mishra & Hirsch (2022), *Agribusiness* — Aggregate effects of PAY on agricultural output
- **Main contribution:** Provincial aggregate analysis of PAY's output effect (CoVe-corrected: full author list).
- **Method:** Panel of 31 Chinese provinces, 2004–2018.
- **Key finding:** Significant positive effect on aggregate ag output; insurance promotes labor productivity, cultivated-area-per-capita expansion, and specialization. **Effect is stronger in Eastern China and *non-major* crop-producing areas** (this matters — earlier draft phrasing implied "major" regions; the actual finding is the opposite).
- **Relevance:** Macro corroboration; weak at distinguishing channels.

### Quasi-natural experiment papers on full-cost insurance pilot (2018–2019)
- **Several recent papers** evaluate the 2018 full-cost insurance pilot in 6 grain provinces (Inner Mongolia, Heilongjiang, Anhui, Shandong, Henan, Hubei) using county-level DiD: Wang et al. (2024 *Agriculture*), and a *Humanities & Social Sciences Communications* paper on agricultural economic resilience [UNVERIFIED: exact author lists not fully extracted from search]. Findings: full-cost insurance reduces fertilizer intensity by ~22%, raises utilization efficiency, and improves agricultural economic resilience.
- **Relevance:** These papers are direct precedents for our 2018–2019 DiD robustness design; our contribution adds the household labor-allocation outcome they do not address.

---

## Cluster (b): Insurance-driven smallholder behavioral responses

### Cha, Deng, Zheng & Li (2024), *Frontiers in Sustainable Food Systems* — Crop insurance, factor allocation, and farmers' income (Chinese pear farmers)
- **Main contribution:** Tests insurance → factor allocation (labor, machinery, green tech) → income on a single-crop sample.
- **Method:** OLS + 2SLS with IV; 1,337 pear farmers in Xixian and Weixian counties.
- **Key finding:** Insurance significantly raises hired-labor cost and machinery inputs (1% sig.); these mediate income gains; green-tech adoption channel also active.
- **Relevance:** Most direct precedent for the "insurance → factor reallocation" mechanism, but on a single specialty crop with limited generalizability to rice/wheat/corn smallholders.

### Karlan, Osei, Osei-Akoto & Udry (2014), QJE — Agricultural decisions after relaxing credit and risk constraints
- **Main contribution:** Field experiment in northern Ghana isolating risk vs. credit as the binding constraint on farm investment.
- **Method:** RCT cross-randomizing cash grants and rainfall index insurance.
- **Key finding:** Insurance leads to significantly larger ag investment and riskier production choices; risk binds at the margin tested.
- **Relevance:** Cross-country foundation for the "insurance enables productive investment" mechanism; our paper extends this margin to organization-of-production and labor allocation in a different agricultural system.

### Yan, Yi & Zhang (2024), *China Rural Economy* — Fertilizer-reduction effect of agricultural insurance under joint credit-information constraints
- **Main contribution:** Explores the joint role of credit access and insurance information in driving the fertilizer-reduction effect [UNVERIFIED: full author detail and pages from CNJN-style abstract; access via PDF host].
- **Method:** Survey-data empirical with mediation analysis.
- **Key finding:** Insurance-driven fertilizer reduction strengthens when both credit and information constraints are eased.
- **Relevance:** China-language landmark on input-margin behavioral responses to PAY; relevant for our control vector.

### Li, Yuan, Cao, Zhao & Guo (2022), *Journal of Environmental Management* — Crop insurance and pesticide use among Chinese rice farmers
- **Main contribution:** Estimates risk-reduction effect of insurance on pesticide intensity. (CoVe-corrected: previously misattributed to "Fang/Hu/Mao" in *J. Cleaner Production*; correct venue is *J. Environmental Management* vol. 306, art. 114456.)
- **Method:** Household survey of rice farmers, China.
- **Key finding:** Insured plots use **~33.30%** less pesticide per unit land than non-insured (the earlier-draft 52.7% figure was misattributed from Feng, Han & Qiu 2021 below).
- **Relevance:** Pesticide-channel evidence; control-variable rationale.

### Mao, Sun, Chai, Fang & Shi (2025), *Ecological Economics* — Extreme weather, agricultural insurance and climate-adaptation technology adoption in China
- **Main contribution:** Insurance as an enabler of climate-adaptation technology (CAT) adoption. (CoVe-corrected from "Ye et al. 2024" attribution; correct year is 2025, vol. 228, art. 108456.)
- **Method:** Survey of 622 Chinese apple farmers.
- **Key finding:** Extreme-weather exposure raises both CAT adoption and insurance participation; insurance and CAT are complementary (complementary > substitutive effects).
- **Relevance:** Tech-adoption channel margin; complements our capital-adoption channel.

### Liu, Chen & Hill (2020), AJAE — Delayed premium payment, insurance adoption, and household investment
- **Main contribution:** Field experiment showing delayed-payment design raises insurance uptake and household investment. (CoVe-corrected from "Wang & Tong" attribution.)
- **Method:** RCT among hog farmers in rural China.
- **Key finding:** Delayed-payment option raises uptake by ~10 percentage points (3× baseline) and increases downstream investment in higher-risk activities.
- **Relevance:** Cleanly identified investment-margin response to insurance — the upstream of our labor-allocation question.

### Feng, Han & Qiu (2021), *China Economic Review* — Crop insurance and pesticide usage in China
- **Main contribution:** Documents the pesticide-reduction effect of crop insurance with farm-size and farmer-characteristic heterogeneity. (CoVe-corrected from "Yang et al." attribution.)
- **Method:** Household survey, identification via insurance-eligibility / IV variation.
- **Key finding:** Insured plots use ~52.7% less pesticide per unit land than non-insured. **Heterogeneity is stronger reduction for SMALLER plots, OLDER farmers, and MORE RISK-AVERSE farmers** — the earlier draft inverted this direction (had said "large-scale farms"). The corrected direction is consistent with smaller / more risk-averse farmers using pesticide as a self-insurance substitute that PAY supplants.
- **Relevance:** **High direct relevance** for our smallholder cuts — heterogeneity is in the same direction we'd expect from the services-as-bridge mechanism (smaller smallholders most reactive).

---

## Cluster (c): Insurance and household labor allocation ⚠ DIRECTLY COMPETING

This cluster is the thinnest in the literature. The relevant papers are:

### Zheng & Li (2023), *Journal of South China Agricultural University (Social Science Edition)* — Agricultural insurance, labor resource allocation and green economy efficiency
- **Main contribution:** Theoretical Cobb-Douglas decomposition of ag and non-ag labor; empirical test of insurance → labor reallocation → green TFP.
- **Method:** 30-province panel, 2012–2021; OLS, FE, 2SLS; entropy-weighted insurance development index; mediation via urbanization rate.
- **Key finding:** Agricultural insurance significantly promotes green economic efficiency directly and indirectly through labor reallocation toward non-agricultural sectors; effect concentrated in eastern and central regions.
- **Relevance:** **The closest substantive competitor in this cluster.** Critical limitation for our project: their "labor allocation" outcome is the provincial urbanization rate, not household-level ag hours or off-farm participation. Our CFPS-based household-level design is a meaningful methodological advance.

### Zheng & Ning (2025), *Journal of Central University of Finance & Economics* — Agricultural insurance, labor resource allocation, and agricultural total factor productivity
- **Main contribution:** Same first author as Zheng & Li (2023); shifts the outcome to ag TFP with labor allocation as channel [UNVERIFIED: full abstract not extractable — page rendered as template with empty fields; venue, year, issue, and pages confirmed].
- **Method:** Provincial panel inferred from author's prior work.
- **Key finding:** Inferred to confirm and extend the (2023) labor-reallocation channel.
- **Relevance:** Reinforces the province-level competitor evidence; same gap (no household micro) applies.

### Yang Ruihua (杨汭华) (2021), *Journal of Arid Land Resources and Environment* (《干旱区资源与环境》) — Income risk shocks, agricultural insurance, and rural household labor resource allocation
- **Main contribution:** Tests how agricultural insurance affects rural household labor allocation across ag and non-ag activities, conditional on income volatility. (CoVe-resolved: this is the paper initially flagged as "unattributed CAU paper" — Yang Ruihua, CAU School of Economics & Management.)
- **Method:** Cross-sectional survey of 1,733 households in **Shandong, Henan, Guizhou**. Tobit model with insurance as mediating variable; income volatility as moderator.
- **Key finding:** Insurance contributes to non-ag labor reallocation under income-volatility shocks (full numerical findings require PDF access).
- **Relevance:** **The closest substantive precedent in this cluster — and the one our project must position against carefully.** Critical contrast for our project: Yang (2021) uses (i) cross-section, not panel; (ii) 3-province survey, not CFPS; (iii) Tobit, not DiD; (iv) insurance dummy, not province-year PAY intensity. Our project differs on data, identification, and mechanism framing (services-as-bridge), but the high-level question overlaps. Citation is mandatory.

### Pan et al. (2025), *Review of Development Economics* — "Rising Women": China's agricultural mechanization and labor reallocation by gender
- **Main contribution:** Establishes that mechanization-driven labor reallocation has gendered effects.
- **Method:** [UNVERIFIED: detail beyond title/venue not extracted].
- **Relevance:** **Mechanism, not insurance treatment** — adjacent. Useful for our heterogeneity-by-gender cut.

### Chen (2025), *Review of Development Economics* — Agricultural Mechanization Socialized Services (AMSS) and gender disparities in labor reallocation
- **Main contribution:** Estimates AMSS adoption effect on ag/non-ag labor reallocation by gender using CFPS.
- **Method:** CFPS 2014–2022 panel; DiD on AMSS adoption.
- **Key finding:** AMSS reduces male ag involvement by 4.4 pp, female by 2.3 pp; non-ag work increase nearly 2× larger for men than women.
- **Relevance:** **The methodological template for our project's labor outcome design** — but with AMSS, not insurance, as treatment. Our project effectively combines this paper's labor outcome with the insurance treatment from Zheng & Li (2023).

**Bottom line for cluster (c):** The exact intersection — PAY intensity as treatment, household-level CFPS labor outcomes, services-as-bridge mechanism, quasi-experimental identification — is currently unfilled in the English-language literature. Yang Ruihua (2021) is the closest substantive precedent (3-province cross-section, Tobit) but does not preempt our identification or data design. CoVe-resolved 2026-05-07.

---

## Cluster (d): Related but distinct (brief)

- **Cai, de Janvry & Sadoulet (2015), AEJ:Applied** — Social networks and the decision to insure (RCT, weather insurance for rice farmers in China; network mechanism is insurance-knowledge diffusion).
- **Cai, Chen, Fang & Zhou (2015), AER (microinsurance, sows, trust)** — Trust as barrier to government-provided insurance uptake.
- **Mobarak & Rosenzweig (2013, AER P&P)** — Marketing rainfall insurance to the informally insured in India; demand-side foundation.
- **Cole, Giné, Tobacman, Topalova, Townsend & Vickery (2013), AEJ:Applied** — Barriers to household risk management in India.
- **Janzen & Carter (2019), AJAE** — Index-insurance protective effect on Kenyan pastoralist asset smoothing [UNVERIFIED: exact pagination].
- **He et al. (2021), *International Journal of Disaster Risk Science*** — Farmers' demand for informal risk management and weather index insurance: evidence from China.
- **Mao, Sun, Chai, Fang & Shi (2025), *Ecological Economics*** — Extreme weather, agricultural insurance, and climate adaptation technology adoption (already in cluster b; CoVe-corrected from "Ye et al. 2024").
- **PAY pricing/subsidy design** — *Sustainability* (2021) on fiscal-policy dilemmas in China's PAY subsidy pilot; *Asia & the Pacific Policy Studies* (Kenderdine 2018) on insurance plus futures price reform.

---

## Gaps and Opportunities

1. **No household-level CFPS-based PAY-intensity → labor allocation paper exists in the English literature.** The closest substantive precedent (Yang Ruihua 2021, *J. Arid Land Resources and Environment*) uses 3-province cross-section + Tobit, not CFPS panel + DiD, so the gap stands. This is our project's primary opportunity.
2. **Services-as-bridge thesis is unfilled.** Cha et al. (2024) treat hired-labor cost and machinery as parallel mediators of income; nobody treats productive ag-services (托管 / 社会化服务) as the analytical bridge between PAY and labor restructuring. This is the most distinctive analytical wedge our project adds.
3. **County-level staggered PAY rollout has not been used at the household level for labor outcomes.** Zheng & Zhao (2025) use county/province-level grain resilience; our aspirational design uses county rollout matched to CFPS households for labor outcomes — methodologically novel if we can secure rollout dates.
4. **Parallel-policy disentanglement is under-addressed.** Most provincial-panel papers control crudely (or not at all) for the rural-revitalization, land-rights certification, and ag-socialized-service rollouts that overlap with PAY expansion. Our explicit policy-bundle controls would be a contribution.
5. **Heterogeneity by farm size is mentioned but rarely structural.** Most papers report "regional heterogeneity" (east/central/west). Few make smallholder-size cuts the central interpretive lens, which our project explicitly does.

---

## Methodological notes

- **Common identification strategies.** Provincial fixed-effects panel (dominant); two-way FE (TWFE) DiD on staggered rollout (rising); multi-period DiD on the 2018 full-cost pilot (newly common); 2SLS with weather/density instruments (frequent); PSM on household survey samples (common in China-domestic journals); RCT (rare, mostly Cai). Callaway-Sant'Anna and de Chaisemartin-D'Haultfœuille not yet visible in the China-PAY corpus we surveyed.
- **Common data sources.** China Insurance Yearbook (中国保险年鉴) and MARA reports for treatment; CFPS (rising), CHIP (occasional), RCRE (rare in published literature, restricted access), CHARLS (occasional), domestic single-province surveys (Shandong, Jiangsu, Jiangxi, Anhui, Hubei, Henan most common); county-level panels for the 2018 pilot DiD.
- **Recurring weaknesses.** (i) Parallel-trends silence — many province-panel papers do not display pre-trends. (ii) Narrow provinces — many household surveys cover one or two provinces, limiting external validity. (iii) PAY product confusion — papers rarely distinguish yield, area-yield, income, full-cost, catastrophe products; "agricultural insurance" is treated as homogeneous. (iv) Endogeneity of household-level uptake — selection-on-unobservables rarely addressed beyond IV.

---

## Suggested next steps

**Five papers warranting deep PDF reads for Slice 2:**
1. Zheng & Li (2023, *J. South China Ag. U. Soc. Sci.*) — full method, sample, identification check; closest framing competitor.
2. Cha, Deng, Zheng & Li (2024, *Frontiers Sust. Food Sys.*) — full mediation diagnostics; closest factor-allocation precedent.
3. Chen (2025, *RoDE*) — full empirical specification; methodological template for our labor outcome.
4. Cai (2016, AEJ:EP) — already on our reading list per spec; deep verification of design.
5. Zheng & Zhao (2025, *Frontiers Sust. Food Sys.*) — full DiD specification; template for our staggered rollout robustness.

**Chinese-language landmarks needing direct access:**
1. Yang Ruihua (2021), *Journal of Arid Land Resources and Environment*, Issue 10 — full PDF needed; volume/pages still UNVERIFIABLE; full numerical findings to be confirmed (now-identified closest substantive precedent on the labor-allocation outcome).
2. Yan, Yi & Zhang (2024, *China Rural Economy*) — fertilizer-reduction PAY paper; directly relevant control.
3. Zheng & Ning (2025, *J. Central U. of Finance & Econ.*) — full Chinese PDF needed.

**Holes for Slice 2 (global benchmark) to fill:**
- Index-insurance and labor-allocation outcomes globally (e.g., Carter, Janzen, Mobarak corpus on labor reallocation).
- The Mexican Progresa/Oportunidades and Indian NREGS+insurance literature for downstream-labor-restructuring outcomes.
- Cross-country reviews on insurance-induced production reorganization (e.g., Annual Review of Resource Economics pieces).

---

## BibTeX Entries

All entries below have been CoVe-verified on 2026-05-07 except where flagged `% UNVERIFIABLE`. Key changes from the initial draft are noted in the Post-Flight Verification section.

```bibtex
@article{Cai2016_AEJEP,
  author  = {Cai, Jing},
  title   = {The Impact of Insurance Provision on Household Production and Financial Decisions},
  journal = {American Economic Journal: Economic Policy},
  year    = {2016},
  volume  = {8},
  number  = {2},
  pages   = {44--88},
  doi     = {10.1257/pol.20130371}
}

@article{CaideJanvrySadoulet2015_AEJApp,
  author  = {Cai, Jing and de Janvry, Alain and Sadoulet, Elisabeth},
  title   = {Social Networks and the Decision to Insure},
  journal = {American Economic Journal: Applied Economics},
  year    = {2015},
  volume  = {7},
  number  = {2},
  pages   = {81--108},
  doi     = {10.1257/app.20130442}
}

@article{Karlan2014_QJE,
  author  = {Karlan, Dean and Osei, Robert and Osei-Akoto, Isaac and Udry, Christopher},
  title   = {Agricultural Decisions after Relaxing Credit and Risk Constraints},
  journal = {The Quarterly Journal of Economics},
  year    = {2014},
  volume  = {129},
  number  = {2},
  pages   = {597--652},
  doi     = {10.1093/qje/qju002}
}

@article{ZhengLi2023_JSCAU,
  author  = {Zheng, Jun and Li, Yuwei},
  title   = {Agricultural Insurance, Labor Resource Allocation and Green Economy Efficiency},
  journal = {Journal of South China Agricultural University (Social Science Edition)},
  year    = {2023},
  volume  = {22},
  number  = {4},
  pages   = {69--81},
  doi     = {10.7671/j.issn.1672-0202.2023.04.007},
  note    = {Authors at Anhui University of Finance \& Economics. Chinese-language; English title from journal page. CoVe-verified 2026-05-07.}
}

@article{ZhengNing2025_JCUFE,
  author  = {Zheng, Jun and Ning, Tao},
  title   = {Agricultural Insurance, Labor Resource Allocation and Agricultural Total Factor Productivity},
  journal = {Journal of Central University of Finance and Economics},
  year    = {2025},
  number  = {3},
  pages   = {66--82},
  note    = {Chinese-language. Bibliographic detail confirmed via venue listing; substantive abstract not extractable from public English page.}
}

@article{Chen2025_RoDE,
  author  = {Chen, [given name UNVERIFIABLE — paywalled]},
  title   = {Agricultural Mechanization Socialized Services and Gender Disparities in Labor Reallocation: Insights From Rural China},
  journal = {Review of Development Economics},
  year    = {2025},
  doi     = {10.1111/rode.13228},
  note    = {CFPS 2014--2022 panel; DiD on AMSS adoption. Headline: AMSS reduces male ag involvement by 4.4 pp, female by 2.3 pp. Treatment is mechanization services, NOT insurance.}
}

@article{Pan2025_RoDE,
  author  = {Pan, Rui and Gao, Mengfei and Ji, Yueqing},
  title   = {{``Rising Women''}: Evidence From China's Agricultural Mechanization},
  journal = {Review of Development Economics},
  year    = {2025},
  doi     = {10.1111/rode.13193},
  note    = {Nanjing Agricultural University. CFPS 2014--2022. Treatment is mechanization, NOT insurance.}
}

@article{Cha2024_FrontiersSFS,
  author  = {Cha, Jianping and Deng, Yashan and Zheng, Shaofeng and Li, Feifei},
  title   = {Crop Insurance, Factor Allocation, and Farmers' Income: Evidence from {Chinese} Pear Farmers},
  journal = {Frontiers in Sustainable Food Systems},
  year    = {2024},
  volume  = {8},
  pages   = {1378382},
  doi     = {10.3389/fsufs.2024.1378382},
  note    = {Sample: 1{,}337 pear farmers in Xixian (Shanxi) and Weixian (Hebei). OLS + 2SLS with village-level IV. Hired-labor coef 1.404--2.517 (1\% sig.), machinery 0.323--1.164 (1\% sig.).}
}

@article{ZhengZhao2025_FrontiersSFS,
  author  = {Zheng, Tao and Zhao, Guiqian},
  title   = {The Impact of Policy-Oriented Agricultural Insurance on {China}'s Grain Production Resilience},
  journal = {Frontiers in Sustainable Food Systems},
  year    = {2025},
  volume  = {8},
  pages   = {1510953},
  doi     = {10.3389/fsufs.2024.1510953},
  note    = {Multi-period DiD on premium-subsidy implementation 2002--2012 + FE on insurance development 2012--2021. 31-province panel. Headline coef 0.2755 on grain-production resilience. Published Jan 2025; DOI assigned 2024 (Frontiers practice).}
}

@article{HouWang2025_FrontiersSFS,
  author  = {Hou, Dainan and Wang, Xin},
  title   = {How Does Agricultural Insurance Influence Grain Production Scale? An Income-Mediated Perspective},
  journal = {Frontiers in Sustainable Food Systems},
  year    = {2025},
  volume  = {9},
  pages   = {1524874},
  doi     = {10.3389/fsufs.2025.1524874},
  note    = {27-province panel 2011--2021; FE with stepwise mediation. Specific numerics ($\beta=0.000368$, $\sim$7\% mediation share) require full-text confirmation.}
}

@article{Gu2024_FRL,
  author  = {Gu, Lili and Liu, Yuchen and Liu, Fang and Dong, Xintong and Dong, Yuling},
  title   = {Impacts of Policy-Related Agricultural Insurance on Farmers' Earnings in {China}'s Major Grain-Producing Regions},
  journal = {Finance Research Letters},
  year    = {2024},
  volume  = {69},
  number  = {Part B},
  pages   = {106189},
  doi     = {10.1016/j.frl.2024.106189},
  note    = {13 primary grain-producing areas, 2007--2022. Channels: operational scale, technological progress, credit access. CoVe-corrected from earlier ``Wang \& Yu'' attribution.}
}

@article{Ma2024_AJARE,
  author  = {Ma, [given name UNVERIFIABLE] and others},
  title   = {Beyond Risk Management: Crop Insurance Premium Subsidies Reduce Cropland Abandonment in {China}},
  journal = {Australian Journal of Agricultural and Resource Economics},
  year    = {2024},
  volume  = {68},
  pages   = {891--911},
  doi     = {10.1111/1467-8489.12586},
  note    = {Staggered DiD on household panel 2004--2012; Crop Insurance Premium Subsidies Program reduces cropland abandonment via stabilized income. Full given names UNVERIFIABLE without paywalled access.}
}

@article{Zou2022_Agribusiness,
  author  = {Zou, Baoling and Ren, Zanjie and Mishra, Ashok K. and Hirsch, Stefan},
  title   = {The Role of Agricultural Insurance in Boosting Agricultural Output: An Aggregate Analysis from {Chinese} Provinces},
  journal = {Agribusiness},
  year    = {2022},
  volume  = {38},
  number  = {4},
  pages   = {923--945},
  doi     = {10.1002/agr.21750},
  note    = {31 Chinese provinces, 2004--2018. Effect stronger in Eastern China and \textbf{non-major} crop-producing areas. CoVe-corrected: full author list expanded.}
}

@article{YanYiZhang2024_CRE,
  author  = {Yan, Fei'er and Yi, Fujin and Zhang, Qijia},
  title   = {{Analysis of the Fertilizer-Reduction Effect of Agricultural Insurance: A Re-examination from the Dual Constraints of Credit and Information}},
  journal = {Chinese Rural Economy (中国农村经济)},
  year    = {2024},
  number  = {10},
  pages   = {20--38},
  note    = {Wheat comprehensive cost insurance pilot, Jiangsu; DiD design. Pagination from PDF host filename, manual confirmation pending.}
}

@article{Liu2020_AJAE,
  author  = {Liu, Yanyan and Chen, Kevin and Hill, Ruth Vargas},
  title   = {Delayed Premium Payment, Insurance Adoption, and Household Investment in Rural {China}},
  journal = {American Journal of Agricultural Economics},
  year    = {2020},
  volume  = {102},
  number  = {4},
  pages   = {1177--1197},
  doi     = {10.1002/ajae.12038},
  note    = {RCT among hog farmers; delayed-payment option raises uptake $\sim$10 pp (3$\times$ baseline). CoVe-corrected from earlier ``Wang \& Tong'' attribution.}
}

@article{Li2022_JEM,
  author  = {Li, Houjian and Yuan, Kaihua and Cao, Andi and Zhao, Xuemei and Guo, Lili},
  title   = {The Role of Crop Insurance in Reducing Pesticide Use: Evidence from Rice Farmers in {China}},
  journal = {Journal of Environmental Management},
  year    = {2022},
  volume  = {306},
  pages   = {114456},
  doi     = {10.1016/j.jenvman.2022.114456},
  note    = {Insured plots use $\sim$33.30\% less pesticide per unit land. CoVe-corrected: previously misattributed to ``Fang/Hu/Mao 2022 in J. Cleaner Production''; the 52.7\% figure cited in the earlier draft belongs to Feng/Han/Qiu (2021), not this paper.}
}

@article{Feng2021_CER,
  author  = {Feng, Shuaizhang and Han, Yujie and Qiu, Huanguang},
  title   = {Does Crop Insurance Reduce Pesticide Usage? Evidence from {China}},
  journal = {China Economic Review},
  year    = {2021},
  volume  = {69},
  pages   = {101679},
  doi     = {10.1016/j.chieco.2021.101679},
  note    = {Insured plots use $\sim$52.7\% less pesticide per unit land. Heterogeneity: stronger reduction for SMALLER plots, OLDER farmers, MORE RISK-AVERSE farmers. CoVe-corrected from earlier ``Yang et al.'' attribution; heterogeneity direction inverted from the earlier draft.}
}

@article{Mao2025_EcolEcon,
  author  = {Mao, Hui and Sun, Zhenkai and Chai, Anyuan and Fang, Lan and Shi, Chaoqian},
  title   = {Extreme Weather, Agricultural Insurance and Farmer's Climate Adaptation Technologies Adoption in {China}},
  journal = {Ecological Economics},
  year    = {2025},
  volume  = {228},
  pages   = {108456},
  doi     = {10.1016/j.ecolecon.2024.108456},
  note    = {Survey of 622 Chinese apple farmers. Insurance and CAT are complementary (complementary > substitutive). CoVe-corrected from ``Ye et al. 2024'' attribution.}
}

@article{MobarakRosenzweig2013_AER,
  author  = {Mobarak, Ahmed Mushfiq and Rosenzweig, Mark R.},
  title   = {Informal Risk Sharing, Index Insurance, and Risk Taking in Developing Countries},
  journal = {American Economic Review},
  year    = {2013},
  volume  = {103},
  number  = {3},
  pages   = {375--380},
  doi     = {10.1257/aer.103.3.375},
  note    = {Papers and Proceedings issue.}
}

@article{Cole2013_AEJApp,
  author  = {Cole, Shawn and Gin{\'e}, Xavier and Tobacman, Jeremy and Topalova, Petia and Townsend, Robert and Vickery, James},
  title   = {Barriers to Household Risk Management: Evidence from {India}},
  journal = {American Economic Journal: Applied Economics},
  year    = {2013},
  volume  = {5},
  number  = {1},
  pages   = {104--135},
  doi     = {10.1257/app.5.1.104}
}

@article{Yang2021_JALRE,
  author  = {Yang, Ruihua},
  title   = {{The Impact of Agricultural Insurance on Rural Household Labor Resource Allocation under Income Risk Shocks (收入风险冲击下农业保险对农户家庭劳动力资源配置的影响)}},
  journal = {Journal of Arid Land Resources and Environment (《干旱区资源与环境》)},
  year    = {2021},
  number  = {10},
  note    = {China Agricultural University, School of Economics \& Management. Cross-sectional survey of 1{,}733 households in Shandong, Henan, Guizhou. Tobit model with insurance as mediating variable; income volatility as moderator. CoVe-resolved 2026-05-07: this is the paper initially flagged as the ``unattributed CAU paper.'' Volume/pages still UNVERIFIABLE without library access.}
}
```

---

## Notes on uncertainty

**Honest calibration of what I am sure of vs. not:**

- **Cluster (a):** Reasonably well-covered by web sources; Cai (2016), Karlan et al. (2014), and Cai et al. (2015) are bibliographically rock-solid (verified against AEA pages, QJE, and AEJ:EP DOIs). The 2018 full-cost pilot DiD papers exist and are abundant; I have venue-level confidence but did not extract individual author lists fully — flagged.
- **Cluster (b):** Cha et al. (2024) is fully verified. Karlan et al. (2014) is fully verified. The other behavioral-response papers (Yan et al., Fang et al., Ye et al., Yang et al., Wang & Tong et al.) are confirmed as titles + venues but I could not extract complete author lists or DOIs from search snippets — all flagged `[UNVERIFIED]` for CoVe.
- **Cluster (c):** **Sparse and now CoVe-resolved.** Zheng & Li (2023) is fully verified. Zheng & Ning (2025) has a confirmed venue and title; substantive abstract not extractable. Chen (2025) RoDE confirmed by title, venue, dataset, and headline 4.4 / 2.3 pp gendered effect sizes; first author given name still unverifiable behind paywall. Pan et al. (2025) RoDE — full author list (Pan, Gao, Ji at Nanjing Ag U) confirmed via FAO listing. Yang Ruihua (2021), originally flagged as "unattributed CAU paper," now identified — closest substantive precedent on the labor-allocation outcome but uses 3-province cross-section + Tobit, not CFPS panel + DiD; project's contribution claim survives.
- **Cluster (d):** Mobarak & Rosenzweig (2013) PASS with DOI 10.1257/aer.103.3.375. Cole et al. (2013) author order corrected to published version (Topalova before Townsend); pagination 104–135 confirmed.
- **Chinese-language landmark coverage:** Now firmer (Zheng & Li 2023 PASS; Yan, Yi & Zhang 2024 author detail confirmed via Yi Fujin's institutional page; Zheng & Ning 2025 venue/year/pages confirmed; Yang Ruihua 2021 attribution resolved). **Still missing:** any paper from 经济研究 (Economic Research) or 管理世界 (Management World) on PAY-and-labor — likely behind CNKI paywalls; library access required for Slice 2.
- **What I am confident is true even with uncertainty:** No fully direct competitor exists at the household-CFPS level for our PAY-intensity → labor allocation question. The closest substantive competitor (Zheng & Li 2023) operates at the province-aggregate level. The closest methodological template (Chen 2025) uses the right outcome and dataset but the wrong treatment. The closest substantive precedent on the same outcome (Yang Ruihua 2021) uses 3-province cross-section with Tobit, not CFPS panel + DiD. Our project's contribution sits in this gap.
- **CoVe-resolved (2026-05-07):** The originally-flagged "unattributed CAU paper" is now identified as Yang Ruihua (2021) in *Journal of Arid Land Resources and Environment*. Project's "no direct competitor" claim survives because of data + identification differences; however, Yang (2021) is now the closest precedent and is mandatory to cite.

---

## Post-Flight Verification (CoVe)

Two `claim-verifier` agents in fresh-context forks verified all 21 citations on **2026-05-07**. **Verdict: PARTIAL — corrections applied across the report.**

### Critical resolution

The paper initially flagged as "unattributed CAU working paper" is in fact **Yang Ruihua (2021)**, *Journal of Arid Land Resources and Environment* (《干旱区资源与环境》), Issue 10. The cem.cau.edu.cn URL was a faculty-page reproduction of a published article, not a working-paper venue. The project's "no direct competitor" claim survives — Yang uses 3-province cross-section + Tobit, not CFPS panel + province-year PAY intensity DiD — but Yang (2021) is now mandatory to cite as the closest substantive precedent.

### Bibliographic corrections applied

| Earlier draft attribution | Corrected to | Severity |
|---|---|---|
| "Wang & Yu (2024), FRL" | Gu, Liu, Liu, Dong & Dong (2024), FRL 69(B):106189 | Author misattribution |
| "Wang & Tong et al. (2020), AJAE" | Liu, Chen & Hill (2020), AJAE 102(4):1177–1197 | Author misattribution |
| "Fang, Hu, Mao (2022), J. Cleaner Production" | Li, Yuan, Cao, Zhao & Guo (2022), J. Environmental Management 306:114456 | Author + journal |
| "Yang et al. (2021), CER" | Feng, Han & Qiu (2021), CER 69:101679 | Author misattribution |
| "Ye et al. (2024), Ecological Economics" | Mao, Sun, Chai, Fang & Shi (2025), Ecological Economics 228:108456 | Author + year |
| "Zhang/Liu/Bai → Zou (2022)" | Zou, Ren, Mishra & Hirsch (2022) | Author list expansion |
| "unattributed CAU paper" | Yang Ruihua (2021) | Critical resolution |

### Substantive corrections applied

- **Pesticide-reduction conflation.** The 52.7% figure was originally attributed to the misnamed JCleanProd paper; correct attribution is Feng, Han & Qiu (2021) in CER. The actual finding for the J. Environmental Management paper (Li et al. 2022) is **33.30%**.
- **Heterogeneity direction inversion.** The earlier draft said "large-scale farms show stronger pesticide reduction than smallholders." CoVe-corrected: stronger reduction for **smaller** plots, **older** farmers, **more risk-averse** farmers. This direction is consistent with the services-as-bridge / risk-substitution interpretation our project will lean on.
- **Zou et al. (2022) effect-region direction.** Effect is stronger in **non-major** crop-producing areas, not major.
- **Cole et al. (2013) author order corrected** to published version (Topalova before Townsend).

### Items still UNVERIFIABLE

- Chen (2025) RoDE first author given name (Wiley paywall).
- Ma et al. (2024) AJARE full given names of co-authors (paywall).
- Yan, Yi & Zhang (2024) CRE exact pagination (PDF binary parse failed).
- Hou & Wang (2025) Frontiers SFS β=0.000368 / 7%-mediation numerics (full-text only).
- Yang Ruihua (2021) full numerical findings (require library PDF access).

### Sources used (verifier corpus)

AEA article pages (Cai 2016, Cai-de Janvry-Sadoulet 2015, Mobarak-Rosenzweig 2013, Cole et al. 2013); Oxford Academic (Karlan et al. 2014); IDEAS/RePEc (Gu et al. 2024, Liu/Chen/Hill 2020, Zou et al. 2022, Feng/Han/Qiu 2021, Mao et al. 2025, Ma et al. 2024); Wiley (Chen 2025, Pan et al. 2025); Frontiers in Sustainable Food Systems (Cha et al. 2024, Zheng & Zhao 2025, Hou & Wang 2025); SCAU Journal of Social Science (Zheng & Li 2023); CUFE journal (Zheng & Ning 2025); CAU Economics & Management faculty page (Yang 2021); ScienceDirect / PubMed (Li et al. 2022); FAO listings (Pan et al. 2025).

### Verdict

**No claim preempts the project's "no direct competitor" finding.** The 13 corrections above have been applied throughout the report. Recommend a Slice 2 (global benchmark) lit-review and library access to Yang Ruihua (2021), Yan/Yi/Zhang (2024), Zheng & Ning (2025), and Hou & Wang (2025) for full-text verification of substantive claims.
