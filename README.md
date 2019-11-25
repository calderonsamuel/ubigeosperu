
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
library(dplyr)

## ubigeosperu contains a single dataframe object containing the peruvian ubigeos codes.

## This are the dimentions of the dataframe
dim(ubigeos)
#> [1] 1876   18

## The ubigeos dataset is a tibble
ubigeos
#> # A tibble: 1,876 x 18
#>    cod_dep_inei desc_dep_inei cod_prov_inei desc_prov_inei cod_ubigeo_inei
#>    <chr>        <chr>         <chr>         <chr>          <chr>          
#>  1 01           AMAZONAS      0101          CHACHAPOYAS    010101         
#>  2 01           AMAZONAS      0101          CHACHAPOYAS    010102         
#>  3 01           AMAZONAS      0101          CHACHAPOYAS    010103         
#>  4 01           AMAZONAS      0101          CHACHAPOYAS    010104         
#>  5 01           AMAZONAS      0101          CHACHAPOYAS    010105         
#>  6 01           AMAZONAS      0101          CHACHAPOYAS    010106         
#>  7 01           AMAZONAS      0101          CHACHAPOYAS    010107         
#>  8 01           AMAZONAS      0101          CHACHAPOYAS    010108         
#>  9 01           AMAZONAS      0101          CHACHAPOYAS    010109         
#> 10 01           AMAZONAS      0101          CHACHAPOYAS    010110         
#> # … with 1,866 more rows, and 13 more variables: desc_ubigeo_inei <chr>,
#> #   cod_dep_reniec <chr>, desc_dep_reniec <chr>, cod_prov_reniec <chr>,
#> #   desc_prov_reniec <chr>, cod_ubigeo_reniec <chr>, desc_ubigeo_reniec <chr>,
#> #   cod_dep_sunat <chr>, desc_dep_sunat <chr>, cod_prov_sunat <chr>,
#> #   desc_prov_sunat <chr>, cod_ubigeo_sunat <chr>, desc_ubigeo_sunat <chr>

## You can access the tidy version and pipe it!
ubigeos_tidy %>%
    filter(lugar == "CHORRILLOS", nivel == "Distrito")
#> # A tibble: 3 x 4
#>   lugar      nivel    entidad ubigeo
#>   <chr>      <chr>    <chr>   <chr> 
#> 1 CHORRILLOS Distrito INEI    150108
#> 2 CHORRILLOS Distrito RENIEC  140108
#> 3 CHORRILLOS Distrito SUNAT   150108
```
