# Decoupling of Aboveground and Belowground Intraspecific Trait Variation Along Richness Gradients in Plants

Reproducible analysis code and data for the manuscript (Annals of Botany,
AOB-2026-167.R1): a three-year controlled seedling experiment testing how
species richness shapes intraspecific trait variation (ITV) in aboveground
vs belowground plant organs.

## Data availability note

The individual-level raw measurement file is not shared, to avoid
prematurely releasing data intended for other manuscripts. This repository
instead provides `data/SeedlingTraitData_public.csv`, in which single-trait
columns are already log10-transformed (where applicable) and z-standardized
and QC-flagged/dead individuals are already removed, plus
`data/PCA_summary_public.csv` (PCA loadings and variance explained). Both
files, together with `Analysis_public.Rmd`, reproduce every figure and
table in the manuscript.

## Contents

- `Analysis_public.Rmd` — single, ordered R Markdown document that reads the
  public data files and produces all main-text figures/tables and Fig. S1:
  - Fig. 1: Multidimensional ITV (TPD/FRic) and PCA-axis ITV, aboveground vs belowground
  - Fig. 2: Single-trait ITV (11 traits)
  - Fig. 3: Gini coefficient of biomass inequality
  - Fig. 4: Within- vs between-species biomass variance decomposition,
    aboveground and belowground shown as separate panels
  - Fig. 5: Species-level mean trait value shifts along the richness gradient
  - Table S1: Aboveground vs belowground compartment interaction test
  - Table S2: Composition random-effect LRT decisions (Fig. 1 and Fig. 2 metrics)
  - Fig. S1: PCA biplots (trait loadings)
  - Fig. S2: Species-specific richness-ITV relationships (multidimensional and PCA-axis ITV)
  - Fig. S3: Species-specific richness-ITV relationships (single-trait ITV)
  - Appendix: robustness checks (paired-organ intersection; pot-level subsampling)
- `data/SeedlingTraitData_public.csv` — individual-seedling data: metadata,
  raw aboveground/belowground biomass (ABM/UBM, grams), and 11
  log10-transformed (where applicable) and z-standardized functional traits.
  QC-flagged measurement errors and dead/replaced individuals are already
  removed.
- `data/PCA_summary_public.csv` — PCA loadings and proportion of variance
  explained per compartment (PC1/PC2), used to draw the Fig. S1 biplot
  without recomputing the PCA.
- `figures/` — rendered figure outputs (PDF + PNG).
- `tables/` — rendered table outputs (CSV).

## Reproducing

Open `Analysis_public.Rmd` in RStudio and knit, or from the command line:

```r
rmarkdown::render("Analysis_public.Rmd")
```

Required R packages are loaded at the top of the document (tidyverse, lme4,
lmerTest, effects, TPD, ineq, patchwork, ggpubr, ggthemes, MuMIn, eoffice).
