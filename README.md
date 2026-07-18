# Reaction time and prior-choice congruency

This repository contains one complete notebook for the behavioral reaction-time analysis of the International Brain Laboratory Brain-Wide Map release.

The question is whether choices that agree with the block prior begin earlier than choices that oppose it, at 0%, 6.25%, and 12.5% visual contrast.

## Run the project

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
jupyter lab notebooks/reaction_time_analysis.ipynb
```

Run the notebook from top to bottom. The committed processed data allow an immediate offline analysis. Set `REFRESH_DATA = True` only when you intentionally want to fetch and validate the 459 source sessions again.

## Analysis levels

1. One session from mouse `CSH_ZAD_029`.
2. All seven sessions from that mouse.
3. The same all-session summary for every mouse.
4. All 139 mice and 459 sessions, with mice weighted equally.

Reaction time is `first movement - stimulus onset`. A positive `incongruent - congruent` difference means that prior-incongruent choices began later, supporting the hypothesis.

The primary analysis includes all completed choices. The notebook keeps a disabled `CORRECT_ONLY` switch for a future correct-trial sensitivity analysis.
