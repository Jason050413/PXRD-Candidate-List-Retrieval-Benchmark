# PXRD Candidate List Retrieval Benchmark

This repository hosts a PXRD candidate list retrieval benchmark. The dataset contains query spectra, paired target structures, source mapping tables, a theoretical spectrum candidate-library manifest, and diagnostic examples for generated spectra.

## Dataset Composition

- 1,804 query spectra.
- 304 real experimental spectra from RRUFF and opXRD.
- 1,500 physically constrained generated spectra.
- 541,393 theoretical spectrum candidates in the candidate-library manifest.
- 21 diagnostic examples selected from the generated spectra.

## Repository Layout

```text
PXRD-Candidate-List-Retrieval-Benchmark/
|-- README.md
|-- CITATION.cff
|-- LICENSE
|-- NOTICE
|-- dataset_summary.json
|-- metadata.csv
|-- target_mapping.csv
|-- real_304_source_mapping.csv
|-- candidate_library_manifest.csv
|-- diagnostic_examples.csv
|-- real_spectra/
|   `-- <sample_name>/
|       |-- <sample_name>.xy
|       `-- <sample_name>.cif
`-- generated_spectra/
    |-- all_1500/
    |   `-- <sample_name>/
    |       |-- <sample_name>.xy
    |       |-- <sample_name>.cif
    |       `-- <sample_name>.json
    `-- diagnostic_examples_21/
        `-- <sample_name>/
            |-- <sample_name>.xy
            |-- <sample_name>.cif
            |-- <sample_name>.json
            `-- diagnostic PNG files
```

## Data Files

- `dataset_summary.json`: dataset counts, source composition, and release notes.
- `metadata.csv`: metadata for all query spectra, including source, formula, space group, file paths, angular range, intensity range, and subset labels.
- `target_mapping.csv`: query-to-target mapping table linking each query spectrum to its paired target CIF.
- `real_304_source_mapping.csv`: source mapping and curation information for the real experimental spectra.
- `candidate_library_manifest.csv`: candidate-library manifest with source database, source identifier, formula, space group, peak-table reference, peak range, and peak-count fields.
- `diagnostic_examples.csv`: index of the 21 generated-spectrum diagnostic examples.
- `real_spectra/`: real experimental query spectra and paired target CIF files.
- `generated_spectra/`: generated query spectra, paired target CIF files, JSON metadata, and diagnostic visualizations.

## Data Processing

The `.xy` files are two-column text files containing 2-theta in degrees and intensity. Generated spectra are sampled over 5-90 degrees with 8,501 points. Real spectra retain their processed benchmark profiles; their angular ranges are listed in `metadata.csv`.

The generated-spectrum JSON files include generation parameters, donor-template provenance, and quality descriptors used to document spectrum construction and diagnostic checking. The 21 diagnostic examples are also included as PNG visualizations.

## Notes on Data Reliability

The benchmark combines real experimental spectra and physically constrained generated spectra. Source identifiers, target mappings, and diagnostic metadata are provided to support traceability. The candidate-library manifest stores upstream CIF and peak-table references for source-record tracking.

## Usage and Citation

If you use this benchmark, cite the associated manuscript and this dataset release. Citation metadata are provided in `CITATION.cff`.

## License and Source Terms

Author-generated metadata and documentation are released under CC BY 4.0. Structures and spectra derived from COD, Materials Project, RRUFF, and opXRD remain subject to the terms and citation requirements of their original sources. See `NOTICE` for the third-party data notice.
