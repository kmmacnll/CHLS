# CHLS

Research repository for the CHLS project: hypotheses, literature, data, models, causal analysis, simulation, and policy design.

## Layout

| Path | Purpose |
|------|---------|
| `research/` | Living research docs (hypotheses, literature, datasets, methodology, experiments, findings, policy design) |
| `data/raw/` | Immutable source data as received (not edited by code) |
| `data/processed/` | Cleaned / derived datasets produced by `src/preprocessing` |
| `data/metadata/` | Data dictionaries, provenance, licenses, schemas |
| `src/ingestion/` | Loaders and downloaders for raw sources |
| `src/preprocessing/` | Cleaning, feature construction, harmonisation |
| `src/models/` | Predictive / statistical models |
| `src/causal/` | Causal inference (identification, estimation, robustness) |
| `src/simulation/` | Simulation and counterfactual policy models |
| `src/evaluation/` | Metrics, validation, diagnostics |
| `experiments/` | One folder per experiment: config, run script, results pointer |
| `notebooks/` | Exploratory analysis (`NN_topic_initials.ipynb`) |
| `reports/` | Written deliverables (memos, papers, briefs) |
| `outputs/` | Generated figures, tables, model artefacts (reproducible, git-ignored by default) |

## Workflow

1. Record a hypothesis in `research/hypotheses.md`.
2. Log sources in `research/literature.md` and `research/datasets.md`.
3. Fix the approach in `research/methodology.md` before running.
4. Run an experiment under `experiments/`, log it in `research/experiments.md`.
5. Record results in `research/findings.md`; translate to `research/policy_design.md`.

## Conventions

- Raw data is never modified; every processed file must be reproducible from `src/`.
- Each hypothesis, dataset, and experiment has a stable ID (`H1`, `D1`, `E1`) used across docs.
- See `CLAUDE.md` for assistant guidance.
