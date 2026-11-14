# P1 — Data / ML Researcher: Canadian housing data landscape audit (revised after second search round)

**Verification key.** [V] = confirmed by web search this session (source URL at the end). [unverified] = recalled from memory, not confirmed. About 20 searches were run in total. Table numbers and existence were confirmed from search-result snippets and listings, not from opening the tables, so confirm on statcan.gc.ca before coding. Access: O = open, R = free registration/key, P = paid or licensed, RDC = restricted.

## 1. Dataset inventory

### 1a. CMHC

| Dataset | ID / publisher | Measures | Geography / frequency / span | Access | Quality issues | Linkage keys | Panel/causal use |
|---|---|---|---|---|---|---|---|
| Starts and Completions Survey (SCS) | CMHC. StatCan mirrors: 34-10-0134-01 annual selected CMAs [V]; 34-10-0154-01 monthly selected CMAs [V]; 34-10-0135-01 is quarterly Canada/regions/provinces, not CMA [V]. | Starts, under construction, completions; absorptions and intended market, dwelling type [unverified detail]. | Monthly. Starts in CMAs and CAs; completions in CMAs only. Surveyed monthly in CMAs/CAs; urban centres 10,000 to 49,999 enumerated in the last month of each quarter [V]. Completions collection limited to CMAs from 1 Jan 2023, so Canada/province/CA/urban-centre completions discontinued (secondary source) [V]. Definition: completion when all proposed work done, or up to 10% remaining [V]. | O | Break in completions coverage in 2023 [V]. Intended market is surveyor-assigned [unverified]. | CMA code; CMHC zone/neighbourhood to CT crosswalk [unverified] | **High.** Core supply outcome. CMA×month. |
| Housing Market Information Portal (HMIP) | CMHC | SCS, Rental Market Survey (RMS), absorptions, by CMA/zone/neighbourhood/CT [unverified detail]. | Monthly/annual | O (UI). R package `cmhc` (mountainMath) wraps HMIP: `get_cmhc()`, vacancy, starts, completions, under construction, rental survey; links to CMHC data by census GeoUID; CRAN, v0.2.x; CMHC licence requires a source notice [V]. No official API [unverified]. | Small-cell suppression and zone redraws [unverified]. | zone ID, CT GeoUID | High for within-CMA variation. |
| Rental Market Survey | CMHC | Purpose-built rental stock: vacancy, average rent, universe. Excludes secondary market [unverified]. | CMA/zone/CT, annual (fall) [unverified] | O | Stock averages, not asking rents [unverified]. | CMA, zone | High for CMA×year rent. |
| Secondary rental market survey | CMHC | Condo and other rentals [unverified] | CMA, annual [unverified] | O | Sample-based, coverage varies [unverified]. | CMA | Medium |
| Construction duration | No standard open table found [unverified]. Derivable from SCS unit-level data (restricted) [unverified]. | | | | | | Medium |
| Housing Supply Reports | CMHC | Modelled supply-gap projections [unverified]. | Province, selected CMAs | O | CMHC's own model, not reproducible [unverified]. | | Benchmark only |
| Housing Accelerator Fund (HAF) data | CMHC rounds data and progress report; PBO update using CMHC data; OpenCouncil tracker [V] | Funded municipalities, funding, targeted units, initiatives. CMHC reports 160,585 residential permits issued under HAF, 22,000 more than expected (CMHC's own counterfactual) [V]. PBO: $4.1B committed and 113,817 anticipated units in Large/Urban stream; $4.44B over 5 years [V]. As of 15 Apr 2024: 544 applications, 179 signed agreements [V]. | Municipality, from 2023 | O | Selection into program; self-reported commitments. | CSD name/code (crosswalk needed) | High (staggered DiD) with selection caveats. |

### 1b. Statistics Canada

| Dataset | ID | Measures | Geography / frequency | Access | Issues | Use |
|---|---|---|---|---|---|---|
| Building Permits Survey | Current monthly value tables 34-10-0292-01 and 34-10-0285-01 on the subject page [V]. Older 34-10-0066-01 cited 2019-2023 and not on the current subject page; probably retired [V, inferred]. | Units and value by structure type and type of work. | Province, CMA, CSD [CSD level unverified]. Monthly. | O | Permit issued at different stages across municipalities [unverified]; value declared at issuance; no stage of build. | **High.** CSD×month if CSD tables confirmed. |
| New Housing Price Index | 18-10-0205-01 (monthly from Jan 1981, base Dec 2016=100; Canada, regions, provinces, CMAs, CAs) [V]. 18-10-0205-02 percent change [V]. Weights 18-10-0210-01 [V]. | Constant-quality contractor-reported new-home prices, with land/structure split [land/structure unverified]. | CMA/CA, monthly | O | Contractor-reported; condo coverage [unverified]. | High for CMA×month price. |
| Building Construction Price Index | Series is rebased and moved repeatedly: 18-10-0135-01 archived and replaced by 18-10-0276-01; that archived and replaced by 18-10-0289-01 (base 2023=100 from Q3 2024); related 18-10-0287-01 (division weights), 18-10-0290-01 (CMA/building weights) [V]. Four new CMAs only from 2023 [V]. | Construction cost index by building type, CMA | Quarterly | O | Table churn; short history for new CMAs [V]. | Medium (cost side). |
| Investment in building construction | Monthly [unverified ID] | Investment | Province, CMA | O | Derived from permits [unverified] | Low independent value |
| Canadian Housing Statistics Program (CHSP) | 46-10-0030-01 (owners by ownership type, residency, number of properties and assessed value), 46-10-0054-01 (non-resident ownership rates), 46-10-0069-01 (owners by investor status) [V, listings]. | Ownership, investors, non-residents, assessed value | Provinces covered from about 2018, coverage expanded by year (NS, ON, BC early) [V partial]. Annual. CSD detail [unverified]. | O (tables); RDC (micro) [unverified] | Assessment-roll based; differing provincial valuation dates [unverified]; uneven coverage over time [V partial]. | High for ownership/investor panels. |
| Census/NHS | Profile tables [IDs unverified] | Stock, tenure, shelter cost, core housing need | DA/CT/CSD/CMA; 5-yearly | O | 2011 NHS voluntary [unverified]; boundary changes; rounding/suppression | High for long-run stock; 5 time points. |
| Population estimates and NPR | 17-10-0148-01 population July 1 by CMA/CA, 2021 boundaries (release 14 Jan 2026) [V]; 17-10-0149-01 components of change by CMA/CA [V]; 17-10-0136-01 content not confirmed [unverified]. Jan 2026 Daily: growth slowed in all 41 CMAs 2024-25 as NPR fell [V]. StatCan warns NPR differs from IRCC temporary-resident counts [V]. Whether NPR is broken out at CMA/CSD in a table is not confirmed [unverified]. | Population and components | CMA annual; province quarterly [quarterly unverified] | O | Boundary vintage (2021 CMA boundaries) [V]; frequent revisions [unverified]. | High (demand), measurement-limited. |
| LFS / Job Vacancy and Wage Survey | table IDs unverified | Construction employment, vacancies | Province/CMA | O | Large sampling error at CMA×industry [unverified] | Medium |
| Municipal Land Use and Regulation Survey (MLURS) | StatCan survey 5382 run on behalf of CMHC; 2022 data released 13 Jul 2023 and "available upon request" [V]. | Zoning, fees, approval times, consultation, density limits, environmental assessments; feeds a Land Use Regulation index. GTA and Greater Vancouver highest index scores (100 and 98) [V]. CMHC finds higher regulation associated with lower affordability across municipalities (association) [V]. | Municipality, single wave (2022) [number of waves unverified] | Upon request; micro access terms unclear [V partial] | Single wave limits panel use; confidentiality rules restrict release [V]. | Very high potential for cross-section; no time dimension. |
| Canadian Housing Survey | biennial [unverified] | Household need | Household/province | RDC/PUMF [unverified] | Small samples | Low |
| Municipal finance | Ontario FIR (Ministry of Municipal Affairs and Housing): downloadable by schedule and year; from 2019 Schedule 61 (DC reserve funds) and 62 (DC rates) separate yearly files, latest 2025; Schedule 60 reserves. Open data catalogue also lists it (file last updated Dec 2021) [V]. FIR is meant to reflect audited statements under PSAB [V]. Municipal treasurer DC statements published separately [V]. Other provinces' equivalents [unverified]. | Revenue, expenses, reserves, DCs | Municipality×year | O | Reserve vs revenue timing [unverified]; amalgamations | High for ON CSD×year fiscal panel. |
| Residential property price index (StatCan) | [unverified] | | | | | |

### 1c. Prices and rents

| Dataset | Notes | Access |
|---|---|---|
| Teranet–National Bank HPI | Repeat-sales, registered land-registry prices; 11 CMAs (Victoria, Vancouver, Calgary, Edmonton, Winnipeg, Hamilton, Toronto, Ottawa, Montréal, Québec, Halifax); unsmoothed since Sept 2022 [V, secondary sources]. Licences offered for index-linked products [V]. Free summary vs paid detail [unverified]. | Mixed |
| CREA MLS HPI | CMA/board benchmark prices [unverified]; access terms not confirmed [unverified]. | Free summary; detail unverified |
| Rentals.ca / Urbanation | Asking rents, monthly reports [unverified]; Urbanation GTA pipeline [unverified]. Asking vs stock rents differ. | Reports free; data P [unverified] |
| MPAC / BC Assessment | Parcel assessments; mostly restricted/paid [unverified]. | P/RDC |

### 1d. Municipal and provincial open data

| Item | Status |
|---|---|
| Toronto Development Applications, building permits (active/cleared) | Listed in Toronto's catalogue, development applications daily-updated; found via a third-party mirror, so confirm at open.toronto.ca [V partial]. Open licence permits commercial use [V]. |
| Calgary | data.calgary.ca has Building Permits and development-permit information, daily updates; standalone development permit dataset not confirmed [V partial]. City publishes approval-timeline info [V]. |
| Vancouver | Issued Building Permits: all permits issued since 2017 per portal description; issuance-date based, status changes not reflected; elapsed-day fields; pre-May-2016 records may have quality problems from software change; monthly update [V]. (The "since 2017" wording is inconsistent with pre-2016 records noted, so check coverage.) |
| Edmonton, Ottawa, Montréal | not searched [unverified] |
| Zoning GIS | Metro Vancouver: 21 municipalities' by-laws digitised and harmonised into a parcel-level dataset (MountainMath/UBC), GeoJSON [V]. Manitoba province-wide zoning polygons [V]. Quebec municipal zoning layers on open data portal [V]. Toronto zoning shapefiles under By-law 569-2013 dated Sept 2014 (old); Mississauga 2016 land use/zoning dataset [V]. Mostly current-vintage only; historical zoning needs archives [unverified]. |
| Development-charge histories | Ontario FIR Schedules 61/62 from 2019 [V]; earlier years and other provinces hand-collected from bylaws [unverified]. BILD/Altus benchmarking [unverified]. |
| Provincial housing-target tracking (ON 2023-31 targets, BC target orders) | [unverified] |

### 1e. Regulatory indices and zoning atlases
- **CMHC/StatCan Land Use Regulation index from MLURS 2022** (above) [V]. Municipal-level and cross-sectional only.
- **Fraser Institute** developer-survey indices for Greater Golden Horseshoe, Lower Mainland and Calgary-Edmonton corridor; five components (Approval Timelines, Council and Community, Cost and Fees, Rezoning Prevalence, Timeline Uncertainty); typical approval timelines from 13.8 months (Burlington) to 28 months (Clarington) [V]. Perception survey by an advocacy think tank; treat as validation not truth.
- **National zoning atlas:** none found; a Canadian Zoning Atlas has been called for but not shown to exist [V, podcast description]. Closest is the Metro Vancouver parcel-level harmonised zoning [V].

### 1f. Access routes and boundaries
- **StatCan WDS:** JSON over HTTPS; methods include getDataFromVectorsAndLatestNPeriods and getDataFromCubePidCoordAndLatestNPeriods; not intended for large bulk pulls; limits of 50 requests/s server-wide and 25/s per IP; scalar factor must be applied separately [V]. Wrappers: R `cansim` (`get_cansim_vector_for_latest_periods` etc.) and Python `stats-can` [V].
- **cancensus:** needs a free CensusMapper API key (`set_cancensus_api_key(..., install=TRUE)`); Python port pycancensus uses the same service [V].
- **cmhc:** see HMIP above [V].
- **Boundaries:** StatCan CMA tables use 2021 boundaries [V]; four CMAs added to BCPI in 2023 [V]. CMA/CSD redefinitions, CT redraws every census and amalgamations require a fixed vintage and concordances [unverified general knowledge]. 2022-23 StatCan Daily referencing 41 CMAs vs the 37 geography items in the annual starts table suggests the CMA count differs across tables [V, inferred].

## 2. Assessment

**(a) Constructible panels (N×T are my estimates, [unverified] unless noted).**
1. CMA×month: starts, under construction, completions (selected CMAs), NHPI, permits, population (annual). N about 37-41 CMAs [V that tables show 37-41], T about 25-45 years; about 10,000+ obs. Best.
2. CSD×month/year permits plus Census (5-yearly) plus Ontario FIR (2019+ for DC schedules). N about 1,000+ CSDs. Many zeros in small places. FIR DC panel short.
3. CT×year from HMIP: thousands of CTs, about 20 years; scraping and CT concordance needed.
4. Municipality×year policy panel (HAF from 2023, provincial targets 2023+): short post window.
5. City application-level pipeline (Toronto, Calgary, Vancouver at least): tens of thousands of records, not harmonised.
6. Cross-section: MLURS 2022 index (about 400+ municipalities per trade press [V secondary]) merged to permits and prices: a regulation-outcome cross-section, no time variation.

**(b) Missingness, suppression, measurement.** CMA-only completions from 2023 [V]. Small-cell suppression at CT [unverified]. Permit timing and valuation vary by municipality. CHSP coverage grows over time [V partial]. NPR revisions and definitional differences from IRCC [V]. RMS excludes the secondary market [unverified]. BCPI and other table IDs churn [V], so pipelines must use vector IDs or maintain mapping. Vancouver issuance-date basis [V].

**(c) Leakage.** Permits to starts to completions are mechanical lagged links; under construction = prior + starts - completions (identity) [reasoning]. Investment in building construction is permit-derived [unverified]. Contemporaneous prices and population are common-cycle drivers (bad controls). Use real-time vintages for revised series (NPR). Use time-blocked and leave-CMA-out CV given spatial and serial correlation. MLURS 2022 and Fraser indices are measured after outcomes (reverse causality); HAF "expected vs actual" is CMHC's counterfactual.

**(d) Where ML adds value.** Panel/event-study methods suffice for HAF, targets, DC reforms. ML adds value for: NLP of bylaws and council minutes to build time-varying stringency measures; duration/survival models on application data; nowcasting with proper CV; double ML for high-dimensional controls; heterogeneity (causal forests) once a credible design exists; harmonising boundaries and imputing suppressed cells. Little value on aggregate national series.

**(e) Biggest gaps.** (1) Time-varying national zoning/land-use rules (MLURS is one wave; no atlas) [V]. (2) Harmonised application-level approval timelines. (3) Historical DC and fee panel outside Ontario 2019+. (4) Project-level costs and pro formas. (5) Developer/builder concentration and entry. (6) Serviced land and infrastructure capacity. (7) Secondary-market rents, conversions and demolitions. (8) NPR housing demand at CSD level. (9) Non-CMA completions after 2023 [V].

## 3. Data/ML-driven hypotheses

### DATA-1 — Permit-to-start-to-completion conversion varies by city and drives supply gaps
- Mechanism: attrition and delay after permit reflect financing, costs, inspections, local conditions.
- Predicted effect: conversion falls with rates and costs; varies with regulation. Magnitude unknown.
- Unit: CMA×quarter.
- Variables: permits, starts, completions, BCPI/NHPI, policy rate, MLURS index.
- Datasets: Building Permits, SCS (34-10-0134/0154), BCPI (18-10-0289), MLURS 2022.
- Literature: not searched.
- Against: definitional mismatch, permit lapse, timing.
- Identification: descriptive decomposition; panel FE; rate-shock exposure heterogeneity.
- Difficulty: low-medium. Novelty: medium. Policy importance: high.
- Class: D under-researched

### DATA-2 — Staggered HAF effects on permits and starts
- Mechanism: HAF funding conditional on zoning and process reforms raises permits.
- Predicted effect: positive on permits; CMHC reports 22,000 more permits than expected (its own counterfactual, not causal) [V].
- Unit: CSD×month.
- Variables: HAF agreement dates/amounts, rejected/pending applicants, permits, population.
- Datasets: CMHC HAF rounds data, Building Permits.
- Literature: PBO update on HAF (committed funding and anticipated units only verified) [V].
- Against: selection, pre-trends, announcement effects, short post period, concurrent shocks.
- Identification: staggered DiD (Callaway-Sant'Anna), rejected-applicant comparison, synthetic DiD.
- Difficulty: medium. Novelty: medium-high. Policy importance: high.
- Class: D under-researched

### DATA-3 — Using MLURS 2022 plus NLP bylaw measures to estimate regulation-supply relationships
- Mechanism: restrictive land-use rules reduce supply elasticity.
- Predicted effect: negative on permits per population growth; stronger in high-demand cities. CMHC reports association with lower affordability [V]; causal size unknown.
- Unit: municipality (cross-section), extended to municipality×year via NLP of archived bylaws.
- Variables: MLURS index and components, permits, prices, demand shifters.
- Datasets: MLURS (on request), Building Permits, Census, bylaw text.
- Literature: Fraser Institute indices [V]; CMHC analysis [V].
- Against: stringency endogenous to demand; measured after outcomes; single wave.
- Identification: reform events (e.g. provincial legislation) with MLURS as treatment intensity; no instrument yet.
- Difficulty: high. Novelty: high. Policy importance: high.
- Class: E potentially novel

### DATA-4 — Application-level survival models of approval time across cities
- Mechanism: delay acts as carrying-cost tax.
- Predicted effect: longer expected approval lowers start hazard; magnitude unknown.
- Unit: application/project.
- Variables: submission, approval, permit dates, size, type, ward.
- Datasets: Toronto, Calgary, Vancouver portals [V partial].
- Literature: Fraser survey timelines 13.8 to 28 months in GGH [V]; Calgary and Vancouver publish timelines [V].
- Against: selection of harder projects, censoring, inconsistent status codes.
- Identification: survival models with ward/planner variation, council turnover; ML (survival forests) for prediction only.
- Difficulty: medium-high. Novelty: medium. Policy importance: high.
- Class: D under-researched

### DATA-5 — Development-charge reliance and municipal approvals (Ontario)
- Mechanism: DC funding structure shapes local approval incentives.
- Predicted effect: ambiguous.
- Unit: Ontario municipality×year.
- Variables: DC rates/reserves (FIR Sch. 61/62), permits.
- Datasets: Ontario FIR (2019+) [V], bylaws for earlier years.
- Literature: not searched.
- Against: endogenous DC setting; province-wide reforms (Bill 23) lack cross-sectional variation except via pre-reform exposure.
- Identification: exposure-based event study.
- Difficulty: medium. Novelty: medium. Policy importance: high.
- Class: B partially understood

### DATA-6 — Time-blocked forecasting benchmark for CMA starts and completions
- Mechanism: lagged permits, rates, population flows predict starts.
- Predicted effect: prediction only; ML gain over AR plus permits uncertain.
- Unit: CMA×month.
- Datasets: SCS, Building Permits, NHPI, population.
- Literature: not searched.
- Against: autocorrelation, regime breaks (2020, 2022-24).
- Identification: none (predictive); rolling-origin evaluation, vintage data.
- Difficulty: low-medium. Novelty: low. Policy importance: medium.
- Class: A (method); application D

## Summary
- Claims (confidence):
  - CMA×month (SCS plus permits plus NHPI plus population) is the cleanest open panel; CSD×month permits the finest (med-high).
  - MLURS 2022 (StatCan survey 5382 for CMHC) is a national municipal regulation dataset but a single wave, available on request (high on existence, med on access).
  - No national time-varying zoning/approval-time dataset or zoning atlas found; the Metro Vancouver harmonised zoning is the closest (med).
  - CMHC completions coverage narrowed to CMAs from 2023 (med-high; primary CMHC confirmation not found, secondary source plus CMHC methodology page on current coverage).
  - BCPI table IDs have churned (18-10-0135 to 0276 to 0289), so ID-pinning is fragile (high).
  - Permits, starts, under-construction and completions are mechanically linked; this is the main leakage source (high, reasoning).
  - Ontario FIR DC schedules 61/62 are available from 2019 (high).
  - ML adds most in text-based regulation measures, duration models and nowcasting; panel econometrics suffices for most policy evaluation (med).
- Supporting evidence: StatCan listings for 34-10-0134/0154/0135/0292/0285, 18-10-0205/0289, 17-10-0148/0149, 46-10-0030/0054/0069; MLURS survey pages; CMHC HAF pages and PBO update; Ontario FIR site; Fraser indices; cansim/cmhc/cancensus docs; WDS guide.
- Sources:
  - https://www150.statcan.gc.ca/n1/en/subjects/construction/building_permits
  - https://www150.statcan.gc.ca/n1/en/catalogue/3410013501
  - https://www150.statcan.gc.ca/n1/en/cansim/327-0056
  - https://www150.statcan.gc.ca/n1/en/surveys/2317
  - https://www150.statcan.gc.ca/n1/daily-quotidien/250204/dq250204b-eng.htm
  - https://www150.statcan.gc.ca/t1/tbl1/en/tv.action%3Fpid%3D1710014801
  - https://www150.statcan.gc.ca/n1/daily-quotidien/260114/dq260114a-eng.pdf
  - https://www150.statcan.gc.ca/n1/pub/46-28-0001/2023001/article/00001-eng.htm
  - https://www.statcan.gc.ca/en/survey/business/5382
  - https://www150.statcan.gc.ca/n1/en/surveys/5382
  - https://www.cmhc-schl.gc.ca/observer/2023/approval-delays-linked-lower-housing-affordability
  - https://www.cmhc-schl.gc.ca/en/professionals/housing-markets-data-and-research/housing-research/surveys/methods/methodologies-starts-completions-market-absorption-survey
  - https://comox-valley-vital-signs.tracking-progress.org/?p=836
  - https://www.cmhc-schl.gc.ca/professionals/project-funding-and-mortgage-financing/funding-programs/all-funding-programs/housing-accelerator-fund/housing-accelerator-fund-rounds-data
  - https://www.pbo-dpb.ca/en/additional-analyses--analyses-complementaires/BLOG-2526-005--an-update-housing-accelerator-fund--point-fonds-accelerer-construction-logements
  - https://opencouncil.ca/housing-accelerator-fund/
  - https://efis.fma.csc.gov.on.ca/fir/index.php/open-data/fir-by-schedule-and-year/
  - https://data.ontario.ca/en/dataset/municipal-financial-information
  - https://opendata.vancouver.ca/explore/dataset/issued-building-permits/
  - https://mountainmath.ca/mountain_math/metro_vancouver_zoning
  - https://housepriceindex.ca/about/our-methodology/
  - https://www.fraserinstitute.org/studies/new-homes-and-red-tape-in-ontario-residential-land-use-regulation-in-the-greater-golden-horseshoe
  - https://rdrr.io/cran/cancensus/man/set_cancensus_api_key.html
  - https://mountainmath.ca/mountain_math/cmhc_pkg
  - https://statcan.gc.ca/en/developers/wds/user-guide
- Uncertainty: Table IDs verified from listings, not by opening tables. Start years, CSD-level availability of permit and CHSP tables, NPR at CMA/CSD, LFS/JVWS IDs, CREA access terms, Edmonton/Ottawa/Montréal portals, provincial target tracking remain unverified. N×T figures are rough.
- Assumptions: N×T estimates are orders of magnitude; 37-41 CMA counts differ by table and vintage.
- Contradictions found: 34-10-0135-01 is a quarterly national/provincial table, not CMA. 34-10-0066-01 appears superseded. Vancouver permit dataset description (since 2017) conflicts with a note about pre-May-2016 records, so confirm coverage. CMHC's HAF "22,000 more permits than expected" is its own counterfactual, not an independent estimate. The earlier draft's statement that a StatCan MLURS could not be verified is now corrected: it exists.
- Recommended next investigations: (1) Request MLURS 2022 microdata/index and document access terms. (2) Pull table metadata via WDS to confirm table IDs, coverage and start dates (permits CSD, CHSP, NPR). (3) Build the CMA×month panel and the conversion analysis (DATA-1). (4) Assemble the HAF treatment file including rejected applicants (DATA-2). (5) Test harmonisation of Toronto/Calgary/Vancouver application data (DATA-4). (6) Verify CREA data terms and Edmonton/Ottawa/Montréal portals.
