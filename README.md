# DA5401-Assignment-5
# 🧬 Manifold Learning on Yeast Gene Expression Data  
*DA5401 Assignment – Visualizing Multi-Label Structures*

---

## 📖 Overview

This project explores **manifold learning techniques** (t‑SNE and Isomap) to visualize and analyze the **Yeast gene expression dataset**, which contains **103-dimensional features** and **14 functional labels** (multi-label setting).

The key goals are to:
- **Project the high-dimensional data to 2D**, preserving key structures,
- **Simplify the label space** into 4 interpretable groups for visualization,
- **Identify noisy, outlier, and hard-to-learn samples**, using diagnostics on the 2D manifold,
- **Compare t‑SNE and Isomap** for understanding the curvature and complexity of the data manifold.

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
