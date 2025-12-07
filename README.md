# Data and Code for "Mosaic brain evolution in woodpeckers and its relationship to extraordinary beak behavior"

## Description

This archive contains the data and R code necessary to reproduce the analyses presented in the manuscript **"Mosaic brain evolution in woodpeckers and its relationship to extraordinary beak behavior"** by Daniel J. Tobiansky, Ghislaine Cardenas-Posada, and Matthew J. Fuxjager. The analysis examines the comparative morphology and ecology of the Choroid Plexus (ChP) in Piciformes.

## Directory Structure

-   `code/`: R scripts for analysis.
-   `data/`: CSV data files.
-   `phylo_trees/`: Phylogenetic trees used for comparative analysis.

## Key Files

### 1. Analysis Script (`code/`)

-   **`Piciformes_ChP_Analysis.R`**: The comprehensive R script that replicates all manuscript results. It performs:
    -   **Descriptive Stats & T-tests:** Shelf-life, Relative ChP Size, Cell Morphology.
    -   **Ancestral State Reconstruction (ASR):** For relative ChP size (Figure 3).
    -   **Phylogenetic PCA (pPCA):** For Picidae and All Piciformes (Figure 2, Supp Fig).
    -   **PGLS Analysis:** Testing evolutionary relationships between brain cell morphology (PC1) and relative ChP size with ecological traits (Nesting, Foraging, Habitat, etc.).

### 2. Data (`data/`)

-   `Data_Specimens.csv`: Detailed specimen info (metadata, body size).
-   `Data_Ecology_and_ChP_Size.csv`: Ecological variables and ChP/brain measurements.
-   `Data_Cell_Morphology.csv`: Cell-level morphology measurements (nuclei size, etc.).

### 3. Phylogenetic Trees (`phylo_trees/`)

-   `Tree_Piciformes_Expanded_2018.nex` (Fuxjager Tree)
-   `Tree_Piciformes_Consensus.nwk` (Consensus Tree)
-   `Tree_Piciformes_Ultrametric.nwk` (Ultrametric Tree)
-   `Tree_Picidae_Pruned_Miles2018.nwk` (Pruned Miles Tree)

## Outputs Produced

Running `Piciformes_ChP_Analysis.R` generates the following findings:

### Figures

-   **`Figure1_Relative_ChP_Regions.png`**: Multi-panel dot plots showing relative ChP size (Posterior, Anterior, 3rd Ventricle) for Picidae vs. Non-Picidae.
-   **`Figure2_Picidae_pPCA.png`**: Phylogenetic PCA biplot for Picidae species.
-   **`Figure3_ASR_pLV_ChP_Area.png`**: Ancestral State Reconstruction of ChP area.
-   **`Figure4_Ecological_Trends.png`**: Panels A-F showing relationships between Posterior ChP size and ecological variables (Foraging, Nesting, Clutch, Habitat, Drumming).
-   **`Supplemental_Figure_AllPiciformes_pPCA.png`**: PCA biplot for all Piciformes.
-   **`Correlation_Matrix.png`**: Correlation plot of cell morphology variables.

### Statistical Tables (Saved as CSV)

The script prepares these tables for export (lines are commented out in code by default): \* `Results_Ttest_ChP_area.csv` \* `Results_Ttest_cell_morphology_log.csv` \* `pPCA_loadings_PicTree18.csv`, `pPCA_loadings_EricsonConsensus.csv`, `pPCA_loadings_AllPiciformes.csv` \* `Results_PGLS_FuxjagerTree.csv` \* `Results_PGLS_ConsensusTree.csv` \* `Results_PGLS_UltrametricTree.csv` \* `Results_PGLS_AllPiciformes.csv` (Includes new Group Effect test)

## Instructions for Use

1.  **Install R:** Ensure you have R installed (v4.0+ recommended).
2.  **Packages:** The script automatically checks for and installs required packages (e.g., `ape`, `phytools`, `nlme`, `caper`, `tidyverse`).
3.  **Run:** Open `Piciformes_ChP_Analysis.R` in RStudio or run via command line.
    
