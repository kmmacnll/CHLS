# Datasets — Phase 2 audit

Index of data sources audited in Phases 1-2. Detail and source URLs: `research/agent_findings/P1_data_ml.md` and the four `P2_*.md` audits.

**Nothing has been downloaded.** Identifiers were confirmed from search listings, not by opening tables. First Phase 4 task: confirm every ID, geography and span through the StatCan Web Data Service and the CMHC portal. Sandbox egress to `statcan.gc.ca` and `cmhc-schl.gc.ca` is currently blocked.

Access: O open · R free registration/key · P paid/licensed · X restricted. Status: V confirmed from listing · u unconfirmed.

## Index

| ID | Dataset (publisher) | Identifier | Measures | Geography × frequency × span | Access | Known issues | St. |
|----|--------------------|-----------|----------|------------------------------|--------|--------------|-----|
| D01 | Starts and Completions Survey (CMHC; StatCan mirror) | 34-10-0154-01 (monthly, selected CMAs); 34-10-0134-01 (annual CMA); 34-10-0135-01 (quarterly, Canada/provinces) | Starts, under construction, completions by dwelling type | CMA × month; long span | O | Completions collected only in CMAs from 2023; revisions | V |
| D02 | Starts/completions/under construction **by intended market** (CMHC) | CMHC data tables / HMIP | Rental, condo, freehold, co-op | CMA and large CA × month | O (portal) | Tenure assigned at start; relabelling incentive after 2023; StatCan does not appear to publish this split | u (history, format) |
| D03 | Starts, completions by municipality (CMHC) | "by Census Subdivisions" tables | As D01 | CSD × month, centres ≥10,000 | O | Portal access; completions at CSD added Dec 2025 | V (sec) |
| D04 | Approved units awaiting start (CMHC) | pending-starts series | Permitted-not-started stock | Centres ≥50k; from Apr 2026 | O | ~7 observations; no back-cast | V (sec) |
| D05 | Building permits (StatCan) | 34-10-0292-01 / 34-10-0285-01 (monthly); 46-10-0075-01, 46-10-0087-01 (annual, CSD, units created/lost) | Value; units | Monthly: Canada/province/CMA/CA only. CSD: annual | O | **Monthly CSD not available** (Phase 1 assumption wrong); issuance timing varies by municipality | V (sec) |
| D06 | New Housing Price Index (StatCan) | 18-10-0205-01 | Contractor new-home prices | CMA/CA × month, 1981+ | O | Contractor-reported; condo coverage | V |
| D07 | Building Construction Price Index (StatCan) | 18-10-0289-01 (replaces 0276, 0135) | Contractor cost by building type | ~15 CMAs × quarter | O | Table IDs churn; excludes land, finance, margin | V |
| D08 | Population and components (StatCan) | 17-10-0148-01, 17-10-0149-01; 17-10-0121-01 (quarterly NPR, province) | Population; net NPR change | CMA × year (2021 boundaries); province × quarter | O | Frequent revisions; NPR stock by CMA unconfirmed | V |
| D09 | Quarterly rent statistics (StatCan, experimental) | 46-10-0092-01 | Asking rents | ~42 CMAs × quarter, 2019Q1+ | O | Not quality-adjusted; listings only | V |
| D10 | Rental Market Survey (CMHC) | HMIP; `cmhc` R package | Vacancy, average rent, turnover, universe | CMA/zone/tract × year (October), 1989+ | O | Purpose-built only; in-place rents sticky; excludes secondary market | V |
| D11 | Canadian Housing Statistics Program (StatCan) | 46-10-0030-01, 46-10-0054-01, 46-10-0069-01 | Ownership, investors, non-residents | Province/CMA (CSD u) × year, ~2018+ | O | Coverage grows over time | V |
| D12 | Census / NHS | profile tables | Stock, tenure, shelter cost, NPR, students | DA-CMA × 5 years | O / R (cancensus key) | Boundary changes; 2011 NHS | u (tables) |
| D13 | Job Vacancy and Wage Survey; LFS (StatCan) | 14-10-0325 (province, quarterly) | Construction vacancies, employment | Province × quarter; CMA noisy | O | Sub-provincial history truncated | u |
| D14 | Ontario Financial Information Return | Schedules 60/61/62 | DC reserve funds and revenue | ~440 municipalities × year, 2019+ | O | **Revenue, not per-unit rates**; contaminated by payment-timing rules | V |
| D15 | Development-charge rate schedules | municipal bylaws and background studies | $ per unit by type and tier | Municipality; hand collection | O | No existing panel; upper/lower-tier stacking; rate locked at application date | — |
| D16 | CMHC development-charge dataset | Housing Observer 2025 (30) / 2026 (40 municipalities) | DCs by dwelling type | Snapshot | O (article); microdata u | No time series | V (sec) |
| D17 | Municipal Land Use and Regulation Survey (StatCan for CMHC) | survey 5382 | Regulation index, approval delay | Municipality; 2022 only | On request | Single wave; measured after outcomes | V |
| D18 | Housing Accelerator Fund rounds data (CMHC) | program page | Agreements, funding, targets | Municipality, 2023+ | O | Selection; self-reported; scores not public | V |
| D19 | Calgary open data | building permits (c2es-76ed); parcel assessments (current, historical) | Permits with application/issue dates; assessed values | Parcel; daily | O | Units and parcel-key fields unconfirmed; development-permit dataset unconfirmed; assessed ≠ market | V (third-party) |
| D20 | Edmonton open data | general building permits (24uj-dj8v) | Permits, 2009+ | Parcel | O | Fields unconfirmed; assessment dataset not found | V (third-party) |
| D21 | Vancouver, Toronto open data | issued permits; development applications/pipeline | Permits; applications | Parcel/project | O | Vancouver issuance-date basis; Toronto zoning layer stale | V (partial) |
| D22 | Metro Vancouver harmonised zoning (MountainMath/UBC) | — | Parcel zoning, 21 municipalities | Current vintage | O | No history | V |
| D23 | IRCC study-permit holders | open.canada.ca 90115b00-… | Permit counts | **Province** × month | O | CMA breakdown archived (2017) | V |
| D24 | Bank of Canada rates | Valet series | Policy, mortgage, prime | Daily/weekly | O | Construction-loan rate not published | u |
| D25 | Teranet-National Bank HPI | — | Repeat-sales index | 11 CMAs × month | summary O; detail P | City level only | V (sec) |
| D26 | Land and transaction prices (Teranet, MPAC, BC Assessment, Altus) | — | Parcel sales, land | Parcel | P/X | Cost and terms not checked | u |
| D27 | Urbanation / Altus | — | Presales, cancellations, unsold, new-home prices | Project, GTHA and other | P | Press figures only | — |

Programmatic access: StatCan Web Data Service (JSON; R `cansim`, Python `stats-can`); CMHC portal via R `cmhc`; CensusMapper via `cancensus` (free key).

## Constructible panels (open data)

| Panel | N × T (approx.) | Supports |
|-------|-----------------|----------|
| CMA × month: starts by dwelling type and intended market, under construction, completions, NHPI, CMA permits; annual population | ~37-41 CMAs × 20+ years | H40, H41, H34, H35, H45 |
| Municipality × month: CMHC starts (centres ≥10,000) + hand-built DC schedule | Ontario GTHA focus, 2018+ | H28 |
| Parcel × month: Calgary, Edmonton permits + Calgary assessments | Thousands of parcels, 2022-26 | H15, H16 |
| CMA × quarter: asking rents + annual NPR components + completions | ~42 CMAs, 2019Q1+ | H02 |
| Municipality × year: annual CSD permits + HAF + Census | ~1,000 CSDs | H25 |
| Municipality cross-section: MLURS 2022 | ~400 | H14 (association only) |

## Coverage by shortlisted hypothesis

| Hypotheses | Outcome data | Treatment/exposure data | Sufficient variation? |
|-----------|-------------|------------------------|----------------------|
| H40 rental tax relief | D02 (CMA × month by tenure) | Federal date; provincial matching rules (to verify) | Cross-province and tenure variation; few provincial clusters |
| H41, H34-H36 pipeline | D01, D02, D05, D07, D13 | Rate shock × pre-shock condo share | Yes for description; causal only for viability arm |
| H15, H16 upzoning | D19, D20 | Reform and repeal dates; prior zoning (reconstruct) | Within-city yes; cross-city few clusters |
| H26-H28 development charges | D03, municipal portals | D15 (to build) | Retiming yes; level effect and incidence no |
| H02 student cap | D09, D10 | D08, D12, D23 | Weak: exposure ≈ province; 2-3 post years |
| H42 rent-control cutoff | none at unit level | none (no first-occupancy date) | No |

## Missing variables and measurement problems

1. Applications and approvals (entitlement stage) are not observable nationally — only in Toronto, Calgary, Edmonton, partly Vancouver.
2. No time-varying national zoning or approval-timeline data; no national zoning atlas.
3. No per-unit development-charge panel; none outside Ontario.
4. No open land prices, municipal new-home prices, project pro formas or presale data.
5. No unit-level rents or first-occupancy dates.
6. Non-permanent-resident stocks and current study permits are not available below province/CMA.
7. "Unbuilt inventory" is not a single object: sources count different pipeline stages.
8. Permits (issuance) ≠ starts (construction begins) ≠ net new units (demolitions, conversions, suites).

## Leakage and endogeneity

- **Mechanical links.** Permits → starts → completions; under construction = previous + starts − completions (holds only approximately; residual must be checked). DC revenue is a function of permits.
- **Revisions.** Population/NPR, starts and permits are revised; use data vintages or lagged availability for any forecasting.
- **Policy-induced relabelling.** Tenure label at start responds to the rental rebate; permit timing responds to DC deadlines and payment-timing rules (Bill 17, 2025); rezonings reclassified as development permits at upzoning dates.
- **Endogenous treatment.** DC cuts followed collapsing sales; regulation indices measured after outcomes; HAF selection; reforms adopted under price pressure.
- **Bad controls.** Contemporaneous prices and population share the cycle with supply outcomes.
- **Validation design.** Time-blocked and leave-CMA-out cross-validation; report errors by regime (pre-2020, 2020-22, 2023+).

## Corrections to Phase 1 data assumptions

- Monthly building permits are CMA/CA-level, not municipality-level.
- 34-10-0135-01 is national/provincial quarterly, not CMA.
- BCPI current table is 18-10-0289-01.
- Ontario FIR reports DC revenue and reserves, not rate schedules.
- IRCC CMA-level study-permit data are archived (2017).
