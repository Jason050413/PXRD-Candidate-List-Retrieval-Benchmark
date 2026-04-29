# PXRD Candidate List Retrieval Benchmark

This repository hosts the source files for a PXRD generated-spectrum benchmark and real-spectrum application samples. The release contains only spectra, paired structure files, minimal provenance records, and diagnostic examples for generated spectra. Retrieval results, model outputs, evaluation scripts, experiment result tables, and candidate-library manifests are not included.

## Dataset Composition

- 1,500 physically constrained generated benchmark spectra.
- 304 real experimental application samples from RRUFF and opXRD.
- 21 diagnostic examples selected from the generated spectra.

## Repository Layout

```text
PXRD-Candidate-List-Retrieval-Benchmark/
|-- README.md
|-- CITATION.cff
|-- LICENSE
|-- NOTICE
|-- DATASET_SUMMARY.md
|-- benchmark/
|   |-- generated_spectra/
|   |   `-- <sample_name>/
|   |       |-- <sample_name>.xy
|   |       |-- <sample_name>.cif
|   |       `-- <sample_name>.json
|   `-- example/
|       `-- <sample_name>/
|           |-- <sample_name>.xy
|           |-- <sample_name>.cif
|           |-- <sample_name>.json
|           `-- diagnostic PNG files
`-- application_samples/
    |-- source_mapping.csv
    `-- real_spectra/
        `-- <sample_name>/
            |-- <sample_name>.xy
            `-- <sample_name>.cif
```

## Data Files

- `DATASET_SUMMARY.md`: readable dataset counts, source composition, and release boundary.
- `benchmark/generated_spectra/`: 1,500 generated benchmark spectra, paired CIF files, and JSON metadata.
- `benchmark/example/`: 21 diagnostic examples selected from the generated spectra.
- `application_samples/real_spectra/`: 304 real experimental application samples and paired CIF files.
- `application_samples/source_mapping.csv`: minimal source records for the 304 real experimental application samples.

## Data Processing

The `.xy` files are two-column text files containing 2-theta in degrees and intensity. Generated spectra are sampled over 5-90 degrees with 8,501 points. Each spectrum folder contains the paired CIF file with the same sample name. Paths in `application_samples/source_mapping.csv` are relative to the `application_samples/` directory.

The generated-spectrum JSON files include generation parameters, donor-template provenance, and quality descriptors used to document spectrum construction and diagnostic checking. The 21 diagnostic examples also include PNG visualizations for direct inspection.

## Notes on Data Reliability

The generated-spectrum benchmark and the real-spectrum application samples are separated into different top-level folders to avoid mixing benchmark source files with application samples. Source identifiers for the real experimental spectra and diagnostic metadata for the generated examples are provided to support traceability.

## Usage and Citation

If you use this benchmark, cite the associated manuscript and this dataset release. Citation metadata are provided in `CITATION.cff`.

## License and Source Terms

Author-generated metadata and documentation are released under CC BY 4.0. Structures and spectra derived from COD, Materials Project, RRUFF, and opXRD remain subject to the terms and citation requirements of their original sources. See `NOTICE` for the third-party data notice.
