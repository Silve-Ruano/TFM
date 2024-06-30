
![B](https://github.com/Silve-Ruano/TFM/assets/157005665/1f9ec5e4-fc2a-474f-93dc-c876f0fe1486)
# Introduction
In this repository, we will use the Beyondcell platform (Fustero-Torres et al., 2021). This platform is based on identifying how drugs affect different cell lines in scRNA-seq data. In this way, we can unravel the tumor heterogeneity of the datasets we analyze. We will work in an R environment.
# Pipeline Description
![BCpipeline](https://github.com/Silve-Ruano/TFM/assets/157005665/48ee4417-9852-43d1-b1ff-ddc11cb0d847)

- Step 1: From two matrices, a Seurat expression matrix (pre-processed) and a drug expression signature (PSc or SSc), we calculate Beyondcell scores for each cell-drug pair.
- Step 2: Beyondcell scores range from 0 to 1, measuring each cell's sensitivity to a drug. The resulting Beyondcell matrix should be scaled and normalized.
- Step 3: With the Beyondcell matrix, we can obtain therapeutic clusters (in UMAP) of the desired dataset, according to the characteristic we want to highlight.
- Step 4: We perform drug prioritization by obtaining a ranking after computing the ranks.
- Step 5: The score obtained for each drug (the susceptibility) can be visualized in a UMAP plot.
*NOTE*: The PSc matrix indicates susceptibility to perturbation (before vs. after), and the SSc matrix shows the sensitivity of cells to a drug.

# Current Applications
- Ability to use a reliable tool to unravel Tumor Heterogeneity.
- Rank drugs by their effect on various tumor cell lines.
- Prioritize drugs in the fight against certain types of cancer.

# Future Applications
- A layer for performing Spatial Transcriptomics (ST) will be included to investigate expression patterns within tissues (Coming Soon).
- Detect resistance and tolerance mechanisms against drugs from the pharmacological signatures.

# How to install the 'Beyondcell' Package
It is recommended to install the Beyondcell package on an R version >= 4.0.0. Additionally, Seurat v4 is necessary for its proper functioning, as Beyondcell does not work with Seurat v5. For the correct installation of the package, we use a conda environment and mamba to download the package from Beyondcell's Github: 

``` ruby
# Create a conda environment.
conda create -n beyondcell 
# Activate the environment.
conda activate beyondcell
# Install beyondcell package and dependencies.
mamba install -c bu_cnio r-beyondcell
```
It is recommended that if any errors appear, check the R session with SessionInfo() and look at the dependencies of the different packages that Beyondcell requires. The devtools::install.packages(...) function will be useful.

# Autors
- Silvestre Ruano Rodríguez*
- Juan Antonio Nepomuceno Chamorro
- Isabel de los Ángeles Nepomuceno Chamorro

# Acknowledgements
We would like to thank Fátima Al-Shahrour and María José Jiménez-Santos for their selfless dedication in helping us and sending us some data that were not available in public repositories.

# Citation
Ruano, S., Nepomuceno, JA., Nepomuceno, IA. "Beyondcell: A Bioinformatics Approach to Adress Tumor Heterogeneity in Personalized Cancer Treatment". 2024. 

# Technical Support
If you have any questions, we recommend commenting on the 'issue' tab for resolution. If the issue is not resolved this way, please do not hesitate to send an email with the incident to silruarod@alum.us.es.
