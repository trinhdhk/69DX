# HTD Dengue Severity Profile (69DX)

This repository contains Rscript for the descriptive analysis for Dengue severity profile

Trinh Dong, 2024


## Prerequisites

RStudio >= 2024.04

R >= 4.4.0
 
## How to run

> [!WARNING]  
> This code is tailored for RStudio. It is required to change the code to run in other environment/IDE. See below for instructions.

You have to create a directory data/raw/ and input your raw data inside.
Additionally: data/raw/BirthDataFix.xlsx contains fixed age demographic info.


```sh
mkdir('data')
mkdir('data/raw')
```

```r
install.package('renv')
renv::restore()
```

Given all datasets are in data/raw, to generate report, open in Rstudio `69DX.Rproj`

1. Open `analysis/01_import.R`, click on `Source`
2. Open `analysis/02_create_VAR.R`, click on `Source`
3. Open `69DX.Rmd`, click on `Knit`

In case of failure in 1 or 2 (or not Rstudio), comment out this line

```r
setwd(dirname(rstudioapi::getActiveDocumentContext()$path))
```

in both files, then change the working directory to analysis

```r
setwd('analysis')
```

and run 1, 2 again.

 ## Project tree
 
- 69DX.Rmd: report generation file, requiring data generated for 02_create_VAD.R
- analysis/: analysis code
- analysis/01_import.R: code for importing data
- analysis/02_create_VAD.R: generate processed data for 69DX
- data/: data
- data/raw: raw data
- data/imported: imported data, generated by analysis/01_import.R
- data/vad: processed data, generated by analysis/02_create_VAD.R

