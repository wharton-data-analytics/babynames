# babynames

[![Travis-CI Build Status](https://travis-ci.org/wharton-data-analytics/babynames.svg?branch=master)](https://travis-ci.org/wharton-data-analytics/babynames)

## Overview

This package contains three datasets provided by the USA Social Security Administration:

* `babynames`: For each year from 1880 to 2015, the number of children of 
  each sex given each name. All names with more than 5 uses are given.
  (Source: http://www.ssa.gov/oact/babynames/limits.html)

* `applicants`: The number of applicants for social security numbers (SSN) for
  each year for each sex. 
  (Source: http://www.ssa.gov/oact/babynames/numberUSbirths.html)

* `lifetables`: Cohort life tables data
  (Source: http://www.ssa.gov/oact/NOTES/as120/LifeTables_Body.html)

It also includes the following data set from the US Census:

* `births`: Number of live births by year, up to 2014.
  (Source: http://www.census.gov/statab/hist/02HS0013.xls and
  http://www.cdc.gov/nchs/data/nvsr/nvsr62/nvsr62_09.pdf)


## Usage

Install it from github with:
  
```{r}
if(!require(devtools)) {
  install.packages(devtools)
}
devtools::install_github("wharton-data-analytics/babynames")
```

Then, you can do:

```{r}
baby_names <- babynames::babynames
head(baby_names)
```

Alternatively, if you look under `data-raw/csv` in this repository, you will find the raw csv files for this dataset, if you want to analyze this data with a different environment.

Babynames csv: https://cdn.rawgit.com/wharton-data-analytics/babynames/3192856738dee4a91bfc7d320355daa5ae428c17/data-raw/csv/babynames.csv
