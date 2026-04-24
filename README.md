# PXRD Candidate List Retrieval Benchmark

This repository provides a benchmark dataset for powder X-ray diffraction (PXRD) candidate list retrieval. It contains query spectra, paired target structures, source mapping tables, a theoretical spectrum candidate-library manifest, and diagnostic examples for generated spectra.

## Dataset

- 1,804 query spectra.
- 304 real experimental spectra from RRUFF and opXRD.
- 1,500 physically constrained generated spectra.
- 541,393 theoretical spectrum candidates in the theoretical spectrum candidate library.
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

## File Description

- `dataset_summary.json`: dataset counts, source composition, and release notes.
- `metadata.csv`: query-level metadata for all 1,804 spectra, including source, formula, space group, spectrum path, target path, angular range, intensity range, and subset flags.
- `target_mapping.csv`: query-to-target mapping table linking each query spectrum to its paired target CIF.
- `real_304_source_mapping.csv`: source and curation table for the 304 real experimental spectra.
- `candidate_library_manifest.csv`: manifest of the 541,393 theoretical spectrum candidates, including source database, source identifier, formula, space group, peak-table reference, peak range, and peak-count fields.
- `diagnostic_examples.csv`: index of the 21 generated-spectrum diagnostic examples.
- `real_spectra/`: real experimental query spectra and paired target CIF files.
- `generated_spectra/all_1500/`: generated query spectra, paired target CIF files, and JSON metadata.
- `generated_spectra/diagnostic_examples_21/`: diagnostic subset with spectra, paired target structures, JSON metadata, and PNG visualizations.

## Data Format

The `.xy` files are two-column text files containing 2-theta in degrees and intensity. Each real-spectrum folder contains one `.xy` file and one paired `.cif` file. Each generated-spectrum folder contains one `.xy` file, one paired `.cif` file, and one `.json` metadata file.

Generated spectra are sampled over 5-90 degrees with 8,501 points. Real spectra retain their processed benchmark profiles; their 2-theta ranges are listed in `metadata.csv`.

The generated-spectrum JSON files record spectrum-construction metadata, including generation parameters, donor-template provenance, and generated-spectrum quality descriptors. These fields document how the generated spectra were built and checked.

The real-spectrum curation table records source identifiers and profile-quality descriptors used during benchmark assembly. The candidate manifest records source references for candidate CIF records and peak-table records. These references identify upstream candidate-library records and are not file paths within this repository.

## Citation

If you use this benchmark, cite the associated manuscript and this dataset release. Citation metadata are provided in `CITATION.cff`.

## License and Source Terms

Author-generated metadata and documentation are released under CC BY 4.0. Structures and spectra derived from COD, Materials Project, RRUFF, and opXRD remain subject to the terms, licenses, and citation requirements of their original sources. See `NOTICE` for the third-party data notice.
