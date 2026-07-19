# Decoupling of Aboveground and Belowground Intraspecific Trait Variation Along Richness Gradients in Plants

Reproducible analysis code and data for the manuscript (Annals of Botany,
AOB-2026-167.R1): a three-year controlled seedling experiment testing how
species richness shapes intraspecific trait variation (ITV) in aboveground
vs belowground plant organs.

## Contents

- `Analysis.Rmd` — single, ordered R Markdown document producing all main-text
  figures/tables and Fig. S1:
  - Fig. 1: Multidimensional ITV (TPD/FRic) and PCA-axis ITV, aboveground vs belowground
  - Fig. 2: Single-trait ITV (11 traits)
  - Fig. 3: Within- vs between-species biomass variance decomposition
  - Fig. 4: Gini coefficient of biomass asymmetry
  - Fig. 5: Species-level mean trait value shifts along the richness gradient
  - Table S1: Aboveground vs belowground compartment interaction test
  - Table S2: Composition random-effect LRT decisions (Fig. 1 and Fig. 2 metrics)
  - Fig. S1: PCA biplots (trait loadings)
  - Fig. S2: Species-specific richness-ITV relationships (multidimensional and PCA-axis ITV)
  - Fig. S3: Species-specific richness-ITV relationships (single-trait ITV)
  - Appendix: robustness checks (paired-organ intersection; pot-level subsampling)
- `data/SeedlingTraitData.csv` — individual-seedling trait, biomass, and
  richness-treatment data underlying all analyses.
- `figures/` — rendered figure outputs (PDF + PNG).
- `tables/` — rendered table outputs (CSV).

## Reproducing

Open `Analysis.Rmd` in RStudio and knit, or from the command line:

```r
rmarkdown::render("Analysis.Rmd")
```

Required R packages are loaded at the top of the document (tidyverse, lme4,
lmerTest, effects, paran, psych, TPD, ineq, patchwork, ggpubr, ggthemes,
MuMIn, eoffice).
