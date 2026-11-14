# Literature — Phase 2 audit

Lead-agent consolidation of the Phase 1 and Phase 2 specialist audits. Full tables, URLs and per-item verification tags are in `research/agent_findings/` (file given per section).

**Verification status of everything below:** confirmed from search-result summaries or abstracts only. No full text was read (sandbox blocks direct access to most hosts). `[sec]` = secondary/press only. `[u]` = not confirmed. Re-verify against the primary source before citing in any report.

**Type:** C causal design · A association · D descriptive/accounting · S simulation · R review.

## 1. Development charges and levies (H26-H29) — `P2_development_charges.md`

| Study | Type, design | Finding | Status |
|-------|-------------|---------|--------|
| Skidmore & Peddle 1998 (Growth & Change) | A, DuPage County IL municipal panel 1977-92 | Impact fees cut residential development rate >25% | abstract |
| Burge & Ihlanfeldt 2006 (J Regional Sci) | A, Florida county panel | Water/sewer fees reduce multifamily construction; other fees raise it in inner suburbs | abstract |
| Mayer & Somerville 2000 (RSUE) | A, 44 US metros | Fees small; delay/process restrictions matter more | abstract |
| Mathur, Waddell & Blanco 2004; Evans-Cowley et al. 2009 | A, hedonic | Fees raise new-home prices; Texas: +1.4% new, +6.5% existing homes | abstract |
| Ihlanfeldt & Shaughnessy 2004 (RSUE) | A, hedonic + land | Consistent with capitalization ("new view"); coefficients not retrieved | abstract |
| UK MHCLG developer-contributions series | D | Contributions fall on land value where policy is clear | summary |
| Dachis (C.D. Howe) | A, Ontario cross-section | +10% DC ↔ +0.45% price of new and existing homes | `[sec]`; original not located |
| CMHC Housing Observer 2025/2026 + viability tool | S | DC cuts raise viable projects 9-14% in high-DC cities; Toronto >10% only with 90-100% cut | `[sec]` |
| Desjardins 2026; BILD/Altus | D | DCs grew faster than underlying costs; DCs 8-16% of Ontario condo price | `[sec]`, industry data |
| Sancton 2026 (C.D. Howe) | R | Incidence "exceptionally difficult" to establish | summary |

- **Disagreements.** Sign of supply effect depends on fee type (benefit side capitalized). Incidence: buyers (US hedonics) vs land (UK; theory). An effect on *existing* home prices larger than on new homes signals omitted-variable bias.
- **Gap.** No design-based Canadian estimate of DC effects on starts or of incidence. All US estimates have endogenous fee-setting.

## 2. Zoning entitlement and upzoning (H15, H16, H18, H24) — `P2_upzoning_entitlement.md`

| Study | Type, design | Finding | Status |
|-------|-------------|---------|--------|
| Greenaway-McGrevy & Phillips 2023 (JUE), Auckland | C, upzoned vs non-upzoned areas with displacement modelling | Construction ≈ doubled; ≈5% of dwelling stock | summary |
| Greenaway-McGrevy & So (WP), Auckland rents | C, synthetic control | Rents ~28% below counterfactual at 6 years; range varies by source | summary; WP |
| Murray & Helm 2023 | critique (not peer-reviewed) | Control selection does not support causality | summary |
| Donovan & Maltman 2025 (Land Use Policy) | rebuttal | Critiques fail; independence from pro-reform camp unconfirmed | summary |
| Freemark 2020 (Urban Affairs Rev), Chicago | C, parcel DiD, 5 yrs | Values up; no added permits | summary |
| Büchler & Lutz (WP), Zurich | C, parcel-level | +9% to +13% supply over 5-10 yrs (sources differ); rents unchanged locally | `[sec]` |
| Anagol, Ferreira & Rexer (NBER 29440), São Paulo | C, spatial RD | +1.9% stock, −0.5% prices | abstract |
| Stacy et al. 2023 (Urban Studies) | A, 1,136 US cities | Upzoning +0.8% supply at 3-9 yrs; no rent effect; measurement critique (AEI) | summary |
| Kuhlmann 2021 (JAPA), Minneapolis | C, property comparison | Prices +3-5% | abstract |
| Gu & Munro (WP), Minneapolis | C, synthetic control | Rents below counterfactual but construction weaker — not a supply channel | `[sec]` |
| Terner Center, California SB 9 | D | Very low first-year take-up | summary |
| Zhang 2026 (AAEA conference), Edmonton | C?, parcel | 3-7% value effect; method unread | listing only |
| TRREB (Torous & Xie) 2026, Toronto multiplex | C, DiD large vs small lots | Small relative price rise; pre-trend 2021-22 | summary; industry-commissioned |
| City monitoring (Calgary, Edmonton, Toronto, Vancouver) | D | Calgary 478 DPs/1,904 units; Edmonton 17,775 net new units permitted in 2025; Toronto 452 multiplex permits (May 2023-Nov 2024); Vancouver ~370 R1-1 applications | summary |

- **Disagreements.** Auckland (large supply response) vs Chicago, Zurich, Minneapolis (capitalization, slow or no supply). Auckland itself contested.
- **Gap.** No peer-reviewed causal Canadian evaluation of as-of-right upzoning.
- **Events.** Calgary repeal vote 8 Apr 2026 (12-3), effective 4 Aug 2026; Alberta order to Edmonton and Calgary, early Oct 2026 (date unconfirmed); HAF funds withdrawn from Red Deer, Oakville, Tecumseh.

## 3. Demand, immigration and the rental market (H01, H02, H42, H43) — `P2_demand_rental.md`

| Study | Type, design | Finding | Status |
|-------|-------------|---------|--------|
| Hou, Koumaglo & Zhang 2025 (IRCC/StatCan) | C, municipal census panel 2006-21, FE-IV | +1% new immigrants → +0.143% house values, +0.045% rents nationally; ≈11% of value increase. Rent 0.086 is the large-municipality subsample | summaries; instrument unconfirmed |
| Akbari & Aydede 2012 (Applied Econ) | A, census-division panel 1996-2006 | ≤0.1-0.12% price effect | abstract |
| Saiz 2007 (JUE), US | C, enclave IV | Inflow of 1% of population → ~1% rents | abstract |
| BoC SAN 2023-17; MPR Jul 2024 | D | Newcomers add to demand faster than supply | summary |
| CMHC 2018 supply elasticity | A | Starts response to 1% price rise: Toronto 0.5%, Vancouver 0.3%, Montreal/Calgary/Edmonton 1-2% | snippet |
| Paixão (BoC SAN 2021-21) | A, regional-cycle sensitivity | Low elasticity in Vancouver/Toronto; city values `[u]` | method only |
| Kholodilin 2024 (JHE) | R, ~112 studies | Rent control lowers controlled rents, raises uncontrolled, reduces supply | summary |
| Diamond, McQuade & Qian 2019 (AER) | C | Rent control cut rental supply ~15%; city rents +5.1% | abstract |
| CMHC 2020 rent control; CMHC 2025 review | A / R | 2020 headline: no start difference (report calls it inconclusive); 2025: stock shrinks via conversion, new-build effect unclear | summary |
| CMHC 2026 "Filtering in Canada" | C?, building-level | Calgary nearby rents 2-3% lower after new rental completion; weaker in Vancouver | snippet; design unread |
| Asquith, Mast & Reed 2023 (REStat); Mast 2023 (JUE) | C | Nearby rents −5% to −7%; migration chains reach lower-income tracts | abstract |
| Rentals.ca Oct 2025 | D | Near-campus rents fell in Montreal; rose near U of Toronto while city fell | snippet |

- **Disagreements.** Immigration elasticity spans ~0 to ~1 across designs and countries. No estimate separates NPR from PR or covers 2022-25.
- **Gaps.** No causal study of the 2024 student cap. No econometric evaluation of Ontario's 2018 rent-control exemption.

## 4. Pipeline, viability, capacity, rental policy (H13, H17, H34-H37, H40, H41) — `P2_pipeline_viability.md`

| Study | Type, design | Finding | Status |
|-------|-------------|---------|--------|
| BoC SAP 2026-52 (Surprenant) | C, BVAR with high-frequency shocks | Rate hikes lower prices persistently; starts/permits fall but stock effect slow and modest | abstract |
| BoC SAP 2026-35 | C, state-dependent local projections | Easing lifts resales fast, starts with a lag; larger when unemployment low | abstract |
| BoC SAP 2026-2 (Rao & Wang) | C, SVAR | Tightening lowers prices, raises rent inflation; larger price falls in inelastic cities | abstract |
| Watt, Gu & ab Iorwerth 2026 (StatCan) | D, firm-level 2001-23 | Output per worker −37.3% (−2.1%/yr); all firm sizes | summary; "38.5 pp" not found |
| CMHC labour capacity 2022+ | S, scenario accounting | Capacity short mainly in ON, BC; record 650k workers in 2023 with weak starts | `[sec]` |
| CMHC pending-starts series (from Apr 2026) | D | ~144k approved units awaiting start (Sep 2026), centres ≥50k | `[sec]` |
| City of Toronto pipeline Q4 2025 | D | ~297k approved units; 24,342 approved/yr vs 17,888 built/yr | `[sec]` |
| CivicAction 2025 | D | ~1.2M GTHA units approved-not-built; 12 approved per 1 under construction; project count `[u]` | press |
| Urbanation 2025-26 | D | GTHA condo sales −60% (2025), record cancellations; Toronto condo starts 156 in H1 2026 | press |
| Letwin Review 2018 (UK) | D, 15 large sites | Build-out limited by market absorption rate, not land banking | summary |
| PBO RP-2425-003 | costing | GST rental rebate $5.8B foregone revenue to 2028-29; not an impact evaluation | summary |

- **Disagreements.** Unbuilt-inventory counts differ 8-fold because they count different stages (CMHC 144k permitted; Toronto 297k approved; CivicAction 1.2M). Labour "shortage" vs record employment and record starts in Calgary/Edmonton.
- **Gaps.** No published stage-by-stage pipeline decomposition by city. No causal evaluation of the GST rental rebate or MLI Select found by the audit.

## 5. Other evidence carried from Phase 1 (not re-audited)

- Demand taxes: Dachis, Duranton & Turner 2012 (Toronto LTT, border DiD: 1.1% tax → ~15% fewer sales); BC foreign-buyer tax −5% to −9% (Du, Yin & Zhang 2022) vs much larger (Hartley et al. WP) — `P1_causal_inference.md`.
- Regulation indices: MLURS 2022 (StatCan survey 5382 for CMHC); CMHC 2026 regulation-price estimate (identification unverified) — `P1_urban_planning.md`.
- International institutions (Vienna, Helsinki, Tokyo, Berlin Mietendeckel) — `P1_international.md`. Singapore, Netherlands, Germany tenure, Australia and NZ MDRS not researched.

## 6. Cross-cutting conclusions

1. Canadian design-based evidence exists for demand-side taxes and credit rules; almost none for supply-side policy.
2. Most cited Canadian magnitudes on supply-side costs are accounting or simulation, often industry-commissioned.
3. Every post-2022 natural experiment shares the same confounders: the 2022-23 rate shock, the condo-presale collapse, swings in non-permanent residents, and overlapping federal/provincial measures.
