# CLAUDE.md

Guidance for Claude Code when working in this repository.

## CHLS PROJECT INSTRUCTIONS

Project CHLS is a serious research project investigating structural causes of Canada's housing affordability and supply problems.

Priorities, in order:

1. Empirical validity
2. Reproducibility
3. Causal identification
4. Data quality
5. Policy usefulness
6. Predictive performance
7. Model sophistication

Never fabricate evidence.
Do not assume the initial hypothesis is correct.
Distinguish prediction, correlation, and causation.
Do not build complex ML models before establishing strong statistical baselines.
Maintain research artifacts in `/research`.
Maintain reproducible code in `/src`.
Document datasets and transformations.
Record major decisions and rejected approaches.
Do not overwrite previous experimental results.
Use concise research logs rather than lengthy conversational explanations.
Before starting a major new phase, inspect the existing research artifacts and determine what has already been established.
The repository is the source of truth for the project.

---

## Project Scope

The project spans hypotheses, data, modelling, causal inference, simulation, and policy design.

## Structure

See `README.md` for the directory map. Research reasoning lives in `research/*.md`; code in `src/`; runs in `experiments/`.

## Rules

- **Never modify `data/raw/`.** Derived data goes to `data/processed/` via code in `src/preprocessing/`.
- **Do not commit large data or outputs.** Document them in `data/metadata/` instead.
- **Cross-reference by ID:** hypotheses `H#`, datasets `D#`, experiments `E#`, findings `F#`.
- **Pre-specify before running:** update `research/methodology.md` before a new experiment; log it in `research/experiments.md` after.
- **Report honestly:** record null and negative results in `research/findings.md` with the same care as positive ones. Separate correlation from causal claims and state identifying assumptions.
- **Reproducibility:** set random seeds, record package versions and data versions in each experiment's config.
- **No fabricated citations or numbers.** Mark unverified items `[unverified]`.

## Code conventions

- Python; modules under `src/` are importable packages (`from src.causal import ...`).
- Each experiment folder: `config.yaml`, `run.py`, `README.md`.
- Notebooks are for exploration only; promote reusable logic into `src/`.

## Commands

(Add setup, test, and run commands here once the toolchain is chosen.)
