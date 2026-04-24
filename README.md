# PXRD Candidate List Retrieval Benchmark

This repository provides a benchmark dataset for powder X-ray diffraction (PXRD) candidate list retrieval.

## Dataset

- 1,804 query spectra.
- 304 real experimental spectra from RRUFF and opXRD.
- 1,500 physically constrained generated spectra.
- 541,393 theoretical spectrum candidates in the theoretical spectrum candidate library.

This release contains benchmark inputs, target mappings, source information and diagnostic examples.

## Files

- `dataset_summary.json`: dataset counts and source composition.
- `metadata.csv`: metadata for all 1,804 query spectra.
- `target_mapping.csv`: query-to-target mapping.
- `real_304_source_mapping.csv`: source mapping for the 304 real spectra.
- `candidate_library_manifest.csv`: manifest of the theoretical spectrum candidate library.
- `diagnostic_examples.csv`: index of the 21 diagnostic examples.
- `real_spectra/`: real spectra and paired target structures.
- `generated_spectra/`: generated spectra, paired target structures and metadata.

The 21 diagnostic examples are a subset of the 1,500 generated spectra. Their PNG files are retained as visual diagnostic aids.

## File Format

The `.xy` files are two-column text files containing 2-theta in degrees and intensity. Each real-spectrum folder contains one `.xy` file and one paired `.cif` file. Each generated-spectrum folder contains one `.xy` file, one paired `.cif` file and one `.json` metadata file.

Generated spectra are sampled over 5-90 degrees with 8,501 points. Real spectra retain their processed benchmark profiles; their 2-theta ranges are listed in `metadata.csv`.

The candidate manifest includes source references for candidate CIF records and peak-table records. These references identify the upstream candidate-library records and are not file paths within this repository.

## License

Author-generated metadata and documentation are released under CC BY 4.0. Third-party data terms are summarized in `NOTICE`.

## Citation

If you use this benchmark, cite the associated manuscript and this dataset release. Citation metadata are provided in `CITATION.cff`.
