# Alternative_models_Po_Z_P_tot

This repository contains an example dataset and R code associated with the following publication:

**Eleni Servou**<sup>1,2*</sup>, **Eudoxia Schismenou**<sup>1,2</sup>,and **Stylianos Somarakis**<sup>2</sup>

<sup>1</sup> University of Crete, Biology Department, 70013, Heraklion, Crete, Greece

<sup>2</sup> Hellenic Centre for Marine Research (HCMR), Institute of Marine Biological Resources and Inland Waters (IMBRIW), 71003, Heraklion, Crete, Greece


**Corresponding author:** Eleni Servou ([e.servou@hcmr.gr](mailto:e.servou@hcmr.gr))

**DOI:** [To be added]

---

## Abstract

The Daily Egg Production Method (DEPM) is an ichthyoplankton-based method widely used to estimate the spawning stock biomass of small pelagic fishes. However, obtaining reliable estimates of daily egg production (i.e., the number of eggs produced daily by the stock) remains a central challenge. Traditionally, daily egg production is estimated by fitting an exponential mortality model describing the decline in egg abundance with age; however, inadequately accounting for the characteristics of abundance-at-age datasets (high proportions of zero observations, overdispersion, and spatial dependence) can challenge the accuracy and precision of estimates. This study evaluates how alternative modelling frameworks account for the properties of ichthyoplankton data and consequently affect parameter estimates. Using data from DEPM applications to the European anchovy (Engraulis encrasicolus) stock in the North Aegean Sea (eastern Mediterranean), six approaches were compared for fitting the mortality curve: (i) the classical non-linear least squares (NLS) regression, (ii) generalized linear models (GLMs) using Negative Binomial and Tweedie distributions, and (iii) spatially explicit generalized linear mixed models (GLMMs) incorporating Gaussian random fields to account for spatial structure in egg production, including a formulation allowing for spatially varying embryonic mortality.

The NLS model produced biologically plausible estimates but showed clear departures from underlying statistical assumptions. GLM formulations improved residual behaviour; however, substantial spatial dependence remained. Spatially explicit GLMMs further improved model diagnostics and goodness-of-fit by accounting for spatial structure, although allowing embryonic mortality to vary spatially resulted in overparameterization.

Spatial models consistently produced lower estimates of mean daily egg production (P0) reflecting the partitioning of variability between the overall mean and spatial components rather than a reduction in egg production integrated across the spawning area (Ptot). Ptot estimates did not exhibit any systematic change among modelling frameworks, showing overlapping confidence intervals. Increasing model complexity primarily affected how variability was partitioned among model components, generally improving model fit and reducing Ptot uncertainty. Differences between spatial and non-spatial approaches depended on the strength of the spatial structure in the data. Future DEPM applications should evaluate model assumptions and select a modelling framework based on the dataset's properties to improve the estimates' reliability and their uncertainty quantification.

---

## Repository contents

The repository is organized as follows:

### 1. `data/`
This folder contains the data required for the analyses.

* **`data.xlsx`**
  Contains the abundance-at-age dataset for the year 2006 as an example to fit the different model formulations  

* **`Greece\_geology.zip/`**
Contains shapefiles representing the coastline of Greece (`Greece`). These spatial data were used to construct the barrier mesh and for visualization and mapping purposes.

* **`voronois.zip/ ... .shp`**  
Contains shapefiles representing the A1 in each annual survey and stratum.

### 2. `code.qmd`
Quarto document containing the code used to fit and compare the different model formulations presented in the study using the example dataset.

### 3. `Barrier_mesh_sensitivity_analysis.qmd`

Quarto document containing the code used to perform the sensitivity analysis for optimizing the characteristics of the barrier mesh.
---

## Software and packages

The analyses were performed in *`R version 4.5.1`* using the following package versions:
* `sdmTMB` v1.0.0
* `sdmTMBextra` v0.0.5
Other R packages used are specified within the code files.
---

## Data use and restrictions

The data provided in this repository were collected as part of the Greek National Program for the Collection of Fisheries Data (co-funded by the Greek Ministry of Rural Development and Food and the European Union) and are made available for the purpose of reproducing the analyses presented in the associated publication. 

*Please do not use or redistribute the data for analyses or purposes outside the scope of this work without contacting the authors*





