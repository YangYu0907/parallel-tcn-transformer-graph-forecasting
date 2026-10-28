# Parallel TCN–Transformer graph forecasting

Data and code for **A parallel TCN–Transformer framework with adaptive graph learning for multi-location electricity price forecasting**.

## Download the data and code

Download [Supplementary Software S1 (version 1.0.0)](Supplementary_Software_S1_Parallel_TCN_Transformer_Graph_v1.0.0.zip) and extract it. The archive preserves the directory structure and contains the model implementation, recorded training/evaluation workflows, processed result data, plotting scripts and reproduction instructions.

The archive checksum is provided in [SHA256SUMS.txt](SHA256SUMS.txt). Each packaged file also has a SHA-256 entry in the archive's `FILE_MANIFEST.json`.

## Run the verification and reproduce result figures

After extraction, open the `parallel-tcn-transformer-graph-forecasting` directory and run with Python 3.10 or later:

```bash
python -m pip install -r requirements-analysis.txt
python scripts/check_package.py
python tests/test_scientific_components.py
python scripts/reproduce_result_figures.py
```

These commands verify the processed research results and regenerate numerical figures; they do not retrain models. Full model fitting requires the admitted raw input archive and the documented workflow/environment mappings. See `docs/REPRODUCTION_LEVELS.md` inside the archive.

## Contents

| Directory inside the archive | Contents |
| --- | --- |
| `src/electricity_forecasting/` | Parallel TCN–Transformer backbone, adaptive graph aggregation, loss functions, point decisions and evaluation |
| `archived_workflows/` | Recorded training, baselines, risk selection, quantile calibration and chronological replay |
| `configs/` | Experiment configuration and optimization protocol |
| `data/processed/` | All 15 manuscript tables, numerical figure data and editable architecture illustration |
| `data/manifests/` | Data-source, publication-time and manuscript provenance records |
| `results/` | Frozen experimental summaries and optimization receipts |
| `scripts/` and `tests/` | Figure reproduction, integrity checks and scientific arithmetic tests |
| `docs/` | Data access, reproduction instructions and attribution |

## Source data

Processed results are distributed in the archive. The original source-data access points are [CAISO OASIS](https://oasis.caiso.com/), the [European electricity-price benchmark](https://doi.org/10.5281/zenodo.4624805) and the [EPF toolbox](https://github.com/jeslago/epftoolbox). Publication-time admission requirements and historical-vintage provenance are documented in `docs/DATA_ACCESS.md` and the source manifests. Large raw training arrays and fitted checkpoints are not included in this compact archive.

## Citation and rights

Cite the associated manuscript and Supplementary Software S1, version 1.0.0. A software citation template is included as `CITATION.bib`; no DOI or author list has been invented. The authors retain software rights unless a license is explicitly added. Source datasets and third-party dependencies retain their own terms.
