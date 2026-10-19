# SMC56Box

Interactive 3D UMAP of 5,045 cells across BRCA, COAD, LUAD, and STAD, with SMC5/6 subunit and module overlays.

## View

Open `four_cancer_3D_interactive.html` in a browser. The page loads Plotly.js 2.35.2 from the Plotly CDN, so an internet connection is needed.

## Cell groups

The page can color cells by cancer type, the 10 original cell subtype labels, or eight unsupervised Louvain clusters. Clustering uses the archived first 30 PCA dimensions (k=20, resolution=1.2); the 3D UMAP is recomputed from those dimensions (cosine distance, 20 neighbors, min_dist=0.1, seed=42). Clusters 1, 3, and 4 are each enriched for malignant epithelial subtypes.

The original `cell_type` labels were inconsistent with the more specific `original_cell_type` annotations, so the page uses the 10 original subtype labels. This archived object has no patient or sample identifiers, and its source accession is unresolved. Cluster and cancer-type comparisons are exploratory cell-level descriptions, not patient-level inference.
