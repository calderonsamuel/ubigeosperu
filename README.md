
<!-- README.md is generated from README.Rmd. Please edit that file -->

# ubigeosperu

<!-- badges: start -->

[![Project
Status](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
[![CRAN
status](https://www.r-pkg.org/badges/version/ubigeosperu)](https://cran.r-project.org/package=ubigeosperu)
<!-- badges: end -->

The goal of ubigeosperu is to have an easy way to get the peruvian
ubigeos into R. The data has been collected from CONCYTEC’s GitHub
[repository](https://github.com/CONCYTEC/ubigeo-peru/blob/master/equivalencia-ubigeos-oti-concytec.csv).

## Installation

You can install the released version of ubigeosperu from
[CRAN](https://CRAN.R-project.org) with:

``` r
## This will work when the package is published into CRAN
install.packages("ubigeosperu")
```

And the development version from [GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("calderonsamuel/ubigeosperu")
```

## Example

This is a basic example which shows you how to solve a common problem:

``` r
library(ubigeosperu)

## ubigeosperu contains a single dataframe object containing the peruvian ubigeos codes.

## This are the dimentions of the dataframe
dim(ubigeos)
#> [1] 1876   18

## This code gives you the first ten rows of the first 4 columns of the dataframe
ubigeos[1:10,1:4]
#>    cod_dep_inei desc_dep_inei cod_prov_inei desc_prov_inei
#> 1            01      AMAZONAS          0101    CHACHAPOYAS
#> 2            01      AMAZONAS          0101    CHACHAPOYAS
#> 3            01      AMAZONAS          0101    CHACHAPOYAS
#> 4            01      AMAZONAS          0101    CHACHAPOYAS
#> 5            01      AMAZONAS          0101    CHACHAPOYAS
#> 6            01      AMAZONAS          0101    CHACHAPOYAS
#> 7            01      AMAZONAS          0101    CHACHAPOYAS
#> 8            01      AMAZONAS          0101    CHACHAPOYAS
#> 9            01      AMAZONAS          0101    CHACHAPOYAS
#> 10           01      AMAZONAS          0101    CHACHAPOYAS
```
