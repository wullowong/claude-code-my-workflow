# China Agricultural Insurance — Project Reference Card

Compact reference for `/lit-review`, `/review-paper`, `/research-ideation`, `/data-analysis`, and the domain-reviewer / domain-referee agents. Project-specific to **agri-insurance-labor-china**.

> **Citation discipline:** entries below name authors and rough chronology, but treat any specific claim about findings as **provisional** — verify in the actual paper before relying on it. Use `/verify-claims` on anything that lands in the manuscript.

---

## Policy timeline

| Year | Event | Significance |
|---|---|---|
| 2004 | Central No. 1 Document raises ag insurance | First high-level policy signal |
| 2007 | **政策性农业保险 (Policy-Based Agricultural Insurance, PAY) launched** | County-level pilots in 6 provinces; central + provincial premium subsidy structure introduced |
| 2008–2012 | Phased provincial expansion | Coverage expands to most provinces; crops covered grow from staples to broader list |
| 2013 | Income-protection products piloted | Beyond yield-loss; addresses price + yield jointly |
| 2014 | "Income-as-policy-target" expansion | Subsidy structure refined for major grain crops |
| 2018 | Catastrophe (大灾) insurance pilots | Targets weather + disaster events specifically |
| 2019–2021 | Full-cost insurance pilots in major grain provinces | Subsidy covers up to ~70-80% of premium for grain producers |
| 2022– | Continued expansion of full-cost + income insurance | Aligns with rural revitalization (乡村振兴) strategy |

**Sources to verify the timeline:** Ministry of Agriculture and Rural Affairs (MARA, formerly MOA) annual reports; CIRC / CBIRC / NFRA insurance regulator reports; provincial-level ag-insurance implementation rules.

**Subsidy structure (post-2007 standard):** central government typically covers ~40–50% of premium, provincial ~25%, county/local ~15–20%, smallholder pays the residual. Exact split varies by province, crop, and central directive year — **never claim a fixed share without citing the specific rule**.

---

## Major data sources

### Microdata

| Source | Provider | Strength for this project | Access |
|---|---|---|---|
| **CFPS** (China Family Panel Studies) | Peking U. ISSS | Household labor allocation, ag income, biennial panel since 2010 | Free with registration |
| **CHIP** (Chinese Household Income Project) | CASS / NBS | Rural household income, labor structure; selected years 1988, 1995, 2002, 2007, 2013, 2018 | Restricted; institutional access |
| **RCRE / RFOPS** (Rural Fixed Observation Point Survey) | MARA | Village-level panel since 1986; ag operations, technology adoption | Highly restricted |
| **CHARLS** (China Health and Retirement Longitudinal Study) | Peking U. NSD | Older rural population; some ag insurance variables | Free with registration |
| **CLDS** (China Labor-force Dynamics Survey) | Sun Yat-sen U. | Rural labor allocation, migration | Restricted |
| **CHFS** (China Household Finance Survey) | Southwestern U. of Finance & Economics | Household financial behavior; ag insurance demand | Restricted |

### Administrative / aggregate

- **MARA county-level ag insurance series** — coverage, premium, claims by county/year (often via provincial implementation reports)
- **China Statistical Yearbook on Agriculture (中国农村统计年鉴)** — county and province aggregates
- **China Insurance Yearbook (中国保险年鉴)** — insurer-side data
- **NBS county-level statistics** — for control variables (population, ag GDP, land area)
- **Provincial / municipal Bureau of Statistics yearbooks** — finer geographic detail

### Spatial / weather

- **CMA gridded weather data** — for climate controls or weather-shock instruments
- **MIRCA2000 / MapSPAM** — global crop-area grids; useful for cross-validation
- **GAEZ** — agroecological zones

---

## Terminology (EN ↔ ZH)

| English | 中文 | Notes |
|---|---|---|
| Policy-Based Agricultural Insurance | 政策性农业保险 | The central program; abbreviated PAY in some EN literature |
| Commercial Agricultural Insurance | 商业农业保险 | Pre-2007 / parallel-track non-subsidized |
| Premium subsidy | 保费补贴 | Central + provincial + local layers |
| Smallholder farmer | 小农户 | Operational definition varies; common: <0.67 ha or <1 mu/person |
| Productive Ag-Services | 农业生产性社会化服务 / 农业社会化服务 | "Service outsourcing" of ag operations |
| Ag-service托管 | 农业生产托管 | Specific outsourcing form: a service provider runs operations |
| Cooperative | 农民专业合作社 | Often abbreviated 合作社 |
| Family farm | 家庭农场 | Formalized smallholder; registration-eligible since 2013 |
| Household registration | 户籍 (城镇 / 农业) | "Hukou"; agricultural vs. non-agricultural matters for sample-frame definitions |
| Rural revitalization | 乡村振兴 | Post-2017 policy umbrella |
| Land-rights certification | 农村土地确权 | 2013–2018 nationwide effort; relevant for tenure controls |
| Index insurance / area-yield | 指数保险 / 区域产量保险 | Specific PAY product variants |
| Catastrophe insurance | 大灾保险 | 2018+ pilots |
| Full-cost insurance | 完全成本保险 | 2019+ pilots for major grain provinces |
| Income insurance | 收入保险 | 2013+ pilots |

---

## Anchor literature

These are authors / streams to engage. Do **not** cite a specific paper from memory — find the actual reference, verify the claim, then add to `Bibliography_base.bib`.

### China ag-insurance evaluation

- **Cai (Hongbin)** and co-authors — PAY policy effects on farm decisions
- **Wang Hongmei** and co-authors — ag-insurance demand and adoption in China
- **Mao** and co-authors — area-yield insurance pilots in China
- **Yu Xiaohua** — agricultural risk and insurance from a Chinese-policy lens
- **Liu Yuanyuan, Wang Xiaobing** — ag insurance and household behavior

### Global weather / index insurance benchmark

- **Mobarak (Ahmed) & Rosenzweig (Mark)** — weather index insurance, smallholder risk-taking, rural labor
- **Karlan, Osei, Osei-Akoto, Udry** — rainfall insurance and ag investment (Ghana)
- **Cole, Giné, Vickery; Cole, Tobacman et al.** — ag insurance demand and uptake (India)
- **Cai, de Janvry, Sadoulet** — social networks and insurance adoption (China experiment)
- **Janzen & Carter** — index insurance and asset protection

### Smallholder modernization / ag-service markets

- **Deininger (Klaus)** — land rights, smallholder transitions
- **Otsuka (Keijiro)** — global smallholder transformation, ag value chains
- **Huang Jikun** — Chinese ag-policy + smallholder modernization
- **Wang Xiaobing, Yang** — ag-service outsourcing in China

### Rural labor in China

- **Zhang Xiaobo** — rural labor reallocation, ag-nonag transitions, lewis-turn
- **Yang Dennis Tao** — Chinese rural labor markets
- **Rozelle (Scott)** — rural China labor + education + migration

### Identification methods (when papers are doing DiD on staggered policy rollouts)

- **Callaway & Sant'Anna (2021)** — staggered-adoption DiD, group-time ATT
- **de Chaisemartin & D'Haultfœuille** — DiD with heterogeneous treatment effects
- **Goodman-Bacon (2021)** — TWFE decomposition, negative weights
- **Roth (Jonathan), Sant'Anna, Bilinski, Poe** — pre-trend testing critiques
- **Borusyak, Jaravel, Spiess** — event-study estimators

---

## Cross-references

- `.claude/agents/domain-referee.md` — uses this file when calibrating reviews of project-neighborhood papers.
- `.claude/agents/domain-reviewer.md` — uses this file when reviewing project slides.
- `.claude/references/journal-profiles.md` — pre-staged ag-econ / development journal profiles.
- `Bibliography_base.bib` — canonical bibliography; add anchor citations as you read papers.
