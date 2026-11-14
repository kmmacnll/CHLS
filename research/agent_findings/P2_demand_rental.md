# P2 — Housing Economist: Demand shocks and rental market (cluster audit)

Method: ~24 WebSearches, snippets only. WebFetch to canada.ca failed (host not in session allowlist), so no primary full text was read. Tags: [V] = seen in a search result attributed to the primary or an official page; [sec.] = secondary summary only; [unverified] = not confirmed this session. Date of audit: 2026-11-14.

## 1. Discrepancy resolved: Hou, Koumaglo & Zhang (IRCC/StatCan, June 2025)

Source: https://www.canada.ca/en/immigration-refugees-citizenship/corporate/reports-statistics/research/immigration-housing-prices-municipalities-canada.html (PDF: https://publications.gc.ca/collections/collection_2026/ircc/Ci4-284-2025-eng.pdf). Not read in full.

| Item | Finding | Status |
|---|---|---|
| Design | Municipal panel, long-form census, 2006–2021 (5-year differences; municipalities >1,000 pop.), first-difference FE and FE-IV | [V] design; instrument construction **not retrieved** |
| Instrument | Shift-share style per one secondary source; "enclave" label not confirmed by any result | [unverified] |
| National FE-IV elasticities | 1% more new immigrants (landed within 5 yrs) → **+0.143% median house value; +0.045% median rent**; immigration ≈ 11% of 2006–21 house-value rise | [V via 2 summaries] |
| Large municipalities (>100k pop., 53 municipalities, ~82% of new immigrants) | 21% of house-value increase, 13% of rent increase (these are **shares of increases, not elasticities**). The **0.086** rent elasticity is attributed to this large-municipality subsample (FE-IV 0.086; FE 0.077) | [sec.], med confidence |
| Rent share, alt. | 2.8% of average 5-yr rent increase under FE vs 11.3% under FE-IV (one summary) | [sec.] |
| Time pattern | Positive 2006–11 and 2016–21; negative for house values 2011–16 | [sec.] |

**Resolution:** the two Phase 1 numbers are not contradictory. 0.045 (rent) and 0.143 (value) are the all-municipality national FE-IV estimates; 0.086 is most likely the rent elasticity in the large-municipality subsample. Phase 1 ECON-1 should not cite 0.086 as the national figure. Do not use a stray 0.419 value-elasticity seen on one immigration.ca page (unlocated, geography unknown). Residual uncertainty: exact table/column not seen.

Key limits of this study for our purposes: new immigrants at census dates are mostly PR landers; NPR (students, workers) enter only if resident at census day; 2021 census predates the 2022–24 NPR surge; five-year spacing; census "rent" is stock rent paid by tenants, not market rent.

## 2. Existing estimates (design, estimate, source, status)

### 2a. Population/immigration → prices and rents

| Study | Design | Estimate | URL | Status |
|---|---|---|---|---|
| Saiz (2007, JUE) US | MSA panel; immigrant-enclave IV | Inflow of 1% of city population → ~1% rents and values | https://repec.iza.org/dp2189.pdf | [V] |
| Cabral & Steingress, BoC SWP 2024-40, US counties | Ancestry IV | Median prices +3.8%, rents +2.2% per their headline; ~2% of US shelter-price growth from immigration (Phase 1) | https://bankofcanada.ca/wp-content/uploads/2024/10/swp2024-40.pdf | [V snippet]; figures from two sources differ in framing |
| Akbari & Aydede (2012, Applied Econ 44(13):1645) | Census-division panel 1996–2006 | Small, significant; ≤0.1–0.12% price effect; driven by earlier-arrived immigrants, not recent | https://econpapers.repec.org/RePEc:taf:applec:44:y:2012:i:13:p:1645-1658 | [V abstract-level; 0.1–0.12 via press summary] |
| Latif, "Immigration and Housing Rents in Canada: A Panel Data Analysis" | Provincial panel | Paper exists (IDEAS record found); Phase 1 quoted rent elasticity 0.14–0.17 | https://ideas.repec.org/a/eis/articl/115latif.html | existence [V]; coefficient **[unverified]** |
| Hou et al. 2025 | see section 1 | | | [V partial] |
| Gala, Univ. Alberta provincial panel 2005–21 | Province panel | "no significant effect on average" | https://journals.library.ualberta.ca/esi/index.php/esi/article/download/1/1 | [sec.] undergraduate-level |
| BoC SAN 2023-17; MPR Jul 2024 "In Focus" | Descriptive/qualitative | Newcomers raise demand faster than supply; adds to rent pressure | https://www.bankofcanada.ca/wp-content/uploads/2023/12/san2023-17.pdf ; https://www.bankofcanada.ca/publications/mpr/mpr-2024-07/in-focus-2/ | [V] qualitative only |
| 2024–26 BoC/StatCan/CMHC causal NPR-rent work | — | **None found** (no BoC SAN/SWP on NPR and rents in 2025–26 surfaced). RBC, BMO commentary: asking rents fell in 2025, in-place rent growth sticky (RBC 3.6% avg 2026 forecast; BMO CPI rent 3.5% from 9.0% peak in 2024) | see section 2b | [sec.] |
| Desjardins/Scotiabank/NBF, Moffatt/Smart Prosperity/Missing Middle | — | **Not searched/not found**; budget exhausted | — | [unverified] |

Disagreement: literature spans from near zero (Akbari & Aydede, Gala) through 0.045–0.143 (Hou) to ~1 (Saiz, US, high-density low-elasticity cities). Differences are partly by design: US studies target metro inflows of 1% of population; Canadian ones use census-period changes in recent immigrants. Hou et al. note US effects 4–13x Canadian ones [V via search summary]. No estimate separates NPR from PR, and none covers 2022–25.

### 2b. Student cap and rents

| Source | What it is | Finding | URL | Status |
|---|---|---|---|---|
| Rentals.ca (Oct 2025 release) | Descriptive; asking rents near campuses vs city, Apr 2024–Apr 2025 | Near McGill 1-bed −4.4% vs Montreal −1.3%; near U of Toronto +7.3% listings vs Toronto avg −6.4% (non-student demand downtown); Calgary little affected | https://press.rentals.ca/432008-rental-prices-near-canadian-post-secondary-schools-drop-as-international-student-numbers-fall | [V snippet]; not causal; Toronto contradicts dose-response |
| CMHC Rental Market Report Fall 2024; CMHC mid-2025/2026 updates; CIMM briefings | Descriptive | Cap put downward pressure on student rental demand, esp. BC, Ontario, Nova Scotia; CMHC publishes no student-specific rent series | https://www.canada.ca/en/immigration-refugees-citizenship/corporate/transparency/committees/cimm-dec-04-2025/cmhc-report.html | [V] |
| CMHC RMR Dec 2025 (secondary coverage) | Descriptive | National PB vacancy 3.1% (2.2% in 2024); Montreal vacancy up due to fewer NPR; turnover rate 8.7%; turnover rents fell | https://www.cmhc-schl.gc.ca/media-newsroom/news-releases/2025/canadas-vacancy-rate-rises-amid-historically-high-rental-construction | [V]/[sec.] |
| CMHC Mid-year 2026 update | Descriptive | Landlords cite new supply as primary reason for falling asking rents; Montreal little change | https://www.cmhc-schl.gc.ca/en/blog/2026/2026-mid-year-rental-market-update | [V snippet] |
| Any DiD/event-study working paper on the cap | — | **None found** (searched NBER/SSRN/IZA terms via general search) | — | gap = novelty, also a warning |

### 2c. Supply elasticity (Canada)

| Study | Estimate | URL | Status |
|---|---|---|---|
| Paixão, BoC SAN 2021-21 | Method: Guren et al. (2021) sensitivity to regional price cycle, not Saiz geography/regulation; a secondary summary gives median 2.2 across CAs, Vancouver 0.63, Winnipeg 4.34 (unclear it is the same paper). **Toronto and other city values not retrieved** | https://www.bankofcanada.ca/wp-content/uploads/2021/09/san2021-21.pdf | method [V]; city values [sec.]/[unverified] |
| CMHC (2018) "Supply constraints increased prices" | Starts response to 1% price rise: Montreal/Calgary/Edmonton 1–2%; Toronto 0.5%; Vancouver 0.3% (2010–16) | https://www.cmhc-schl.gc.ca/professionals/housing-markets-data-and-research/housing-research/research-reports/accelerate-supply/research-insight-supply-constraints-increased-prices-ca-cities | [V snippet] |
| Green, Filipowicz, Lafleur & Herzog (2016) | Not retrieved | — | [unverified]; the unlabelled summary with median 2.2 may be this or Paixão |

Note: Paixão-type elasticities identify sensitivity to regional cycles, assume differences are supply-driven; they are weak instruments of "supply constraint" for rental markets specifically.

### 2d. Rent control

| Study | Design | Finding | URL | Status |
|---|---|---|---|---|
| Kholodilin (2024, JHE 63:101983) | Review (~112 published empirical studies) | 56 of 65 studies: controlled rents lower; 10 of 12: uncontrolled rents higher; reduced supply, misallocation | https://www.diw.de/de/diw_01.c.893635.de/publikationen/externe_referierte_aufsaetze/2024_0000/ | [V]; study counts per slides, [sec.] |
| Diamond, McQuade & Qian (2019 AER) | 1994 SF expansion; treated vs untreated buildings (DiD/RD-style on building date) | Treated landlords cut rental supply ~15% (conversions, redevelopment); city-wide rents +5.1%; tenants more likely to stay | https://www.aeaweb.org/doi/10.1257/aer.20181289 | [V] |
| Autor, Palmer & Pathak (Cambridge decontrol, JPE 2014) | Cambridge MA 1994 decontrol | Not retrieved this session | — | [unverified] |
| CMHC (Nov 2020; KPMG-led) | Toronto, Vancouver, Montreal, Winnipeg comparison; econometrics | Headline: no evidence rental starts lower in rent-control markets; full report calls comparison inconclusive; later econometric section reports negative relationship between control and starts (per commentary) | https://cmhc-schl.gc.ca/professionals/housing-markets-data-and-research/housing-research/research-reports/housing-needs/research-insight-impact-rent-control-housing-affordability | [V]; **disputed reading**; not read in full |
| CMHC (Aug 2025) review of 49 studies | Evidence review | Control shrinks stock through conversions; lower vacancy and listings; effect on new construction unclear | https://assets.cmhc-schl.gc.ca/sites/cmhc/professional/housing-markets-data-and-research/housing-research/research-reports/2025/rent-control-affordability-of-rental-housing-canada-en.pdf | [V snippet] |
| Smith (1988, Ontario) | Not retrieved | — | [unverified] |
| Ontario 2018 exemption | **No econometric evaluation found.** Only Urbanation descriptive counts (>7,500 Toronto PB units since), developer statements ("not the only factor"), CCPA/advocacy critiques | https://www.torontomu.ca/centre-urban-research-land-development/blog/blogentry31-rent-control-has-been-eased-will-gta-rent-growth-follow/ | [V]; confirms gap |

Disagreement: CMHC 2020 headline (no start difference) vs. international literature (supply falls via conversion and redevelopment). Reconciling note: international evidence concerns conversion/withdrawal of existing stock under binding control; the Ontario exemption is about new-build, which is a different margin, and CMHC 2025 says new construction effects are unclear.

### 2e. Local supply → rents (Canada)

| Study | Finding | URL | Status |
|---|---|---|---|
| CMHC (2026), "Filtering in Canada: The Price is Right?" | Calgary: nearby (≈150–250 m) buildings' rents 2–3% lower over 5 yrs after new rental completion vs farther; Vancouver weaker overall, up to ~8% for directly competing higher-rent buildings; limited downward filtering to lowest rents in Toronto/Vancouver | https://www.cmhc-schl.gc.ca/professionals/housing-markets-data-and-research/housing-research/research-reports/accelerate-supply/filtering-canada-is-price-right | [V snippet]; design details (matching/DiD) **not read** |
| Urbanation/CMHC mid-year | Descriptive co-movement of completions and falling asking rents | https://urbanation.ca/news/gtha-condo-rents-down-7-past-6-months | descriptive |

US benchmark (Asquith, Mast & Reed; Phase 1 case 5) not re-verified here.

## 3. Data for the student-cap / NPR exposure design

| Dataset | Geography | Frequency/span | Access | Notes |
|---|---|---|---|---|
| IRCC "Temporary Residents: Study Permit Holders – Monthly IRCC Updates" (open.canada.ca dataset 90115b00-f9b8-49e8-afa3-b4cff8facaee) | **Province/territory × study level × year permit effective**; one resource "rounded, not for calculations" | Monthly refresh | Open | [V]. **CMA breakdown resource is ARCHIVED (last updated 2017)**; no current CMA file found. https://open.canada.ca/data/en/dataset/90115b00-f9b8-49e8-afa3-b4cff8facaee |
| IRCC ad hoc / specialized datasets, Access to Information | Possible CMA, DLI | Ad hoc | Request | [unverified]; DLI-level counts not located |
| PAL/TAL provincial allocations | Province; 2024 cap ~485,000 target; 2025 ~437,000 (120,724 exempt + 316,267 requiring PAL/TAL; Ontario below 2024 target of 141,000 per Ontario) | 2024, 2025 (2026 not checked) | Open | [V via sec.]; BC and full table not retrieved. IRCC notice: https://www.canada.ca/en/immigration-refugees-citizenship/news/notices/2025-provincial-territorial-allocations-under-international-student-cap.html. Caveat: provincial allocation to institutions is **not public by institution** [unverified] |
| StatCan 17-10-0148-01 / 17-10-0149-01 | CMA/CA (2021 boundaries), annual July 1; 17-10-0149 includes net NPR change component | Annual; latest release 14 Jan 2026 | Open | [V]. Components for NPR at CMA yes (per Daily); NPR **stock** by CMA not confirmed. CMA only (no CSD); revisions frequent |
| StatCan 17-10-0121-01 | Canada/provinces, quarterly NPR by type | Quarterly | Open | [V]. Province only |
| StatCan Census 2021 | CSD/CT: non-permanent resident, study-permit holders; student share, tenure | 2021 only | Open | Baseline exposure measure [unverified table]; 2026 Census not yet available |
| PSIS (enrolment by institution, international) | Institution | Annual, lagged | Open/StatCan [unverified table no.] | Not verified this session |
| CMHC Rental Market Survey | Urban centres ≥10,000; CMA/zone/neighbourhood/CT; structure ≥3 units; privately initiated only (excludes secondary market) | Annual, **October**, 1989→ | Open (HMIP, data tables, `cmhc` R package) | [V]. Vacancy, average rent by bedroom, year-of-construction and structure-size tables, turnover vs non-turnover rent changes; asking rent recorded for vacant units |
| CPI rent | CMA/province, monthly | Monthly | Open | [unverified table numbers]; CMA coverage limited to ~ 21 CMAs [unverified] |
| StatCan Quarterly Rent Statistics (table 46-10-0092-01, experimental; built with CMHC; 42 CMAs for Q4 2025; some missing CMAs) | CMA (2-bd apartment, by unit type) | Quarterly, 2019Q1→ latest Q2 2026 | Open | [V]. Asking rents, not quality-adjusted; methodology 46-28-0001 |
| Rentals.ca/Urbanation National Rent Report | Municipal, many cities; primary and secondary market asking rents | Monthly | Free reports; microdata not public | [V]; city count not retrieved; Zumper **not verified** |

## 4. Ontario 2018 cutoff data

| Candidate | Observes first-occupancy date? | Verdict |
|---|---|---|
| CMHC RMS by year-of-construction category | Categories historically include pre-1960,…, 2005+ style bands; **no category isolates post-Nov 2018** at CMA level, but new-build vintages after 2018 can be defined from annual universe additions (buildings entering the universe each year) | Coarse; **no unit-level/sitting-tenant rents** |
| Urbanation (paid) | Project-level completions and occupancy dates for GTA/GGH new rentals and condos; condo rents | Likely best for supply side; paid; [unverified] precise fields |
| MPAC year built | Assessment year-built, not occupancy; rent not observed | Not suitable for an RD |
| Toronto building permits / occupancy permits | Permit dates, not first-tenancy dates | Partial |
| Unit-level sitting-tenant rents | Landlord and Tenant Board rent-increase applications (AGIs) and Residential Tenancies filings; microdata not open [unverified]; CMHC RMS gives building-level turnover/non-turnover aggregates only | **Not observable in open data** |

Honest verdict: first-occupancy date is not observable in any open dataset I could confirm; unit-level rents are not available. An RD in occupancy date (Phase 1 C6) is **not feasible** with open data. A coarse cross-province DiD on purpose-built starts and completions (CMHC) is feasible but confounded by 2017 regulatory expansion reversal, CMHC ACLP financing, development-charge deferrals, rates, and Ontario-specific condo cycles.

## 5. Feasibility of (b) and verdicts

Exposure design facts:
- Units: CMHC RMS and StatCan asking-rent series cover ~35–42 CMAs; RMS zones give within-CMA variation (hundreds of zones) but annual October timing only; student exposure at CMA level needs institution→CMA mapping from PSIS/Census (not CMA-level IRCC permit counts after 2017).
- Exposure dispersion: good between provinces (Ontario/BC cut hardest; Alberta little affected per Rentals.ca) but largely **collinear with province** (province allocations drive treatment), so effective cluster count is ~10 provinces for policy, ~40 CMAs for exposure.
- Concurrent shocks (all confounded with the cap in time and often in space): record PB completions 2024–25 (CMHC attributes falling asking rents to supply); Bank rate cuts from June 2024; weak labour market; Oct 2024 PR/NPR level cuts and Sept 2024 cap tightening; Montreal vs Toronto/Vancouver behaving differently despite similar NPR dynamics. Outflows lag permit expiry.
- Pre-trends: college-town rents were already tracking the 2022–24 NPR boom; Rentals.ca reports Toronto near-campus **up** while city fell. Only 2 post-treatment October RMS observations (2024, 2025; 2026 likely by Dec 2026).
- Measurement: RMS in-place rents sticky (CMHC: ~40% of rent growth from turnover; turnover gap Toronto ~44% in 2024); asking-rent series are quarterly but not quality-adjusted and only listings.

| Q | Verdict | What would falsify it |
|---|---|---|
| (a) Share of 2015–24 rent/price growth from population vs supply vs rates | **Feasible with caveats, accounting/structural not causal.** Elasticities from section 1/2 are too dispersed (0.045 to ~1) and measured on pre-NPR data. Would need CMA×year panel with an NPR instrument; decomposition will be assumption-driven | Estimated NPR elasticity not distinguishable from 0 or from the stock-completions effect; results flip across instruments/specifications |
| (b) Cap and later NPR cuts lowered rents in proportion to exposure | **Feasible with caveats; weakest on identification.** Descriptive support exists; no published causal estimate. Needs CMA×quarter asking rents (46-10-0092) + CMA NPR change (17-10-0149) + completions control. Provincial-allocation instrument is policy-driven but ~10 clusters | No dose-response after controlling for completions pipeline; high-exposure CMAs already diverging pre-2024; effect absent in RMS in-place rents; placebo exposure (e.g. 2019–21) shows similar gradient |
| (c) Ontario 2018 exemption effects on rents/turnover/construction | **Not feasible** for rents/turnover (no occupancy-date or unit-level data); **feasible with caveats** for provincial rental starts (cross-province DiD/synthetic control), heavily confounded | Pre-2018 divergence in Ontario PB starts; synthetic control gap within placebo distribution; effect equal across exempt-eligible and ineligible segments (condo vs PB) |
| (d) New completions lower nearby rents | **Feasible with caveats.** CMHC 2026 filtering study already estimates for Calgary/Vancouver using building-level RMS data (access likely restricted); public replication limited to RMS zone/CT-level; endogeneity of building location and demand growth | No distance-decay pattern; effect disappears with zone×year fixed effects; placebo rings (500+ m) equal near ring |

## Biggest threats
1. Confounding of the cap with completions, rate cuts and weak labour market in 2024–26, with only 2–3 annual post-observations.
2. Exposure collinear with province; no current CMA-level IRCC permit data.
3. Rent measurement: stock vs asking rents; RMS excludes secondary market (where students rent).
4. No causal NPR-specific estimate exists; Hou-type estimates predate the NPR surge.

## Corrections to Phase 1
- ECON-1: 0.086 is not the national rent elasticity; national is 0.045 (rents), 0.143 (values); 0.086 likely large-municipality subsample.
- ECON-7: CMHC 2020 "no start difference" is a headline that the full report calls inconclusive; also CMHC 2025 review exists.
- C6: RD in first-occupancy date lacks data.
- ECON-6: Toronto near-campus rents rose while city fell; treat dose-response as unproven.

## Summary
- Claims (confidence):
  - Hou et al. national FE-IV elasticities: rents 0.045, values 0.143; 0.086 is large-municipality rent (med; primary not read).
  - No peer-reviewed causal study of the student cap on rents exists in my searches (med).
  - No econometric evaluation of Ontario 2018 exemption found (med-high); no occupancy-date data (med).
  - Rent control literature (Kholodilin; Diamond et al.) points to lower controlled rents and supply reduction via conversion, but new-build exemption margin is under-studied (med).
  - CMHC 2026 filtering study finds modest nearby-rent reductions (Calgary 2–3%) (med; snippet).
  - Student-exposure design is feasible only with caveats; Ontario RD is not feasible (med-high).
- Supporting evidence: sections 1–5 URLs.
- Sources: canada.ca Hou et al.; publications.gc.ca Ci4-284-2025; BoC SAN 2021-21, 2023-17, SWP 2024-40; CMHC 2018, 2020, 2025, 2026 filtering; Kholodilin 2024 DIW; AER 2019; StatCan Daily/tables 17-10-0148/0149/0121, 46-10-0092; open.canada.ca IRCC study permit dataset; Rentals.ca press.
- Uncertainty: primary texts not read; instrument unconfirmed; Latif and Green et al. coefficients unverified; Paixão city values unverified; Smith 1988, Autor et al. 2014 not retrieved; table numbers for CPI rent, PSIS not verified; Zumper coverage not verified.
- Assumptions: snippets and summaries accurately represent primary sources; "0.086 = large municipalities" holds.
- Contradictions found: 0.086 vs 0.045 (resolved by sample); CMHC 2020 null vs econometric negative start effect in same report; Toronto near-campus up vs dose-response.
- Recommended next investigations: (1) Obtain Hou et al. PDF and verify instrument, tables. (2) Pull table metadata via WDS for 17-10-0149, 46-10-0092, CPI rent; confirm NPR CMA stock. (3) Build CMA exposure from Census 2021 + PSIS; request IRCC CMA/DLI permit counts. (4) Pre-register event-study with placebo 2019–21 and completions control; power check with RMS zones. (5) Read CMHC 2020 full report and 2026 filtering report for design. (6) Check Urbanation data cost for Ontario first-occupancy proxy.
