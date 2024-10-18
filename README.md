# HTD Dengue Severity Profile (69DX)

This repository contains Rscript for the descriptive analysis for Dengue severity profile
Trinh Dong, 2024


# Prerequisites

RStudio >= 2024.04
R >= 4.4.0
 
# How to run

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

 # Project tree
 
- 69DX.Rmd: report generation file, requiring data generated for 02_create_VAD.R
- analysis/: analysis code
- analysis/01_import.R: code for importing data
- analysis/02_create_VAD.R: generate processed data for 69DX
- data/: data
- data/raw: raw data
- data/imported: imported data, generated by analysis/01_import.R
- data/vad: processed data, generated by analysis/02_create_VAD.R
