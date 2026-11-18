[![DOI](https://img.shields.io/badge/DOI-10.82901%2Fnemar.on006377-blue)](https://doi.org/10.82901/nemar.on006377)

<!-- nemar:provenance -->
## Provenance

This dataset is mirrored on NEMAR from OpenNeuro.

- Source: [ds006377](https://openneuro.org/datasets/ds006377)
- DOI: [10.18112/openneuro.ds006377.v1.0.2](https://doi.org/10.18112/openneuro.ds006377.v1.0.2)

## Known issues

Checked in the files of version 1.0.2; the source of each item is given with it.

- The subject-level `sub-<label>_optodes.tsv` / `coordsystem.json` do not describe both hemisphere-specific probes
  (LH and RH runs use different probes); the positions in each recording's SNIRF `/nirs/probe` are the reference.
  Example: the `/nirs/probe` source positions of `sub-277_task-003RestingLH_run-2_nirs.snirf` differ from
  `sub-277_optodes.tsv` by up to 172 mm, while those of `sub-390_task-002RestingRH_run-1_nirs.snirf` equal
  `sub-390_optodes.tsv`.
- `sub-236` tasks 003RestingLH and 004RestingRH (run-2) have all-zero placeholder events tables (one row
  `0 0 0 0`; source: the two events.tsv files).
- The associated paper describes two NIRSport2 systems with 16 dual-tip sources and 16 dual-tip detectors in total
  (doi:10.1038/s41562-025-02274-7; text checked in its CC-BY preprint doi:10.1101/2024.10.28.620644, section 2.2
  "fNIRS Measurements"); each recording holds the 8 sources of one hemisphere probe (NIRSSourceOptodeCount 8 in all
  690 `*_nirs.json` files).
