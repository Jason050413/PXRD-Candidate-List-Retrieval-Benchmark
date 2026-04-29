# Dataset Summary

## Overview

This release contains the source files for the PXRD generated-spectrum benchmark and real-spectrum application samples. It includes generated benchmark spectra, paired CIF files, minimal provenance records for the real experimental samples, and diagnostic examples for generated spectra.

## Dataset Counts

| Item | Count |
| --- | ---: |
| Generated benchmark spectra | 1,500 |
| Real experimental application samples | 304 |
| Diagnostic generated-spectrum examples | 21 |

The 21 diagnostic examples are selected from the 1,500 generated spectra.

## Real Spectrum Sources

| Source | Count |
| --- | ---: |
| RRUFF | 236 |
| opXRD | 68 |

Minimal provenance records for the real experimental application samples are provided in `application_samples/source_mapping.csv`.

## Included Files

- `benchmark/generated_spectra/`: 1,500 generated benchmark spectra, paired CIF files, and JSON metadata.
- `benchmark/example/`: diagnostic examples selected from the generated spectra, with spectrum files, paired CIF files, JSON metadata, and PNG visualizations.
- `application_samples/real_spectra/`: 304 real experimental application samples and paired CIF files.
- `application_samples/source_mapping.csv`: minimal source records for the 304 real experimental application samples.

## Release Boundary

This release only provides benchmark source files, application sample source files, and minimal provenance information. It does not include candidate-library manifests, retrieval results, model outputs, evaluation scripts, or experiment result tables.

Paths in `application_samples/source_mapping.csv` are relative to the `application_samples/` directory.
