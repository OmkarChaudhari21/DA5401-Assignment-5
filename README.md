# DA5401-Assignment-5
# Manifold Learning on Yeast Gene Expression Data  
*DA5401 Assignment – Visualizing Multi-Label Structures*


## Omkar Chaudhari
## Roll No: NA22B059

---

## 📖 Overview

This project explores **manifold learning techniques** (t‑SNE and Isomap) to visualize and analyze the **Yeast gene expression dataset**, which contains **103-dimensional features** and **14 functional labels** (multi-label setting).

The key goals are to:
- **Project the high-dimensional data to 2D**, preserving key structures,
- **Simplify the label space** into 4 interpretable groups for visualization,
- **Identify noisy, outlier, and hard-to-learn samples**, using diagnostics on the 2D manifold,
- **Compare t‑SNE and Isomap** for understanding the curvature and complexity of the data manifold.

---

## Assignment Breakdown
### Part A — Preprocessing (10 pts)

- Loaded Yeast dataset (2417 samples, 103 features, 14 labels)

- Created 4-class color index: TopSingle1, TopSingle2, TopCombo, Other

 - Scaled features using StandardScaler

### Part B — t‑SNE & Veracity Inspection (20 pts)

- Ran t-SNE with perplexity = 5, 30, 50 → chose 30 for balance

- Visualized 4 groups clearly

- Flagged:

-- Ambiguous points via DBSCAN minority

-- Outliers via Local Outlier Factor (LOF)

-- Hard-to-learn zones via KNN label mixing

### Part C — Isomap & Manifold Geometry (20 pts)

- Ran Isomap with k = 5, 10, 20 → chose k = 10

- Compared global structure to t‑SNE

- Found strong curvature in manifold → suggests non-linear classifiers are needed

---

## Repository Structure

```bash
.
├── DA5401_A5_manifold.ipynb     #  Main Jupyter notebook (annotated, all code + markdown)
├── README.md                    #  This file
├── figs/                        #  Saved plots for each stage of analysis
│   ├── tsne_p30.png
│   ├── tsne_p30_dbscan_ambiguous.png
│   ├── tsne_p30_lof_outliers.png
│   ├── tsne_p30_mixing.png
│   ├── isomap_k5_10_20.png
│   └── isomap_k10.png
└── data/
    └── yeast.arff              #  Dataset (ARFF format)

