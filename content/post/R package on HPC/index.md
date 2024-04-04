---
title: Manage R Packages on HPC
date: '2022-07-28'
summary: Manage R Packages on HPC

authors:
  - admin

tags:
  - HPC
  - R

# folder
categories:
  - Data analysis
  - Note
---

When encountering issues installing R packages on the farm HPC using the conventional method (e.g., `install.packages()`), try out the conda environment: https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html

## 1. Load the conda module: module load conda3/1.0

```bash
module load conda3/1.0
```


## 2. Build an environment

```bash
conda create -n myenv
```

## 3. Activate the environment

```bash
conda activate myenv
```

## 4. Add packages to this environment

```bash
conda install -c conda-forge -c bioconda [PKG1] [PKG2] [...]
```

Where [PKG1] etc are conda packages; R packages on conda are named r-[library name]. For example, `conda install -c conda-forge -c bioconda r-dplyr`

## 5. Now start R and run: library(pkg)

For example
```r
library(dplyr)
```

## 6. Once it's done, deactivate the conda environment

```bash
conda deactivate
```
