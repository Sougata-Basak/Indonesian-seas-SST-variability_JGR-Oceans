# Monsoonal Wind-Driven Ocean Dynamics Drive Seasonal Sea Surface Temperature Variability in the Indonesian Seas

Code accompanying the paper:

> **Basak, S., Nikurashin, M., Peña-Molino, B., Sloyan, B. M., Phillips, H.** "Monsoonal wind-driven ocean dynamics drive seasonal sea surface temperature variability in the Indonesian seas." *Journal/Venue*, Year. [DOI or arXiv link]

## Overview

Brief description of what this repository contains and what the paper is about.

## Repository structure

```
.
├── data/               # processed data to run the scripts
├── scripts/            # analysis notebooks used to generate figures/tables
├── figures/            # generated figures
├── environment.yml     # conda environment specification
└── README.md
```

## Installation

```bash
git clone https://github.com/Sougata-Basak/Indonesian-seas-SST-variability_JGR-Oceans.git
cd Indonesian-seas-SST-variability_JGR-Oceans
conda env create -f environment.yml
conda activate <env-name>
```

Or with pip:
```bash
pip install -r requirements.txt
```

## Data files

All processed data required to reproduce the paper's figures and tables are provided in `data/`:

| File | Description |
|---|---|
| `sst_mean_REMSS-MWIR.nc` | Mean SST, REMSS MW+IR satellite product |
| `sst_variance_REMSS-MWIR.nc` | Power spectral density / variance decomposition of SST, REMSS MW+IR satellite product |
| `argo1_5903451.nc` | Argo float profiles, Makassar Strait route |
| `argo2_6901746.nc` | Argo float profiles, Banda Sea |
| `sst_MITgcm-RYF_cntl.nc` | Mean and standard deviation of SST, `MITgcm-RYF` Control experiment |
| `sst_MITgcm-RYF_nowind.nc` | Mean and standard deviation of SST, `MITgcm-RYF` No-wind experiment |
| `temp_profiles_MITgcm-RYF_cntl.nc` | Vertical profiles of mean and standard deviation of temperature, `MITgcm-RYF` Control experiment |
| `mld_summary_IndonesianSeas_MITgcm-RYF_cntl.csv` | Mean and standard deviation of mixed layer depth, Indonesian Seas, `MITgcm-RYF` Control experiment |
| `budget_mean_integrated_MITgcm-RYF_cntl.nc` | Upper 100 m integrated mean heat budget, `MITgcm-RYF` Control experiment |
| `budget_variance_integrated_MITgcm-RYF_cntl.nc` | Upper 100 m integrated temperature variance budget, `MITgcm-RYF` Control experiment |
| `budget_variance_profiles_MITgcm-RYF_cntl.nc` | Vertical profiles of the temperature variance budget, `MITgcm-RYF` Control experiment |
| `budget_mean_integrated_MITgcm-RYF_nowind.nc` | Upper 100 m integrated mean heat budget, `MITgcm-RYF` No-wind experiment |
| `budget_variance_integrated_MITgcm-RYF_nowind.nc` | Upper 100 m integrated temperature variance budget, `MITgcm-RYF` No-wind experiment |
| `budget_variance_profiles_MITgcm-RYF_nowind.nc` | Vertical profiles of the temperature variance budget, `MITgcm-RYF` No-wind experiment |

## Reproducing the paper's results

Each notebook in `scripts/` generates one or more figures/tables from the paper:

| Figure/Table | Script |
|---|---|
| Figure 2, Table 1 | `scripts/fig2_tab1-sst_variance_decomposition.ipynb` |
| Figure 3 | `scripts/fig3-argo_float_profiles.ipynb` |
| Figures 4, 5 | `scripts/fig4_5-model_sst_and_temp_profiles.ipynb` |
| Figures 6, 7, 8 | `scripts/fig6_7_8-budgets.ipynb` |
| Figure 9 | `scripts/fig9-sst_cntl_vs_nowind.ipynb` |

## Data availability

The processed data needed to reproduce the paper's figures and tables are included in `data/`. Raw, unprocessed data are available from the corresponding author upon reasonable request.

## Citation

If you use this code, please cite:

```bibtex
@article{basak2026indonesianseas,
  title   = {Monsoonal wind-driven ocean dynamics drive seasonal sea surface temperature variability in the Indonesian seas},
  author  = {Basak, Sougata and Nikurashin, Maxim and Pe{\~n}a-Molino, Beatriz and Sloyan, Bernadette M. and Phillips, Helen},
  journal = {Journal Name},
  year    = {2026},
  doi     = {10.xxxx/xxxxx}
}
```

## License

See [LICENSE](LICENSE).

## Contact

Sougata Basak — sougata.basak@utas.edu.au
