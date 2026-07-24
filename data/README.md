# Processed behavioral data

`reaction_time_trials.parquet` is the processed behavioral table used by both notebooks. It contains 89,931 selected trials from 459 International Brain Laboratory Brain-Wide Map sessions and 139 mice. Of these, 89,871 trials pass the reaction-time validity rule.

## Provenance

The analysis notebook combines the behavioral trial index from the public Brain-Wide Map sample-data archive with stimulus-onset and first-movement timestamps obtained through the public IBL ONE/OpenAlyx service. Trial sequences are validated before timestamps are attached.

- [IBL Brain-Wide Map Open Data Registry](https://registry.opendata.aws/ibl-brain-wide-map/)
- [IBL public data portal](https://int-brain-lab.github.io/iblenv/public_data/public_data.html)
- [Brain-Wide Map paper](https://doi.org/10.1038/s41586-025-09235-0)
- [Prior-information paper](https://doi.org/10.1038/s41586-025-09226-1)

The source Brain-Wide Map dataset is provided under CC BY 4.0. Credit belongs to the International Brain Laboratory and the contributing laboratories.

## Selection and derived fields

Rows are retained when they have:

- absolute contrast of 0, 0.0625, or 0.125;
- a biased block prior (`probabilityLeft` of 0.2 or 0.8);
- a completed left or right choice; and
- sufficient information to classify the choice as prior-congruent or prior-incongruent.

Reaction time is `firstMovement_times - stimOn_times`. `valid_rt` is true when this value is greater than 0 and no greater than 2 seconds.

The table includes session and subject identifiers, block information, stimulus and choice fields, congruency, source timestamps, reaction time in seconds and milliseconds, validity, and the trial-alignment method. It does not contain local file paths or access credentials.

`download_status.csv` records whether each of the 459 source sessions completed validation and how its trials were aligned.

## Integrity

SHA-256 checksums:

```text
1d6f752c4d53fbdf1a9d32b71bb239b1ea1fccf0de11361d633113fe0ffc0eed  reaction_time_trials.parquet
ee308b35d3e8ad1352dac901c0c7f71007175c9eff7731eda115f82dbcaa2606  download_status.csv
```

The notebooks also assert row counts, session and mouse counts, reaction-time reconstruction, contrast values, pairing coverage, and the published numerical results.
