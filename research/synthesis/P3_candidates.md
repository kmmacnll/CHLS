# Phase 3 candidate research questions (neutral brief)

Lead agent, 2026-11-14. Built from `research/hypotheses.md`, `research/synthesis/P1_synthesis.md` and the four Phase 2 audits (`research/agent_findings/P2_*.md`). This file states candidates and audited facts only; it contains no ranking. All facts are from search summaries, not full texts.

Charter ranking criteria: policy importance · empirical testability · data quality · novelty · causal identification potential · ML suitability · scalability across Canadian regions · potential for actionable policy conclusions.

Constraint: prefer designs feasible with open data. Paid/restricted sources (Teranet, MPAC, BC Assessment, Altus, Urbanation, CMHC microdata) are not assumed.

## C1 — Tax-wedge elasticity of rental starts (GST/HST rental rebate)
- Question: how much do housing starts respond to a cut in the per-unit government tax wedge, and is the response net new supply or a shift from condo to rental tenure?
- Hypotheses: H40, H26, H35.
- Variation: federal GST rebate on purpose-built rental raised 36%→100% for construction begun after 13 Sep 2023. Provincial matching differs: Ontario, Nova Scotia, Newfoundland and Labrador matched the provincial HST share on the federal window; New Brunswick from mid-Nov 2024; PEI capped per unit; Quebec declined to enhance its 36% QST rebate; BC partial PST relief; Saskatchewan and Manitoba separate incentives. Details partly unverified.
- Design: tenure × province × time triple difference on starts; net-additionality test on total starts; possible Ottawa–Gatineau cross-border comparison.
- Data: CMHC starts by intended market (rental / condo / freehold) by CMA, monthly (open via CMHC portal); StatCan starts tables; rates; costs.
- Audited threats: few provincial clusters; concurrent MLI Select / ACLP financing; condo→rental relabelling at start; 2022-23 rate shock; no published causal evaluation found.

## C2 — Pipeline stage diagnostics and regime dependence
- Question: at which stage does permitted housing stop converting into starts and completions, by CMA and structure type, and did the binding stage shift from capacity (2021-22) to viability (2023-26)?
- Hypotheses: H41, H17, H34, H35, H36.
- Variation: 2022-23 rate shock × pre-shock exposure to presale-financed condos; construction vacancy/wage tightness.
- Design: start-hazard models of the permitted-unstarted stock by CMA × structure type; shift-share on exposure.
- Data: StatCan permits (CMA monthly), CMHC starts / under construction / completions, BCPI, job vacancies (province). Applications and approvals unobservable nationally; CMHC approved-not-started series began April 2026.
- Audited verdict: descriptive/diagnostic feasible; structural identification of "the binding stage" not feasible; only the viability arm can be causal.

## C3 — Upzoning switch-on / switch-off (Calgary, Edmonton)
- Question: does as-of-right upzoning raise infill permits, or mostly capitalize into land value?
- Hypotheses: H15, H16, H18, H24.
- Variation: Calgary citywide R-CG effective Aug 2024, partially repealed effective 4 Aug 2026; Edmonton bylaw effective 1 Jan 2024, Alberta order (Oct 2026) to revert within ~3 months.
- Design: within-city parcel DiD, newly upzoned vs already-permissive parcels; event-time around repeal.
- Data: Calgary and Edmonton open permit data; Calgary open parcel assessments (assessed, not transacted, values). Field-level schemas unverified.
- Audited threats: single cities; rush-to-vest; rezonings reclassified as development permits at reform date; already-permissive parcels are selected; short post-repeal window; feasibility-vs-permission not identifiable.

## C4 — Development-charge retiming
- Question: do temporary DC cuts and scheduled DC changes add starts or retime them?
- Hypotheses: H28, H26, H27.
- Variation: Bill 185 (6 Jun 2024); Mississauga/Peel cuts with 13 Nov 2026 sunset; Vaughan, Toronto, Hamilton cuts; federal-Ontario DC program from 30 Mar 2026; Metro Vancouver DCC increase (Jan 2025) and partial rollback (24 Jul 2026).
- Design: bunching and event study around known deadlines; border pairs.
- Data: CMHC starts by municipality (monthly, centres ≥10,000); municipal permit portals; DC rate panel must be hand-built from bylaws (FIR reports revenue, not rates). Monthly StatCan permits appear CMA-level only.
- Audited verdict: retiming feasible; long-run level effect not feasible (≤8 months post, GTHA controls vanish after Mar 2026, Bill 17 moved DC payment timing in 2025); incidence not feasible without paid land/price data.

## C5 — Student-cap / NPR exposure and rents
- Question: how much did the 2024 student cap and later NPR reductions lower rents, and what does that imply for the demand share of 2022-24 rent growth?
- Hypotheses: H02, H01.
- Variation: cap announced 22 Jan 2024, allocated by province; CMA exposure from pre-cap student/NPR shares.
- Design: exposure dose-response event study with completions control and placebo periods.
- Data: StatCan quarterly asking rents by CMA (46-10-0092-01, 2019Q1+); NPR components by CMA (17-10-0149-01, annual); CMHC Rental Market Survey (annual). Current IRCC permit files are province-level only.
- Audited threats: confounded with record rental completions, rate cuts, weak labour market; exposure nearly collinear with province; 2-3 annual post observations; Toronto near-campus rents rose while city fell.

## C6 — Housing Accelerator Fund
- Question: did HAF agreements raise permits beyond what would have occurred?
- Hypotheses: H25.
- Variation: staggered agreements 2023-25; 544 applicants, ~178 round-1 agreements; refusers of four-units conditions lost funds (Red Deer, Oakville, Tecumseh; Windsor rejected).
- Design: staggered DiD among applicants; accepters vs refusers.
- Data: CMHC HAF rounds data; permits (CSD annual; municipal portals).
- Audited threats: selection on ambition and politics; reforms pre-dated agreements; permits are the paid metric; overlapping provincial laws; scores not public.
