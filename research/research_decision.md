# Research decision — Phase 3

Lead agent, 2026-11-15. **Status: proposed; awaiting owner approval. No Phase 4 work has started.**

Basis: `hypotheses.md` (45 hypotheses), `literature.md`, `datasets.md`, four Phase 2 audits, an independent blind ranking and an adversarial review (`agent_findings/P3_*.md`). Reasoning and reviewer disagreement: `synthesis/P3_synthesis.md`.

**Evidence caveat.** Everything below rests on search-result summaries, not full texts, and no data have been downloaded. The decision is therefore conditional on the Phase 4 gate in section 5.

## 1. Selected hypothesis and question

**Question.** How much do multi-unit housing starts in Canadian metropolitan areas respond to shocks to project viability — financing cost and the per-unit tax wedge — and is the response to relief net new supply, or a change of tenure and timing?

**Hypothesis (H\*, from H34, H35, H40, H41).** Since 2022, multi-unit starts have been constrained mainly by project financial viability rather than by entitlement or construction capacity. Viability shocks change *total* multi-unit starts, not only their tenure label.

This is a hypothesis to test, not a finding. Phase 1-2 evidence for it is descriptive.

## 2. Rejected alternatives

| Alternative | Why not selected now | Revisit when |
|-------------|---------------------|--------------|
| C1 as originally framed: "tax-wedge elasticity" via tenure triple difference | Condo is the displaced tenure, not a control. Ontario's incremental relief is ~2-4% of unit value, not 8 points. Effectively three treated provinces. Result cannot be transported to development charges. Kept only as a labelled secondary case study. | — |
| C2 as a structural "which stage binds" study | Applications and approvals unobservable nationally; flows are equilibrium outcomes. Kept as descriptive baseline. | CMHC approved-not-started series has ≥2 years of history |
| C3 Upzoning on/off (Calgary, Edmonton) | Single cities; pre-reform zoning by parcel unverified; reclassification and rush-to-vest inflate counts; low transferability. Best internal validity of the rest. | Edmonton reversion (≈Jan 2027) has a post-period; parcel schemas verified |
| C4 Development-charge retiming | Only timing identifiable; rate panel must be hand-built; ≤8 months post; controls vanish after Mar 2026; incidence needs paid data. | After the 13 Nov 2026 sunset has ≥6 months of post data |
| C5 Student cap and rents | Exposure ≈ province; confounded by record completions and rate cuts; 2-3 post observations. | 2026 Rental Market Survey and Census 2026 exposure data available |
| C6 Housing Accelerator Fund | Selection on ambition; permits are the paid metric; scores not public. | CMHC releases application scores |
| Ontario 2018 rent-control cutoff (RD) | No open first-occupancy or unit-rent data. | Licensed data obtained |
| Cross-city regulation index (MLURS) | Single 2022 wave; measured after outcomes. | Second wave released |

## 3. Evidence supporting the selection

- **Policy weight.** Current federal and provincial housing policy is concentrated on viability levers: rental GST/HST relief, MLI Select and ACLP financing, development-charge cuts, new-home HST relief. None has a design-based Canadian evaluation.
- **Scale of the shock.** GTHA condo starts −63% and record cancellations in 2025 while rental starts hit records in several CMAs; large approved-but-unbuilt inventories. Descriptive, but large relative to noise.
- **Reviewer convergence.** Both independent reviews placed the viability questions (C1, C2) above all others and both proposed merging them on one CMA × quarter starts panel. They disagree on which arm is primary (section 5).
- **Data.** The outcome exists openly at CMA × month by tenure for ~35-40 CMAs; other candidates depend on unverified schemas, hand-built panels or paid data.

## 4. Datasets

| Role | Dataset (`datasets.md` ID) |
|------|---------------------------|
| Outcome | CMHC starts, under construction, completions by intended market and dwelling type, CMA × month, 2015-Mar 2026 (D02, D01) |
| Exposure (primary) | Pre-2022 presale-condo share of multi-unit starts (D02); investor share of condo ownership (D11) |
| Shock | Bank of Canada policy and mortgage rates (D24) |
| Treatment (secondary) | Provincial rental sales-tax relief rules, per-unit dose by province × value band — to be built from CRA and provincial primary texts (new) |
| Controls / descriptives | Permits CMA × month (D05), construction costs (D07), new-home prices (D06), population and NPR (D08), pending-starts stock (D04) |

## 5. Proposed methodology

**Gate (first step of Phase 4; uses pre-2022 data only; nothing after the shock is examined until it is passed and `methodology.md` is frozen).**
1. Download and audit the outcome series: history depth, tenure definitions, accounting-identity residuals.
2. Build the provincial tax-dose table from primary texts.
3. Placebo-date power simulation for both arms; fix all thresholds in section 8.
4. If the primary arm fails pre-trend or power checks, the study proceeds as descriptive only and makes no causal claim.

**Baseline (descriptive).** Starts, completions and permit-to-start conversion by CMA × tenure × quarter; seasonal-naive and fixed-effects benchmarks.

**Primary analysis — financing-viability exposure.** Event study of multi-unit starts on the 2022-23 rate shock interacted with pre-determined CMA exposure to presale-financed condos, with CMA and period effects. Outcomes reported separately for condo, rental and total multi-unit; ground-oriented freehold as placebo. Out-of-sample check on the smaller 2017-18 tightening. Window ends Mar 2026.

**Secondary analysis — provincial tax matching (few-cluster case study).** Per-unit dose; synthetic control per treated province with placebo distribution; leave-one-province-out; British Columbia and Manitoba excluded from controls; first 12 months treated as transition. It cannot rescue a failed primary.

**ML, only after baselines.** Time-blocked counterfactual forecasts of CMA starts trained on pre-shock data as an alternative counterfactual; heterogeneity models only if the design passes the gate.

**Reviewer disagreement on ordering.** The independent methodologist would make the tax-matching arm primary (statutory, dated treatment) and scores the exposure arm's identification lower (exposure correlated with city size, prices, immigration). The adversarial reviewer would make the exposure arm primary (~35 clusters, continuous exposure, models the condo collapse that the tax arm must otherwise control). Lead decision: exposure arm primary, on power and cluster count. The gate can demote either arm.

## 6. Expected contribution

1. First design-based Canadian estimates of how multi-unit starts respond to financing and tax-wedge shocks, by tenure.
2. A direct test of net additionality versus tenure shift for rental tax relief.
3. An open, reproducible CMA × tenure pipeline panel that later phases (simulation) and later questions (C3, C4) can reuse.

Not claimed: a parameter for development-charge cuts; identification of the federal 5-point GST component; separation of MLI Select from the tax relief.

## 7. Major risks

- **Data not yet verified.** Series depth and tenure split are unconfirmed; sandbox cannot currently reach Statistics Canada or CMHC.
- **Exposure endogeneity.** High-exposure CMAs (Toronto, Vancouver) differ in prices, immigration swings and provincial policy.
- **Power in the tax arm.** Large doses sit in Halifax and St. John's; Ontario's is small.
- **Tenure-and-province-specific confounders.** MLI Select/ACLP take-up, Ontario rental DC discounts (from Nov 2022), student cap, Ontario condo collapse.
- **Measurement.** Tenure label assigned at start and responsive to incentives; CRA (excavation) and CMHC (footings) date construction differently.
- **Scope.** Addresses the financing/viability stage only; entitlement, infrastructure and capacity stages remain for later loops.

## 8. Falsification criteria

Thresholds marked † are provisional and are fixed at the gate before post-shock outcomes are examined; they are not changed afterwards.

| # | Result | Consequence |
|---|--------|-------------|
| F1 | Pre-period leads (2015-21) jointly reject parallel trends, or synthetic-control pre-fit exceeds preset error† | No causal claim from that arm |
| F2 | Freehold placebo shows an effect of similar size | Design fails: provincial or city shock, not viability |
| F3 | Total multi-unit starts do not fall more in high-exposure CMAs after the rate shock (interval excludes a meaningful effect†) | **H\* rejected** for the financing channel |
| F4 | Exposure effect absent or reversed in the 2017-18 tightening check, scaled by shock size | Financing interpretation weakened; report as association |
| F5 | Result vanishes when Toronto, or Ontario, is dropped | Reported as a case study, no general estimate |
| F6 | Tax arm: dose ordering violated (Nova Scotia/Newfoundland > Ontario > capped PEI; New Brunswick breaks at Nov 2024) | Not a tax effect |
| F7 | Tax arm: total multi-unit effect includes zero, or condo effect fully offsets rental | "Tenure shift or undetermined", not net new supply |
| F8 | Tax arm: interval for the response lies below 0.3% of starts per point of relief† | Tax-wedge channel (H40) rejected |
| F9 | Quebec's rental starts rise as much as Ontario's without matching relief | Recorded as evidence against H40 |
| F10 | Simulated minimum detectable effect exceeds the plausible effect† | Arm declared uninformative; a null is not reported as "no effect" |

If H\* fails, the hypothesis is revised and the loop returns to the candidates in section 2; the result is recorded in `findings.md` either way.
