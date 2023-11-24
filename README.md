![cc-by-sa 4.0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/by-sa.svg)

[![build-and-deploy-validation-report](https://github.com/imbi-heidelberg/adoptr-validation-report/actions/workflows/build-and-deplay-validation-report.yml/badge.svg)](https://github.com/imbi-heidelberg/adoptr-validation-report/actions/workflows/build-and-deplay-validation-report.yml)

# **adoptr** Validation Report 

This repository contains code to build an automated validation report for the 
[**adoptr**](https://github.com/imbi-heidelberg/adoptr) R package.
The report is built using R Markdown and the **bookdown** 
(https://github.com/rstudio/bookdown) package.
The most recent build of the validation report is hosted on this repository's 
GitHub pages site, [here](https://imbi-heidelberg.github.io/adoptr-validation-report/).
The report itself contains a brief description of the necessary steps to 
produce a report for a local installation of **adoptr**.

The following quality metrics are inspired by https://www.pharmar.org/packages/:

| **Metric**                          | **Value/Statement** |
|:------------------------------------|:--------------------|
| **Vignette?**                       | https://imbi-heidelberg.github.io/adoptr/articles/adoptr.html |
| **Website?**                        | https://imbi-heidelberg.github.io/adoptr |
| **Version Control?**                | https://github.com/imbi-heidelberg/adoptr | 
| **Public/Open Source Development?** | https://github.com/imbi-heidelberg/adoptr |
| **Formal Bug Tracking?**            | https://github.com/imbi-heidelberg/adoptr/issues |
| **Changelog?**                      | https://imbi-heidelberg.github.io/adoptr/news/index.html |
| **Release Cycle**                   | irregular |
| **Unit Testing?**                   | [![codecov](https://codecov.io/gh/imbi-heidelberg/adoptr/branch/master/graph/badge.svg)](https://codecov.io/gh/imbi-heidelberg/adoptr) |
| **License**                         | MIT, https://github.com/imbi-heidelberg/adoptr/blob/master/LICENSE.md |
| **CRAN?**                           | [![CRAN status](https://www.r-pkg.org/badges/version/adoptr)](https://cran.r-project.org/package=adoptr) |
| **Long-term storage?**              | [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.2616951.svg)](https://doi.org/10.5281/zenodo.2616951) |
| **# Downloads**                     | R Studio CRAN mirror: [![R Studio CRAN monthly downloads](http://cranlogs.r-pkg.org/badges/last-month/adoptr?color=green)](https://cran.r-project.org/package=adoptr) [![](http://cranlogs.r-pkg.org/badges/grand-total/adoptr?color=green)](https://cran.r-project.org/package=adoptr) |
| **Maturity**                        | Initial CRAN release date: 2019-04-01 |



## Creating a Local Validation Report

To validate a local version of  **adoptr**, clone the validation report
source repository via
```bash
git clone https://github.com/imbi-heidelberg/adoptr-validation-report.git
```
and switch to the newly created folder
```bash
cd adoptr-validation-report
```
Install the dependencies listed in the DESCRIPTION file, i.e.
```R
install.packages(c("adoptr", "tidyverse", "bookdown", "rpact", "testthat", "pwr", "tinytex"))
```
before finally building the book via
```bash
Rscript -e 'bookdown::render_book("index.Rmd", output_format = "all")'
```
(or executing the equivalent command in an R terminal in the same folder).
This will produce a `_book` folder with an `index.html` file that can be 
viewed in a browser as well as the PDF version of the validation
report.
