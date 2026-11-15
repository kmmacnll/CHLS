# P3 — Independent ranking of candidate research questions (methodologist)

2026-11-15. Independent of the lead agent; `research_decision.md` and any adversarial review not read. Inputs: `P3_candidates.md`, `P1_synthesis.md`, four P2 audits. 10 web searches (§5). Tags: [V] seen in a search summary this session (no full texts); [U] unverified or from memory.

## 1. Scores (1–5)

| Criterion | C1 GST rental rebate | C2 Pipeline stages | C3 Upzoning on/off | C4 DC retiming | C5 Student cap | C6 HAF |
|---|---|---|---|---|---|---|
| Policy importance | 4 prices the whole cost-subsidy lever class | 5 maps which bottleneck binds | 5 zoning central, reversals live | 4 $8.8B bet, only timing answerable | 3 sizes demand share; lever already pulled | 4 flagship programme |
| Testability | 4 surprise date, provincial dose, 3 years of starts | 3 descriptive only; "binding stage" untestable | 3 switch-on yes; switch-off window ~3 months | 3 bunching yes; 13 Nov 2026 sunset has no post data | 3 two or three annual post points | 2 paid metric is the outcome |
| Data quality | 4 CMHC intended-market starts, CMA monthly [V listing]; dose table partly [U] | 3 same outcomes plus permits; no entitlement stage; stock series 7 months | 2 schemas and historic parcel zoning [U]; assessed values | 2 rate panel hand-built; dates conflict; Bill 17 breaks permits | 3 asking rents fine; CMA exposure indirect | 3 annual CSD permits; scores not public |
| Novelty | 4 no evaluation found | 4 no decomposition published | 4 one conference paper, one industry DiD | 4 no Canadian design-based estimate | 4 none found | 4 none found |
| Causal identification | 3 dose DiD sound in form; few high-dose clusters | 2 flows are equilibrium outcomes; exposure confounded | 3 many parcels; selected controls, reclassification, vesting rush | 3 timing identified; level and incidence not | 2 exposure ≈ province; concurrent completions, rates | 2 selection on ambition and politics |
| ML suitability | 2 small panel; counterfactual forecasts only | 4 CMA×type×month hazards, clear baselines | 3 parcel take-up heterogeneity | 2 few events | 2 few units | 2 few units, annual |
| Scalability | 4 all provinces; high dose only ON/Atlantic | 5 national CMA panel | 2 two elastic Alberta cities | 2 GTHA and Metro Vancouver | 4 ~40 CMAs | 4 ~180 municipalities |
| Actionability | 4 transferable cost elasticity; net vs shifted supply | 3 says where, not what an intervention does | 3 take-up only | 3 informs temporary-vs-permanent design | 3 informs demand share, not supply policy | 3 weakly identified answer |
| **Total** | **29** | **29** | **25** | **23** | **24** | **24** |

Unverified-assumption penalty is included: C3 and C4 data scores (unread schemas, hand-built rate panel); C1 identification held at 3 (dose table unconfirmed).

## 2. Ranking and sensitivity

Unweighted: C1 = C2 (29) > C3 (25) > C5 = C6 (24) > C4 (23).

| Weighting | C1 | C2 | C3 | C4 | C5 | C6 |
|---|---|---|---|---|---|---|
| Causal identification ×2 | 32 | 31 | 28 | 26 | 26 | 26 |
| Priority order (testability ×2, identification ×2, data ×1.5, novelty and ML ×0.5) | 35 | 31.5 | 28.5 | 27 | 27.5 | 26.5 |
| Policy importance ×2 | 33 | 34 | 30 | 27 | 27 | 28 |
| ML suitability ×2 | 31 | 33 | 28 | 25 | 26 | 26 |

- C1 leads whenever identification or validity carries extra weight, which is the project's stated order. C2 leads if policy importance or ML is up-weighted.
- The C1/C2 order is fragile: one point off C1 (for example, data 4→3 if the dose table fails verification) puts C2 first unweighted.
- C3–C6 never reach the top two under any weighting tried. C3 is the best of the rest; its weakness is unverified treatment assignment and low transferability, not importance.
- C2's only causal arm (viability) is in substance C1: complements, not rivals.

## 3. Reformulation: C1′ (recommended)

**Question:** how much do multi-unit housing starts respond to a change in the per-unit government tax/charge wedge, and is the response net new supply, a tenure shift, or retiming?

- **Primary analysis (one identification strategy):** provincial-dose difference-in-differences event study on the purpose-built-rental sales-tax rebate, outcome rental and total multi-unit starts by CMA.
- **Secondary, same outcome data, confirmatory only:**
  1. Ontario full HST rebate on new owner-occupied homes, agreements 1 Apr 2026–31 Mar 2027 [V]: reverses the relative tenure wedge in one province and has a known sunset (reversal and retiming test).
  2. DC deadline bunching (C4's feasible part) as a municipal-level wedge shock.
  3. Ottawa–Gatineau pair as a case study.
- **Descriptive baseline:** C2 start-hazard tables by CMA × structure type; also the forecast baseline for any ML counterfactual.
- Rule: secondary analyses cannot rescue a failed primary.
- Scores as C1 except policy importance 5 (covers GST, HST and DC levers). Total 30; 33 with identification doubled.

## 4. Top choice: specification

**Estimand.** θ = average effect, over months 7–30 after 14 Sep 2023, on log purpose-built-rental starts (CMA × quarter) of one percentage point of *incremental provincial* reduction in the statutory sales-tax wedge on a new rental unit (percent of fair market value, net of pre-existing rebates), for CMAs in matching provinces relative to federal-only provinces. Companion estimands: θ_total (all multi-unit starts; net additionality) and θ_condo (substitution). Not identified: the federal 5-point component (common to all provinces) and MLI Select separately.

**Identifying assumptions.**
1. Parallel trends in dose: absent provincial matching, starts in matching and federal-only provinces evolve alike conditional on CMA and period effects and pre-specified controls. Testable on 2018–Aug 2023.
2. No anticipation before the announcement (rebate applied from the announcement date; provincial matches backdated). Check bunching.
3. No province-specific shock to rental viability correlated with dose: MLI Select/ACLP uptake, Ontario rental DC relief, Toronto condo collapse, Nova Scotia HST cut (Apr 2025), Manitoba credit. Weakest assumption.
4. No reallocation of capital or labour from control to treated provinces.
5. Dose measured correctly; intended-market classification stable.

Inference: province-level randomization inference and wild cluster bootstrap; synthetic DiD as robustness.

**Minimum data.**
- CMHC starts by intended market and dwelling type, CMA/large CA and province, monthly, 2018–Oct 2026.
- Dose table for 10 provinces (rate, pre-existing rebate, caps, dates) from CRA RC4231, GI notices and provincial statutes, read as primary text.
- Controls: BoC rates, pre-2022 condo share of starts, population (17-10-0148), BCPI.
- Gate before `methodology.md` is locked: (i) confirm series depth by download; (ii) verify the dose table; (iii) placebo-date power analysis on the pre-period. Proceed only if the minimum detectable effect for a ~10-point dose is ≤ ~25% of rental starts. If the gate fails, fall back to C2 as a descriptive study.

**Three most likely failures.**
1. **Power.** High dose rests on Nova Scotia and Newfoundland (two CMAs). Ontario's incremental provincial dose may be only ~2–4 points if its pre-existing 75%/$24,000-cap rental rebate is confirmed [U, memory]. Canadian supply elasticities of 0.3–2 (CMHC 2018, per P2) imply roughly 0.3–2% of starts per point: below noise in Ontario.
2. **Province-specific confounding of tenure mix.** Ontario's condo collapse pushes builders into rental regardless of the rebate, so a rental rise with a condo fall mimics the "tenure shift" result. The Ontario ownership rebate contaminates the condo arm from Apr 2026, so the primary window must end ~Mar 2026.
3. **Dose and label error.** "Control" provinces were treated: Manitoba $8,500/unit credit for permits from 1 Jan 2024 [V]; BC, New Brunswick and PEI status unclear. CMHC assigns intended market at start, so the rebate itself can move labels.

**Falsification criteria.**
- Abandon "the tax wedge materially constrains rental starts" (H40) if the 90% randomization interval for θ lies below 0.3% per point (under 3% for a 10-point dose). Count it supported only if the lower bound exceeds 0 with flat pre-trends and a null placebo.
- Abandon "net new supply" if θ_total's interval excludes one-third of the rental response and θ_condo is negative and offsetting: pure tenure shift.
- Report as inconclusive, not as a null, if: pre-trends reject jointly; estimates at placebo dates are as large as the actual one in more than 10% of draws; single-detached starts (ineligible) respond; or the gate fails.
- Reversal check: if Ontario's ownership share of starts does not rise after Apr 2026 relative to other provinces, and rental did not respond in 2023–26, the wedge is not what drives tenure mix.

## 5. Web checks (10 searches)

| # | Checked | Result |
|---|---|---|
| 1, 6 | Does a causal evaluation of the rental rebate exist? | None found. Urbanation–FRPO (Aug 2026) attributes the rental surge to several factors at once; one CMHC-based press item reports worsening builder sentiment despite the rebate [V]. |
| 2 | Provincial matching | CRA guide (rev. Nov 2025): 100% provincial rebate in NL, NS, ON only; Quebec does not intend to enhance QST rebate [V]. |
| 3, 8 | CMHC data | "Starts and Completions by Intended Market" tables exist for CMAs/large CAs and for provinces, monthly; a CSD starts table exists [V listing]. History depth and CSD × intended market [U]. |
| 4 | Calgary treatment assignment (C3) | Open development-permit data exist; "land use at time of application" appears only in a paid City Online report [V]. C3's key variable stays [U]. |
| 5, 9 | Other provinces | New Brunswick: intends rebate for starts from 15 Nov 2024, status unclear. Manitoba: credit as above. Saskatchewan: nothing rental-specific. BC: sources conflict. PEI: not found. |
| 7 | Ownership-side shocks | Ontario full HST rebate up to $1M, Apr 2026–Mar 2027 (Osler, PwC); federal first-time-buyer GST rebate law Mar 2026, effective date conflicting [V]. |
| 10 | Ottawa–Gatineau | Gatineau totals reported; no tenure split found [U]. |

## Summary
- Claims (each with confidence):
  - C1 and C2 tie unweighted (29); C1 leads when identification or validity is up-weighted, C2 when policy importance or ML is (high on arithmetic, medium on scores).
  - C3–C6 do not reach the top two under any weighting tried (medium-high).
  - C1′ (tax/charge-wedge elasticity; rental-rebate dose DiD primary; Ontario ownership rebate, DC bunching and C2 hazards secondary) weakly dominates C1 (medium).
  - The main risk to C1′ is power: few high-dose provinces and a possibly small Ontario dose (medium; dose table unverified).
  - No causal evaluation of the rental rebate was found (medium; two searches).
- Supporting evidence: P2 audits; §5 checks.
- Sources: canada.ca CRA PBRH rebate pages, RC4231, memorandum 19-3-9; bdo.ca/insights/gst-relief-announced-for-new-residential-rental-properties; osler.com/en/insights/updates/ontarios-new-hst-rebate-key-details; pwc.com/ca enhanced-hst-relief-sale-new-homes-ontario-2026; cmhc-schl.gc.ca data-tables/housing-market-data; calgary.ca/info-requests/property-details.html; cityonline.calgary.ca development-permit-status; mltaikins.com (Manitoba credit); frpo.org Urbanation–FRPO Aug 2026 update.
- Uncertainty: all checks are search summaries; series depth, Ontario's pre-existing rebate, NB/PEI/BC measures and announcement dates are unverified; scores carry roughly ±1 error.
- Assumptions: CMHC intended-market series extend back to at least 2018 at CMA level; statutory dose can be computed from public texts.
- Contradictions found: `P3_candidates.md` lists New Brunswick as matching from mid-Nov 2024, but the CRA guide lists only NL, NS, ON; Manitoba is a treated "control"; BC PST relief sources conflict.
- Recommended next investigations: run the three-part gate in §4 (series download, dose table from primary texts, placebo power analysis) before locking the question; if it fails, adopt C2 as a descriptive study.
