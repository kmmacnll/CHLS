# CLAUDE.md

Guidance for Claude Code when working in this repository.

## Project

CHLS is a research project spanning hypotheses, data, modelling, causal inference, simulation, and policy design. (Fill in a one-paragraph project statement here.)

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
