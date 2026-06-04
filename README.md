# NeuroFIDELITY: A Brain Twin Discovery Framework for Alzheimer's Disease

## Repository Overview

This repository contains the implementation of **NeuroFIDELITY**, a quantum fidelity-based framework for Alzheimer's disease patient retrieval and Brain Twin discovery using structural MRI data.

The project consists of two primary notebooks:

### 1. `pca-8d.ipynb`

This notebook performs MRI preprocessing and dimensionality reduction.

Functions:

* Loads MRI images from the OASIS dataset
* Applies preprocessing and feature extraction
* Reduces the original MRI representation to an 8-dimensional latent space using Principal Component Analysis (PCA)
* Generates the file:

```text
brain_signatures_8d.csv
```

which contains the compact patient representations used in subsequent analyses.

**Note:** Running this notebook requires access to the OASIS MRI dataset through Kaggle and may take a considerable amount of time due to image loading and preprocessing.

---

### 2. `parameters_data_analysis_classic_and_quantum.ipynb`

This notebook performs the main patient similarity analysis.

Functions:

* Classical similarity retrieval (Cosine, Euclidean, Manhattan)
* Quantum fidelity-based retrieval
* Brain Twin discovery
* Disease-stage consistency evaluation
* Retrieval performance analysis

This notebook requires:

```text
brain_signatures_8d.csv
```

to be present in the working directory.

To simplify reproducibility, the file **brain_signatures_8d.csv** has been pre-generated and included in this repository. Users can therefore run the analysis notebook directly without reprocessing the entire MRI dataset.

---

## Quick Start

1. Download or clone this repository.
2. Ensure that:

```text
brain_signatures_8d.csv
```

is located in the project directory.
3. Open and run:

```text
parameters_data_analysis_classic_and_quantum.ipynb
```

4. All retrieval experiments and Brain Twin analyses can then be reproduced without requiring access to the original MRI dataset.

---

## Dataset

This project utilizes MRI scans derived from the OASIS-1 Alzheimer's Disease dataset.

Disease stages analyzed:

* Non Demented
* Very Mild Demented
* Mild Demented
* Moderate Demented

---

## Notes

The provided `brain_signatures_8d.csv` file is intended solely to facilitate reproducibility and reduce computational overhead. Researchers wishing to regenerate the embeddings from the original MRI scans may do so using `pca-8d.ipynb`, provided they have access to the required OASIS MRI data.
