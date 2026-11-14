# P1 — Causal inference: identification landscape (Canada, 2000–2026)

Causal inference specialist, 2026-11-14, 35 searches. Facts were confirmed from search-result summaries of cited pages (full texts not opened); anything else is tagged `[unverified]`. Ratings concern identification, not policy merit. Sources `[S#]` at end.

**S** strong, **M** moderate, **W** weak. "Rates" = 2022–23 rate hikes and subsequent presale slump, a concurrent shock for every post-2022 design.

## Part 1 — Catalogue of policy variation

### A. Zoning / entitlement

| # | What changed, where | Dates | Treated vs comparison | Outcome → design | Main threats | Cred. |
|---|---|---|---|---|---|---|
| A1 | BC Bill 47 transit-oriented areas: minimum allowed density in rings around stations — SkyTrain 0–200 m 5.0 FAR/20 st, 201–400 m 4.0/12, 401–800 m 3.0/8; bus exchanges 200/400 m; no residential parking minimums; distance "crow-flies" from station coordinate [S3,S4] | Introduced Nov 2023; municipal designation by 30 Jun 2024 [S3]; royal assent date `[unverified]` | Parcels just inside vs just outside 200/400/800 m | Land prices, assembly, rezoning/DP applications, permits → spatial RD; difference-in-discontinuities (pre/post) | Minimums non-binding where plans already allowed more; pre-existing distance gradient (needs diff-in-disc); spillover across ring; short post-period | **S** land value; **M** supply |
| A2 | BC Bill 44 SSMUH: ≥3 units on lots ≤280 m², ≥4 on >280 m², 6 on >280 m² within 400 m of frequent bus stop, in municipalities ≥5,000 pop; exemptions incl. lots >4,050 m², unserviced land, TOAs [S1,S2] | Bylaws due 30 Jun 2024; 21 extensions; Bill 25 (2025) amendments [S1] | Lot-size 280 m² and 400 m-to-bus cutoffs; pop. 5,000; extension vs on-time municipalities | Permits by type, land price → RD at lot size/distance; bunching in subdivision; BC vs rest synthetic control | Site standards set locally → heterogeneous treatment; few lots near 280 m²; few municipalities near 5,000; province-level comparison has one treated cluster | **M** (parcel RD); **W** (province-level) |
| A3 | BC Housing Supply Act targets: first 10 municipalities chosen May 2023 from list of 47 by ranked index; orders Sept 2023; later cohorts → 30+ municipalities [S5] | Staggered 2023–25 | Targeted vs not-yet-targeted from the 47 | Completions, approvals → staggered DiD; RD on selection index if published | Selection on need; weak bite (3 of first 10 met year-1 target [S5]); overlaps A1/A2 | **W** |
| A4 | Ontario Bill 23: 3 units/lot as-of-right province-wide; site-plan control removed for ≤10 units [S6,S41] | Royal assent 28 Nov 2022 [S6] | Municipalities already allowing 3 units vs newly bound; projects ≤10 vs 11+ units | ARU permits → DiD by prior permissiveness; bunching at 10 units | Province-wide, simultaneous with DC changes and rates; prior permissiveness endogenous; other rules may share the 10-unit threshold `[unverified]` | **W–M** |
| A5 | Toronto multiplex (4 units citywide, May 2023); sixplex Jun 2025 only in Toronto–East York district + Ward 23; garden suites adopted 2 Feb 2022 (appealed) [S28,S45]; rooming houses 31 Mar 2024 `[unverified]` | As listed | Large vs small lots; sixplex wards vs others (boundary) | Land price, permits → DiD; boundary RD for sixplex | TRREB DiD shows pre-trend in lot-size price gap before May 2023 [S28]; ward opt-in endogenous (council politics) | **W–M** |
| A6 | Vancouver R1-1 multiplex zone replacing nine RS zones [S29] | Approved 14 Sept 2023; effective 17 Oct 2023; ~370 applications to 31 Mar 2025 [S29] | Former RS lots by lot size/frontage eligibility | Applications, land value → RD on lot-size eligibility | Density bonus/charges offset value [S46]; overlaps A2; single city | **M** |
| A7 | Calgary citywide rezoning to R-CG, then repeal [S27] | Effective 4 Aug 2024; repeal process begun 15 Dec 2025; council vote 8 Apr 2026; repeal effective 4 Aug 2026 [S27] | Newly upzoned parcels vs parcels already R-CG/exempt; before/after/after-repeal | Rowhouse permits, land price → within-city parcel DiD with switch-on/switch-off | Rush to vest before repeal (anticipation is itself informative but contaminates level effect); single city; HAF agreement concurrent | **M** |
| A8 | Edmonton: parking minimums removed (effective 2 Jul 2020); new zoning bylaw (Jan 2024); Alberta order in 2026 to revert to pre-2024 parameters and restore parking minimums [S25] (exact order date `[unverified]`) | As listed | Parcels by prior zone; Edmonton vs Calgary/Prairie CMAs | Infill permits, values → parcel DiD; synthetic control. Zhang (2026 conference paper): rights capitalize immediately, completions lag [S26] | COVID (2020); single city; provincial reversal anticipated | **M** (2024); **W** (2020) |
| A9 | Ontario Greenbelt (2005); 2022 removals announced Nov 2022, reversal announced 21 Sept 2023 [S31] | As listed | Parcels inside/outside boundary; 15 removed sites | Land values → boundary RD/hedonic DiD (Deaton & Vyn); event study on removed parcels | Boundary drawn on land characteristics; 2022–23 window ~10 months with non-random site selection | **M** (2005 land values); **W** (housing supply) |
| A10 | Montreal mixed-metropolis bylaw: obligations above 450 m² (social) and 50 units (family); 97% of 145 projects paid fee in lieu; amended 1 Apr 2026 to 18,000 m² threshold [S40]; start date `[unverified]` | 2021–2026 | Projects just under/over thresholds | Project size distribution → bunching | Fee small relative to project → weak first stage; data on project area | **M** |
| A11 | Calgary office-conversion grants (first projects Apr 2022; 21 projects/2,628 homes by Aug 2025) [S39]; also Ontario MZOs, inclusionary-zoning thresholds `[unverified]` | 2021– | Eligible vs ineligible buildings/sites | Conversions → DiD | Tiny N; discretionary site selection | **W** |

### B. Fees, taxes and finance on the supply side

| # | What changed | Dates | Treated vs comparison | Outcome → design | Threats | Cred. |
|---|---|---|---|---|---|---|
| B1 | Ontario mandatory DC phase-in (80→100% over 5 yrs) for by-laws passed after 1 Jan 2022; repealed by Bill 185 [S7,S8] | In force 28 Nov 2022; repealed 6 Jun 2024 | Municipalities by by-law passage date (before/after 1 Jan 2022) | Permit timing, starts → DiD by by-law vintage; bunching around rate steps | By-law timing set before policy (good) but correlated with growth; rates | **M** |
| B2 | Municipal DC cuts: Vaughan (Nov 2024, reset to 2018 rates; details blog-sourced [S13]); Mississauga 50% all residential/100% 3-bed rental (29 Jan 2025) [S10]; Peel Region 50% (10 Jul 2025–13 Nov 2026) [S11]; Toronto froze 1 May 2025 increase, deferral for 3,000 condo units [S12]; Burlington 2024 (size conflicting) | As listed | Border-pair municipalities; unit types with different cut sizes | Permits, applications, new-home prices → event study with border pairs; triple-difference by unit type | Endogenous adoption (cuts responded to collapsing sales → Ashenfelter dip); temporary cuts induce retiming; lower-tier/upper-tier stacking; few clusters | **M** |
| B3 | Scheduled DC indexation/step increases (known dates) | Recurring | Permit pulls days before vs after | Bunching → intertemporal elasticity | Identifies timing, not long-run quantity | **S** (timing); **W** (level) |
| B4 | Bill 109 application-fee refunds; removed by Bill 185 [S8,S9] | 1 Jul 2023 (delayed from 1 Jan 2023; confirm) – 6 Jun 2024 | Applications filed before/after | Decision timelines → RD in time | Municipalities changed pre-consultation rules (measurement gaming); 11-month window | **W–M** |
| B5 | GST rental rebate 36%→100% for construction begun 14 Sept 2023–2030 [S16]; provincial matching: ON, NS, NL, PEI (capped) yes; NB not at announcement; QC not confirmed; BC no PST on such sales [S16] (current status `[unverified]`) | 14 Sept 2023 | Rental vs condo starts; matching vs non-matching provinces | Rental starts → triple-difference (tenure × province × time); bunching in start dates | Condo→rental relabelling; MLI Select and ACLP concurrent; rates; ~5 provincial clusters | **M** |
| B6 | CMHC MLI Select (95% LTV, 50-yr amortization at 100+ points; premium changes 14 Jul 2025) [S43]; launch Mar 2022 `[unverified]` | 2022– | Rental vs ownership; points thresholds | Rental starts; bunching at point thresholds | National, no control; coincides with rates | **W** (aggregate); **M** (threshold bunching, needs CMHC microdata) |
| B7 | Housing Accelerator Fund: 544 applicants, 178 agreements (round 1); round 2 (portal 15 Jul–13 Sept 2024) only for previously unsuccessful applicants [S15] | Agreements staggered 2023–25 | Funded vs unsuccessful applicants; early vs late signers | Permits, zoning changes → staggered DiD among applicants; RD if scores released | Selection on ambition/capacity; reforms pre-dated agreements (PBO) [S14]; permits are the paid metric (gaming); provincial laws (A1, A2, A4) overlap | **W–M** |

### C. Demand-side taxes, credit, rental regulation

| # | What changed | Dates | Treated vs comparison | Outcome → design | Threats | Cred. |
|---|---|---|---|---|---|---|
| C1 | Foreign-buyer taxes: Metro Vancouver (Aug 2016), Ontario GGH (Apr 2017) [S17]; exact days `[unverified]` | As listed | Inside vs outside taxed region; high vs low foreign-buyer neighbourhoods | Prices, sales → border DiD, synthetic control | Displacement to untaxed areas (SUTVA); Toronto bundled with 16-point Fair Housing Plan; estimates range 5% to >20% by design [S17,S18] | **M** |
| C2 | Federal non-Canadian purchase ban, applies inside CMAs/CAs only [S19] | 1 Jan 2023; extended (announced 4 Feb 2024) to 1 Jan 2027 | Properties just inside vs outside CMA/CA boundaries | Prices → boundary RD | Tiny foreign share by 2023 → no first stage; rates | **W** |
| C3 | Vancouver empty homes tax; BC speculation and vacancy tax; Toronto vacant home tax; federal UHT (dates `[unverified]`) | 2017–2023 | City vs neighbours; high-vacancy tracts | Vacancy, rents → DiD [S22] | Border controls share one rental market [S22 critique]; concurrent C1 | **W–M** |
| C4 | OSFI B-20 stress test on uninsured mortgages [S20] | Jan 2018 | Borrowers near qualifying constraint; 5-yr vs 3-yr terms | Credit, prices → bunching/DiD [S21] | National; coincident BoC rate rises [S20]; lender response [S21] | **M** (credit); **W** (prices) |
| C5 | Toronto land transfer tax (2008; month `[unverified]`) | 2008 | Homes within 5 km either side of city border | Sales, prices → border DiD [S36] | Sorting across border; GFC | **S–M** |
| C6 | Ontario rent-control exemption for units first occupied after 15 Nov 2018 [S30] | 15 Nov 2018 (announced same day `[unverified]`) | Units first occupied just before vs after; Ontario vs other provinces | Sitting-tenant rent growth, turnover → RD in first-occupancy date (donut); purpose-built starts → cross-province DiD/synthetic control | Occupancy date manipulable for buildings near completion; supply effect confounded by B5/B6, rates; no published causal study found | **S** (rents/turnover); **M–W** (supply) |
| C7 | Short-term-rental rules: municipal (staggered), BC principal-residence rule (1 May 2024) [S24] | Staggered 2018–24 | Regulated vs not-yet neighbourhoods; BC exempt vs covered communities (population/vacancy thresholds `[unverified]`) | Rents, listings → staggered DiD | Adoption follows rent pressure; industry-funded BC application; enforcement varies | **M** |
| C8 | International-student permit cap (22 Jan 2024), allocated by provincial population so ON/BC cut most [S32]; later NPR reductions | 2024–26 | CMAs/neighbourhoods by pre-cap student share | Asking rents, vacancy → shift-share/dose-response event study | Exposure correlated with campus-town trends; record completions and rate cuts concurrent; outflows lag [S32] | **M** |

## Part 2 — Existing Canadian causal estimates

| Study | Design | Estimate | Critique |
|---|---|---|---|
| Dachis, Duranton, Turner (2012, J. Econ. Geography) [S36] | Border DiD, 5 km band, Toronto LTT | 1.1% tax → ~15% fewer sales; price fall ≈ tax | Best-identified Canadian housing-tax result; local, identifies transactions not supply |
| Du, Yin, Zhang (2022, JHE) [S17] | Panel program evaluation with city controls | Prices −5% Vancouver (Aug 2016–Dec 2017), −7–9% Toronto (Apr–Dec 2017) (abstract, secondhand) | Short window; controls exposed to spillovers |
| Hartley, Ma, Wachter, Zevelev (2022 WP) [S18] | Synthetic control | Much larger effects (GTA price growth up to 28% below counterfactual) | Donor pool/counterfactual drive magnitude; disagreement with [S17] shows fragility |
| Clark & Li (2022, Rev. Finance) [S21] | DiD, 5-yr vs 3-yr spreads | Banks lowered posted 5-yr rate, weakening stress test | Credible mechanism; not a price effect |
| Bank of Canada staff notes [S20] | Before/after, loan microdata | Stress test cut high-leverage lending | 2018 slowdown not separable from higher rates |
| Caracciolo & Miglino (2024, C.D. Howe) [S22] | DiD Vancouver vs Burnaby border | Vacancy −1.5 pp; no affordability effect | Rent result uninformative: treated and control share a market |
| Wachsmuth & St-Hilaire (2024 WP) [S24] | Staggered DiD of municipal STR rules | BC application: rents ~5.7% lower in regulated areas | Under review; endogenous adoption; funder interest; Conference Board (2023) found no effect |
| Hou, Koumaglo, Zhang (StatCan/IRCC 2025) [S33] | Municipal panel 2006–21, FE + IV | +1% new immigrants → +0.143% house values, +0.045% rents; ~11% of increases | Instrument validity not assessable from summary; five-year census spacing. Cf. Latif (2015), provincial panel: rents +0.14–0.17% [S44] |
| Deaton & Vyn (2010 AJAE; 2015 CJAE); Vyn (2012 Land Econ.) [S31] | Hedonic DiD, farmland sales | Greenbelt lowered farmland values near GTA (fragile in 2015 paper); leapfrog premium beyond boundary | Land values only; boundary endogenous |
| Davidoff, Pavlov, Somerville (2022, JUE) [S37] | Hedonic, neighbours of new laneway homes, 2009–17 | Neighbours −3.8% vs garage comparison, concentrated in high-value areas (press summary) | Externality estimate; builder choice endogenous |
| Zhang (2026 conf. paper) [S26] | Edmonton parcel permits 2009–25, sales 2021–25 | Development rights capitalize quickly; completions lag | Unpublished; single city |
| Paixão (BoC SAN 2021-21) [S34] | Sensitivity of city prices to regional cycles (Guren et al.) | Low elasticity Vancouver/Toronto; values not retrieved | Reduced-form proxy; not tied to regulation |
| C.D. Howe DC work [S35] | Unnamed regression | 10% DC rise ↔ +0.45% prices | Association |
| PBO on HAF (2025) [S14] | Participants vs non-participant CMAs, vs 2018–23 mean | Permits +31%, starts +5%; gains concentrated where rezoning pre-dated HAF | Descriptive; selection |

Gap: no design-based Canadian estimate found for DC incidence, the 2018 rent-control exemption, HAF, Bills 44/47 or the student cap. Upzoning benchmarks: Auckland (construction rose; Greenaway-McGrevy & Phillips) vs Chicago (prices up, no short-run construction; Freemark) [S42].

## Part 3 — Cross-cutting problems and recommended designs

1. **Endogenous regulation / reverse causality.** High prices cause both stricter rules and crisis reform; cross-sectional regulation–price correlations (CMHC/StatCan 2023: approval-delay index most, density index least associated with unaffordability [S38]) are not causal. DC cuts were adopted because markets were distressed.
2. **Spillovers (SUTVA).** Municipalities in a CMA share one market: border controls absorb displaced activity, biasing DiD away from zero and voiding rent comparisons [S22]. Use donut designs; estimate CMA-level effects separately.
3. **Lags.** Policy → application → permit → start → completion takes years; recent completions reflect earlier decisions. Use leading outcomes (land prices, applications, permits), pre-register lag windows; completions effects of 2023–25 reforms are not yet identifiable.
4. **Ecological inference.** CMA aggregates cannot attribute changes to parcels; parcel/project microdata (assessment rolls, municipal permits — access `[unverified]`) are required.
5. **Staggered adoption.** Two-way FE is biased under heterogeneous effects; use Callaway–Sant'Anna, Sun–Abraham or stacked DiD with not-yet-treated controls.
6. **Few clusters.** Ten provinces, ~40 CMAs: use randomization inference, wild-cluster bootstrap, synthetic DiD; province-level package "effects" are case studies.
7. **Bundled treatments.** BC and Ontario changed many levers at once; only sub-provincial thresholds separate them.
8. **Measuring regulation.** Survey indices (CMHC/StatCan; Fraser developer survey [S38]) are perception-based and non-response-selected; statutory entitlement ≠ feasible buildability (site standards, charges [S46]). Prefer parcel-level allowed density and measured approval durations.

### Recommended designs (ranked)

| Rank | Design | Identifies | Falsified if |
|---|---|---|---|
| 1 | **BC TOA ring difference-in-discontinuities** (A1; extend to A2 lot-size/bus cutoffs) | Value of entitlement; early supply response | Discontinuity already present pre-Nov 2023 at same size; equal jumps at placebo radii (300/600 m); covariate/lot-characteristic jumps; no jump where minimum exceeded prior zoning (first stage absent) |
| 2 | **Ontario 15 Nov 2018 rent-control cutoff** (C6), RD in first-occupancy date | Effect of rent control on sitting-tenant rents, turnover; (weaker) on rental starts | Bunching of occupancy dates just after cutoff beyond donut; pre-2018-vintage placebo cutoffs show similar breaks; no rent-growth difference among long-stay tenants |
| 3 | **DC changes: border-pair event study + bunching** (B1–B3) | Short-run supply response and timing elasticity to per-unit charges | Pre-trends diverge (cuts follow local collapse); post-cut gains fully offset by pre-cut deficits (pure retiming); equal response in unit types with no cut |
| 4 | **Student-cap exposure design** (C8) | Rent response to a demand shock → demand-side share of rent growth | High-exposure areas already diverging pre-2024; effect disappears controlling for completions; no dose-response |
| 5 | **Upzoning switch-on/switch-off, parcel DiD** (A7, A8) | Take-up of as-of-right infill; option value of vesting | Already-R-CG control parcels show the same permit rise (citywide demand); no pre-repeal rush; effects vanish with neighbourhood × year effects |

HAF (B7) is policy-central but W–M unless application scores are released.

## Hypotheses

### CAUS-1 — Entitlement capitalizes fast; quantity responds slowly
- Mechanism: upzoning raises land option value immediately; construction waits on financing, servicing, charges.
- Predicted effect: positive land-price jump inside TOA rings within ~12 months; permit discontinuity small within 24–36 months.
- Unit of analysis: parcel.
- Required variables: distance to station, prior zoning, sales, applications, permits.
- Potential datasets: BC Assessment, municipal permits `[unverified access]`.
- Existing literature: Zhang (Edmonton) [S26]; Auckland vs Chicago [S42].
- Evidence against: Auckland shows large construction response; minimums may be non-binding near SkyTrain.
- Identification: difference-in-discontinuities (A1).
- Difficulty: med (parcel data licensing).
- Novelty: high (no published BC evaluation found).
- Policy importance: high.
- Class: D.

### CAUS-2 — Temporary DC cuts mostly retime starts
- Mechanism: time-limited cuts and scheduled increases shift permit dates; per-unit charge is small vs price swings.
- Predicted effect: sharp bunching at rate-change dates; 24-month cumulative effect well below spike.
- Unit: municipality-month, project.
- Variables: DC schedules, permit dates, unit type, presales.
- Datasets: municipal by-laws, StatCan building permits, CMHC starts.
- Literature: C.D. Howe association only [S35]; no Canadian design-based estimate.
- Evidence against: DCs at 8–16% of condo price [S35] could have material level effects; long-run incidence may fall on land.
- Identification: B2/B3 border-pair event study + bunching.
- Difficulty: med (hand-coding schedules).
- Novelty: high.
- Policy importance: high.
- Class: D.

### CAUS-3 — Student-cap exposure lowered rents dose-responsively
- Mechanism: exogenous federal cut in arrivals reduces rental demand most where students concentrated.
- Predicted effect: larger 2024–26 asking-rent declines where exposure is high; magnitude unknown (immigration elasticities 0.05–0.17 [S33,S44]).
- Unit: CMA/neighbourhood-quarter.
- Variables: pre-cap study-permit share, rents, completions.
- Datasets: IRCC permits, CMHC Rental Market Survey, listing rents `[unverified access]`.
- Literature: [S32,S33,S44].
- Evidence against: RBC expected little immediate effect [S32]; completions surge confounds.
- Identification: shift-share event study with pre-trend tests.
- Difficulty: med.
- Novelty: high.
- Policy importance: high.
- Class: E.

## Summary
- Claims (each with confidence):
  - Credible identification exists mainly at sub-municipal thresholds (rings, lot-size and vintage cutoffs, borders), not province/CMA level (high).
  - No design-based Canadian estimates yet for DC incidence, HAF, Bills 44/47, the 2018 rent-control exemption, student cap (med; search-limited).
  - Canadian causal literature is strongest on demand taxes and credit rules, weakest on supply regulation (high).
  - Completions cannot yet identify 2023–25 reform effects; land prices, applications, permits can (high).
  - Reversals (Calgary, Edmonton, Bill 185, Greenbelt, Montreal) add switch-off variation but also anticipation (med).
- Supporting evidence: Part 1–2 tables.
- Sources: [S1] https://www2.gov.bc.ca/gov/content/housing-tenancy/local-governments-and-housing/housing-initiatives/smale-scale-multi-unit-housing · [S2] https://www2.gov.bc.ca/assets/gov/housing-and-tenancy/tools-for-government/local-governments-and-housing/webinars/lghi_webinar_2024-01-22_ssmuh-overview.pdf · [S3] https://www2.gov.bc.ca/assets/gov/housing-and-tenancy/tools-for-government/local-governments-and-housing/webinars/lghi_webinar_2024-01-18_tod-area-overview.pdf · [S4] https://www2.gov.bc.ca/gov/content/housing-tenancy/local-governments-and-housing/housing-initiatives/transit-oriented-areas · [S5] https://news.gov.bc.ca/releases/2023HOUS0123-001505 ; https://amp.cbc.ca/lite/story/1.7383562 · [S6] https://cassels.com/insights/more-houses-built-faster-act-bill-23-receives-royal-assent-whats-changed-and-whats-in-force/ · [S7] https://www.osler.com/en/insights/updates/fundamental-changes-made-to-planning-act-appeals-as-bill-185-receives-royal-assent/ · [S8] https://amo.on.ca/policy/land-use-planning-resources-and-climate-change/bill-185-cutting-red-tape-build-more-homes · [S9] https://engage.ottawa.ca/provincial-legislation-planning/news_feed/bill-109-next-steps · [S10] https://www.mississauga.ca/city-of-mississauga-news/news/mississauga-taking-bold-action-to-make-homes-more-affordable/ · [S11] https://storeys.com/peel-region-lower-development-charges/ · [S12] https://www.thetrillium.ca/municipalities-newsletter/toronto-halts-development-charges-increase-housing-slowdown-10598178 · [S13] https://www.homebaba.ca/blog/vaughan-reduces-development-charges-to-zero-to-accelerate-housing-construction · [S14] https://www.pbo-dpb.ca/en/additional-analyses--analyses-complementaires/BLOG-2526-005--an-update-housing-accelerator-fund--point-fonds-accelerer-construction-logements · [S15] https://www.cmhc-schl.gc.ca/media-newsroom/news-releases/2024/changing-how-build-homes-year-housing-accelerator-fund ; https://mpamag.com/ca/news/general/canada-launches-second-round-of-housing-program-to-expedite-construction/496312 · [S16] https://www.blg.com/en/insights/2023/09/canadas-enhanced-gst-rental-rebate-for-new-rental-construction-projects ; https://bdo.ca/insights/gst-relief-announced-for-new-residential-rental-properties · [S17] https://ideas.repec.org/a/eee/jhouse/v55y2022ics1051137721000620.html · [S18] https://aeaweb.org/conference/2023/program/paper/kBBk4zQd · [S19] https://www.airdberlis.com/insights/publications/publication/federal-government-extends-prohibition-on-purchase-of-residential-property-by-non-canadians-to-january-1-2027 · [S20] https://www.bankofcanada.ca/2024/11/staff-analytical-note-2024-25/ ; https://www.bankofcanada.ca/wp-content/uploads/2019/04/san2019-12.pdf · [S21] https://econpapers.repec.org/RePEc:oup:revfin:v:26:y:2022:i:1:p:187-216. · [S22] https://cdhowe.org/sites/default/files/2024-07/E-Brief_356.pdf ; https://morehousing.substack.com/p/c-d-howe-a-bad-study-of-vacancy-taxes · [S23] https://www.abfer.org/media/abfer-events-2023/annual-conference/papers-realestate/AC23P6023-Frictional-and-Speculative-Vacancies-The-Effects-of-an-Empty-Homes-Tax.pdf · [S24] https://upgo.lab.mcgill.ca/publication/bc-str-2024/Wachsmuth_BC_STR_2024.pdf ; https://upgo.lab.mcgill.ca/publication/canada-str-rent/wachsmuth_st_hilaire_public_preview.pdf ; https://www.cbc.ca/1.7327697 · [S25] https://globalnews.ca/news/7101796/edmonton-removes-minimum-parking-requirements/amp ; https://globalnews.ca/news/12093084/alberta-government-edmonton-infill-bylaws/ · [S26] https://ageconsearch.umn.edu/record/404515 · [S27] https://www.calgary.ca/planning/projects/rezoning.html ; https://globalnews.ca/news/11769678/calgary-city-council-approves-repeal-citywide-rezoning/ · [S28] https://trreb.ca/hlfiles/pdf/2026-MOYIR/TRREB-Multiplex-Policy-Report.pdf · [S29] https://www.shapeyourcity.ca/multiplexes/news_feed/sept-2023-council-approves-zoning-changes ; https://vancouver.ca/files/cov/2025-05-29-memo-to-mayor-council-update-r1-1-residential-inclusive-zone-and.pdf · [S30] https://bac-lac.wayback.archive-it.org/web/20210831163910/https://www.ontario.ca/page/residential-rent-increases · [S31] https://www.cbc.ca/lite/story/1.6974058 ; https://econpapers.repec.org/RePEc:oup:ajagec:v:92:y:2010:i:4:p:941-955 ; https://ideas.repec.org/a/bla/canjag/v63y2015i2p185-208.html ; https://econpapers.repec.org/RePEc:uwp:landec:v:88:y:2012:iii:1:p:457-477 · [S32] https://www.rbc.com/en/economics/canadian-analysis/featured-analysis/insights/proof-point-international-student-cap-wont-immediately-cut-rental-demand-in-canada/ · [S33] https://www.canada.ca/en/immigration-refugees-citizenship/corporate/reports-statistics/research/immigration-housing-prices-municipalities-canada.html · [S34] https://www.bankofcanada.ca/wp-content/uploads/2021/09/san2021-21.pdf · [S35] https://cdhowe.org/wp-content/uploads/2018/08/Final-Final-e-brief_281-web.pdf ; https://www.desjardins.com/content/dam/pdf/en/personal/savings-investment/economic-studies/canada-development-fees-18-june-2026.pdf · [S36] https://www.economics.utoronto.ca/workingPapers/tecipa-423.pdf · [S37] https://dailyhive.com/vancouver/laneway-houses-property-values-vancouver · [S38] https://www.cmhc-schl.gc.ca/observer/2023/approval-delays-linked-lower-housing-affordability ; https://www.fraserinstitute.org/studies/new-homes-and-red-tape-in-ontario-residential-land-use-regulation-in-the-greater-golden-horseshoe · [S39] https://amp.cbc.ca/lite/story/1.7480038 · [S40] https://montreal.ca/articles/metropole-mixte-les-grandes-lignes-du-reglement-7816 ; https://www.cbc.ca/lite/story/1.7143670 · [S41] https://www.blg.com/en/insights/2022/12/bill-23-in-ontario-the-more-homes-built-faster-act-2022-receives-royal-assent · [S42] https://eprints.soton.ac.uk/476826/1/Upzoning_Consents_JUE_R2_v2.pdf · [S43] https://assets.cmhc-schl.gc.ca/sites/cmhc/professional/project-funding-and-mortgage-financing/mortgage-loan-insurance/multi-unit-insurance/mliselect/mli-select.pdf · [S44] https://fsc-ccf.ca/research/immigrant-housing-myths/ · [S45] https://www.toronto.ca/city-government/planning-development/planning-studies-initiatives/expanding-housing-options/ · [S46] https://doodles.mountainmath.ca/posts/2025-08-29-multiplex-reforms----the-details-matter/multiplex-reforms--the-details-matter.pdf
- Uncertainty: verification rests on search summaries; several dates tagged `[unverified]`; Vaughan details blog-sourced; Du et al. and Davidoff et al. estimates secondhand; microdata access untested; working papers may have been missed.
- Assumptions: parcel sales/permit data, prior zoning and Ontario first-occupancy dates are obtainable.
- Contradictions found: foreign-buyer-tax effects differ severalfold between [S17] and [S18]; STR–rent effect vs Conference Board null [S24]; EHT rent finding disputed [S22]; CMHC "above forecast" HAF permits vs PBO's modest starts [S14]; Calgary effective date (4 vs 6 Aug 2024); HAF agreements 178 vs 179; Burlington DC cut size.
- Recommended next investigations: (1) confirm parcel-data access for TOA rings, run pre-period placebo; (2) locate first-occupancy/rent microdata for Ontario cutoff; (3) hand-code Ontario DC schedules 2018–26; (4) request HAF scores; (5) verify `[unverified]` dates against statutes; (6) adversarial review of student-cap exposure measure.
