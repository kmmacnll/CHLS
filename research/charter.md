# Project CHLS — Charter

**Canadian Housing Laboratory System.** Interdisciplinary ML + economic research on Canada's housing crisis. This file records the project mandate and operating method as set by the project owner (2026-11-14). It is the reference for all agents. Do not edit without owner instruction.

## Objective

Not a conventional house-price prediction model. Identify the structural mechanisms that materially constrain housing affordability, availability, and production in Canada; determine which are empirically important; use the findings to construct an evidence-based, implementable policy/system solution.

The final product must answer:

> What are the most important bottlenecks preventing Canada from producing sufficient housing at affordable prices, how large are their effects, and what combination of interventions is most likely to improve outcomes over the next 5–15 years?

## Research principles

1. Prefer discovering what is true over confirming the initial hypothesis.
2. Treat the housing crisis as a system, not a single-variable prediction problem.
3. Distinguish correlation, prediction, and causal inference.
4. No causal claim without an appropriate identification strategy.
5. Prefer Canadian evidence; use international comparisons where they provide useful variation or policy evidence.
6. Explicitly identify uncertainty, missing data, measurement problems, competing explanations.
7. Reject research questions already substantially solved unless a meaningful extension exists.
8. Do not optimize for model complexity; a simple model with a strong result beats unnecessary deep learning.
9. Never fabricate data, sources, statistics, or findings.
10. Every major empirical claim must be traceable to a dataset, paper, government source, or experiment.

## Multi-agent STORM architecture

The Lead Research Agent (Principal Investigator) decomposes questions, delegates separable tasks to specialists, and synthesizes. Do not run the whole investigation from one perspective when independent analysis helps.

### Specialist agents

| # | Role | Scope |
|---|------|-------|
| 1 | Housing economist | supply/demand, rents, prices, elasticity, household formation, population growth, interest rates, development and land economics |
| 2 | Urban / planning researcher | zoning, density, land-use regulation, permitting, municipal planning, approvals, urban form, geographic constraints |
| 3 | Developer / construction economist | land acquisition, construction costs, labour, materials, financing, timelines, project failure, productivity, development charges |
| 4 | Public finance / governance researcher | municipal incentives, property tax, infrastructure financing, development charges, provincial/federal responsibilities, fiscal constraints, institutional incentives |
| 5 | Data / ML researcher | datasets, features, spatial and temporal structure, predictive models, data quality, missingness, leakage, ML opportunities |
| 6 | Causal inference researcher | identification, natural experiments, panel designs, DiD, IV, synthetic control, endogeneity, confounding, causal ML |
| 7 | International comparative researcher | Japan, Germany, Austria, Switzerland, Netherlands, Finland, Sweden, Singapore, Australia, New Zealand, United States — policies providing useful empirical variation, not just better-affordability lists |
| 8 | Adversarial reviewer | tries to disprove leading hypotheses: contradictory evidence, alternative explanations, failed policies, methodological weaknesses, reverse causality, omitted variables, selection bias, ecological fallacies, measurement problems, dissenting studies |

### STORM research loop (per major question)

1. **Decompose** into independent tasks.
2. **Delegate** to appropriate specialists.
3. **Investigate** independently.
4. **Record** concise findings: claims, supporting evidence, sources, uncertainty, assumptions, contradictions, recommended next investigations.
5. **Cross-examine**: do not accept conclusions immediately; identify disagreements between specialists.
6. **Adversarial review** of the strongest conclusions.
7. **Synthesize** (Lead Agent).
8. **Update** hypotheses.
9. **Rank** by empirical support, causal credibility, novelty, data feasibility, policy importance.
10. **Decide** the strongest surviving direction.

Repeat when new evidence materially changes the question.

### Agent independence

- For competing explanations, run independent investigations before exposing agents to each other's conclusions.
- Do not let the initial hypothesis anchor every specialist.
- For important disputed questions, obtain at least two independent analyses before synthesis.
- Preserve disagreement; no artificial consensus.
- The Lead Agent explicitly records: consensus, disagreement, unresolved uncertainty, evidence favouring each position.

### Cost control

Delegate when: questions are independent; different expertise helps; parallelism materially saves time; independent opinions reduce confirmation bias; adversarial review improves reliability.

Work directly for: simple file operations, minor code changes, formatting, straightforward calculations, tightly coupled reasoning chains, steps needing the immediately preceding context.

Prefer a few high-quality investigations over many redundant agents. Use lower-cost models for routine research/execution. Reserve the top model at high effort for: research direction, synthesis, difficult methodological decisions, causal inference, model architecture, adversarial review, final conclusions.

### Shared research state

- `research/agent_findings/` — one file per major investigation (protocol in its README).
- `research/synthesis/` — Lead Agent synthesis.
- `research/decisions.md` — major research decisions and rejected approaches.
- `research/research_log.md` — concise chronological log.
- Inspect existing artifacts before any new major investigation. Do not duplicate investigations. The repository is the shared source of truth.

## Phases

| Phase | Name | Required artifact(s) |
|-------|------|----------------------|
| 1 | Hypothesis discovery | `research/hypotheses.md` — 30–50 hypotheses, each with mechanism, predicted effect, unit of analysis, required variables, potential datasets, existing literature, likely identification strategy, expected difficulty, novelty, policy importance; classified A already well established / B partially understood / C contested / D under-researched / E potentially novel. No expensive modelling. |
| 2 | Literature and data audit | `research/literature.md`, `research/datasets.md` — for the strongest hypotheses: academic literature; CMHC, StatCan, Bank of Canada, Infrastructure Canada, provincial, municipal evidence; existing estimates; disagreements; datasets per hypothesis; geographic/temporal coverage; missing variables and measurement problems; leakage and endogeneity; whether variation suffices for inference. |
| 3 | Research selection | `research/research_decision.md` — rank by policy importance, testability, data quality, novelty, causal identification potential, ML suitability, scalability across regions, actionability. Select the single strongest question. Contents: selected hypothesis; rejected alternatives; supporting evidence; datasets; methodology; expected contribution; major risks; falsification criteria. **STOP after this phase unless explicitly instructed to continue.** |
| 4 | Empirical system | Strongest available Canadian dataset (panel preferred, geographic × temporal). Document variable definitions, transformations, missing values, outliers, geographic changes, sources, preprocessing decisions, leakage risks. Reproducible ingestion and preprocessing pipelines. |
| 5 | Baselines | Descriptives, fixed effects, linear, regularized regression, tree-based, spatial, time-series as appropriate. Purpose: determine whether advanced ML adds information. |
| 6 | Advanced ML | Only where justified: gradient boosting, random forests, neural nets, spatial ML, temporal models, graph approaches, causal ML, heterogeneous treatment effects, clustering/regime detection, simulation. Compare out-of-sample with economic/statistical metrics; not accuracy alone. |
| 7 | Causal and robustness analysis | For every mechanism separate prediction / association / causal effect. Natural experiments, DiD, event studies, IV, RD, panel FE, synthetic control, causal forests, placebo tests, negative controls, geographic and temporal holdouts, sensitivity analysis. State weak identification explicitly. |
| 8 | Housing system simulation | Pipeline model LAND → ZONING → APPROVAL → INFRASTRUCTURE → FINANCING → CONSTRUCTION → OCCUPANCY; where delays, costs, failure probabilities accumulate. Counterfactuals (faster approvals, density, lower development charges, infrastructure, productivity, financing, public/private expansion, alternative zoning, combinations). Effects on starts, completion rates, supply, rents, ownership affordability, construction costs, municipal costs, household costs, time to completion. State all assumptions. |
| 9 | Policy optimization | Smallest/most practical intervention set with largest improvement under realistic constraints: fiscal cost, political feasibility, implementation time, distributional effects, municipal incentives, jurisdiction, infrastructure, unintended consequences. Multiple scenarios; forecasts for 2027, 2030, 2033, 2036, 2040 with uncertainty intervals where justified. |
| 10 | Validation | Alternative specifications, datasets, geographic definitions, time periods; placebo tests; leakage checks; missingness; outlier sensitivity; simple-baseline comparison; independent replication. If a result fails, revise the hypothesis. |
| 11 | Final research output | Paper-quality report; executive summary; methodology; data dictionary; reproducible code; model results; robustness results; policy simulation; limitations; replication instructions; figures and tables; policy recommendations. Clearly separate established facts, empirical findings, model predictions, causal estimates, assumptions, speculative scenarios. |

Hypothesis-discovery mechanisms to consider: zoning and land-use regulation; approval processes; development charges; municipal finance; infrastructure capacity; transportation; construction productivity; labour shortages; materials; financing costs; interest rates; development finance; land speculation; investor behaviour; household formation; immigration; population growth; rental markets; ownership markets; social housing; public housing; construction technology; developer concentration; permitting delays; municipal incentives; provincial/federal policy; geographic constraints; housing type; density; land assembly; vacant/underutilized land; adaptive reuse; regional migration; interprovincial migration.

## Operating rules

- Work autonomously within the current phase; no repeated permission requests for routine research, coding, cleaning, experimentation.
- Do not start the next major phase until the current one has produced its required artifact.
- Maintain a research log. Record important decisions and rejected approaches.
- Prefer concise research artifacts over long conversational explanations.
- When uncertainty is high, investigate rather than speculate.
- When evidence contradicts the working hypothesis, update the hypothesis.
- Never fabricate evidence.
- Build everything so another researcher can reproduce the analysis from the repository.

The goal is not an impressive-looking AI project. The goal is to determine, as rigorously as possible, what is actually constraining Canadian housing production and affordability and which interventions have the strongest evidence.
