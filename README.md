# SMC5/6 multi-cancer single-cell visualizations

Open the [all-visualizations dashboard](https://mingeric.github.io/SMC56Box/) for the expanded cohort overview, donor-level results, paired CRC analysis, and the 16-cancer targeted-panel view. The earlier [3D four-cancer page](https://mingeric.github.io/SMC56Box/four_cancer_3D_interactive.html) retains the 5,045-cell exploratory object whose source accession and patient/sample identifiers are unresolved.

## Evidence included

- Four independent full-transcriptome cohorts: 444,603 cells across CRC, BRCA and LUAD. Each cohort retains its own source full-transcriptome UMAP; these are not a shared coordinate system.
- Donor summaries for cohorts with donor identifiers and patient-paired tumor/normal tests in GSE132465.
- A separate CELLxGENE Census targeted 10-gene panel across 16 cancer labels (5,346,273 cells). It has no full-transcriptome matrix and is not used for UMAPs.
- Processed 444,603-cell feature table, source inventory, module contract, plots, and result tables in `assets/multicohort/`.

## Interpretation

In paired colorectal samples from 10 patients, epithelial NSMCE1 showed a positive tumor-minus-normal shift (mean +0.350 within-cohort z units, BH q=0.0273 across the 14 features in that compartment). None of the four predefined module scores passed multiple-testing correction. This is a bounded gene-level signal, not evidence for uniform SMC5/6 complex elevation. Patient-level cell composition also differed between tumor and normal, so composition is relevant context.

UMAP geometry is descriptive. Within-cohort gene z scores and the Census panel's within-panel count shares use different scales and must not be compared numerically. The original 5,045-cell four-cancer object is kept separate because its provenance and sample IDs are unresolved.

## Interactive 3D view

`all_cohort_3d.html` displays every cell from one selected cohort and lazily downloads that cohort's compressed plot data. It supports rotation, zoom, hover labels, cell-lineage and subtype coloring, and overlays for all 10 genes plus the four frozen modules. The 3D coordinates were recomputed with seed 42 and min_dist 0.2 from the existing cohort-specific full-transcriptome neighbor graphs. The second LUAD atlas had no stored graph, so its graph was built from its existing Harmony representation (30 neighbors) before embedding. Cohorts are kept separate; UMAP axes and distances do not have cross-cohort meaning.
