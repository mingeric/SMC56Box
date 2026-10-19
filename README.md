# SMC56Box

Interactive 3D UMAP of 5,045 cells across BRCA, COAD, LUAD, and STAD, with SMC5/6 subunit and module overlays.

## View

Open `index.html` in a browser or visit the [GitHub Pages visualization](https://mingeric.github.io/SMC56Box/). The page loads Plotly.js 2.35.2 from the Plotly CDN, so an internet connection is needed.

## Cell groups

The page opens colored by the 21 unsupervised Louvain clusters and can also color cells by cancer type or the 10 original cell subtype labels. Clustering uses the archived first 30 PCA dimensions (k=20, resolution=2.0); the 3D UMAP uses cosine distance, 10 neighbors, min_dist=0.01, and seed=42. All 5,045 cells in the archived object are shown; the page does not downsample this view. Twelve clusters are enriched for malignant epithelial labels (>80% of cells in each cluster); cluster numbers are computational labels, not validated cell identities.

The original `cell_type` labels were inconsistent with the more specific `original_cell_type` annotations, so the page uses the 10 original subtype labels. This archived object has no patient or sample identifiers, and its source accession is unresolved. Cluster and cancer-type comparisons are exploratory cell-level descriptions, not patient-level inference.
