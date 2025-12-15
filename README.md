# ofc_schemas

This repository contains the analysis and figure-generation code accompanying the manuscript  
**“Persistent representation of a prior schema in the orbitofrontal cortex facilitates learning of a conflicting schema.”**

All scripts and notebooks reproduce the primary analyses and figures using the dataset published on Figshare.

---

## 📂 Repository Structure

| File / Folder | Description |
|----------------|-------------|
| `Persistent-representation-of-a-prior-schema-updated.ipynb` | Main analysis notebook reproducing all figures **except Figure 5** (behavioral, electrophysiological, and DREADD analyses). Uses the `new_schema_env.yml` environment. |
| `umap_ccgp.ipynb` | Dedicated notebook for **Figure 5**, which includes the UMAP and CCGP population-geometry analyses. Uses the `umap-env` environment. |
| `new_schema_env.yml` | Conda environment file specifying dependencies for the main analysis. |
| `umap-env.yml` |  Environment file for the UMAP/CCGP analyses. |
| `README.md` | This document. |

---

## 📊 Dataset

All data required to run these analyses are available via Figshare:

**DOI:** [10.6084/m9.figshare.30358960](https://doi.org/10.6084/m9.figshare.30358960)  
**Direct link:** [https://figshare.com/s/c44a2d3fc5d00b5116a1](https://figshare.com/s/c44a2d3fc5d00b5116a1)

The dataset includes:
- Preprocessed session-level `.pkl` files (`all_data_X.pkl`)
- UMAP and CCGP result files used for Figure 5
- Confusion-matrix templates for model comparison (Figure 6)
- Behavioral results from the chemogenetic inactivation experiment (Figure 8)

Download and place these files in the `data/` directory (or update paths in the notebooks accordingly).

---

⚙️ Environment Setup & Figure Reproduction

Each analysis notebook runs in its own Conda environment.
Follow the steps below to create and activate the appropriate environment, then reproduce the figures.

Environment Setup
Option 1 — Main analysis (all figures except Fig. 5):

conda env create -f new_schema_env.yml
conda activate new_schema_env

Open Persistent-representation-of-a-prior-schema-.ipynb in your IDE (e.g., DataSpell, JupyterLab)
and select the Python (new_schema_env) kernel.

Option 2 — UMAP / CCGP analysis (Figure 5):

conda env create -f umap-env.yml
conda activate umap-env

Open umap_ccgp.ipynb and select the Python (umap-env) kernel.

Reproducing Figures
Download and unpack the dataset from Figshare.
Activate the matching environment (new_schema_env or umap-env).
Open the corresponding notebook:
Persistent-representation-of-a-prior-schema-updated.ipynb → Figures 1–4 & 6–8
umap_ccgp.ipynb → Figure 5
Run all cells sequentially to reproduce the figures and results.


