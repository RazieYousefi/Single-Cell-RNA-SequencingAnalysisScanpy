# Single-Cell RNA Sequencing Analysis with Scanpy

## Overview

This repository contains Jupyter notebooks for analyzing single-cell RNA sequencing (scRNA-seq) data using Python and [Scanpy](https://scanpy.readthedocs.io/). The notebooks cover the main stages of a scRNA-seq analysis workflow, from quality control and dimensionality reduction to clustering, differential gene expression, cell-type annotation, and spatial transcriptomics.

The workflow is designed to provide a modular starting point for exploring single-cell gene expression data, identifying cellular populations, and characterizing transcriptional differences between groups of cells.

## Analysis Workflow

The notebooks are organized in the following order:

| Step | Notebook | Description |
|---|---|---|
| 1 | [`scanpy_01_qc.ipynb`](scanpy_01_qc.ipynb) | **Quality control (QC):** Examine cell and gene quality metrics and identify low-quality cells before downstream analysis. |
| 2 | [`scanpy_02_dim_reduction.ipynb`](scanpy_02_dim_reduction.ipynb) | **Dimensionality reduction:** Represent high-dimensional gene expression profiles in a lower-dimensional space to facilitate exploration of cellular variation. |
| 3 | [`scanpy_03_integration.ipynb`](scanpy_03_integration.ipynb) | **Data integration:** Integrate datasets or samples to help account for technical variation and facilitate joint analysis. |
| 4 | [`scanpy_04_clustering.ipynb`](scanpy_04_clustering.ipynb) | **Cell clustering:** Group cells according to similarities in their gene expression profiles. |
| 5 | [`scanpy_05_dge.ipynb`](scanpy_05_dge.ipynb) | **Differential gene expression (DGE):** Identify genes with differential expression between selected cell groups or experimental conditions. |
| 6 | [`scanpy_06_celltype_MyVersion.ipynb`](scanpy_06_celltype_MyVersion.ipynb) | **Cell-type annotation:** Explore marker genes and assign putative cell-type identities to clusters. |
| 7 | [`scanpy_07_spatial.ipynb`](scanpy_07_spatial.ipynb) | **Spatial transcriptomics:** Explore spatially resolved gene expression data and its relationship to tissue organization. |

*Note: The descriptions summarize the intended purpose of each notebook based on its filename. Specific methods and outputs depend on the implementation in each notebook.*

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/RazieYousefi/scRNAseq.git
cd scRNAseq
```

### 2. Set up the Python environment

Python and Jupyter Notebook are required. The analysis uses Scanpy and may require additional scientific Python packages, depending on the notebook.

A basic environment can be created using Conda:

```bash
conda create -n scrnaseq python=3.11
conda activate scrnaseq
pip install scanpy jupyterlab
```

Additional dependencies may be required for integration, clustering, differential expression, or spatial analysis.

### 3. Launch JupyterLab

```bash
jupyter lab
```

Open the notebooks in sequence, beginning with `scanpy_01_qc.ipynb`.

## Requirements

The core analysis environment includes:

- Python
- Scanpy
- AnnData
- NumPy
- pandas
- SciPy
- Matplotlib
- JupyterLab or Jupyter Notebook

Other packages may be needed for specific analytical methods.

## Data

The notebooks require appropriate scRNA-seq expression data and associated metadata. Depending on the analysis, inputs may include gene expression count matrices, cell and gene annotations, sample identifiers, experimental conditions, or spatial coordinates.

Ensure that input file paths and metadata fields match the structure expected by each notebook before execution.

## Reproducibility

For reproducible analyses:

- Use a consistent Python environment and package versions.
- Record the source of the input data and any preprocessing steps.
- Keep sample metadata and cell identifiers consistent across analysis stages.
- Document analysis parameters, filtering thresholds, and random seeds where applicable.
- Review integration and clustering results to ensure that biological variation is not inadvertently removed.

## Repository Structure

```text
scRNAseq/
├── scanpy_01_qc.ipynb
├── scanpy_02_dim_reduction.ipynb
├── scanpy_03_integration.ipynb
├── scanpy_04_clustering.ipynb
├── scanpy_05_dge.ipynb
├── scanpy_06_celltype_MyVersion.ipynb
├── scanpy_07_spatial.ipynb
└── README.md
```

## Citation and Acknowledgments

This repository uses [Scanpy](https://scanpy.readthedocs.io/), a Python toolkit for single-cell gene expression analysis.

For the underlying methods, please refer to the [Scanpy documentation](https://scanpy.readthedocs.io/) and the relevant publications cited by the individual analysis methods.

## Author

**Razie Yousefi**

GitHub: [@RazieYousefi](https://github.com/RazieYousefi)

## License

A license has not been specified in this repository. Please check the repository for licensing terms before reusing or redistributing its code.
