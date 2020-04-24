
<!-- README.md is generated from README.Rmd. Please edit that file -->
[ricu](https://septic-tank.github.io/ricu/)
===========================================

<!-- badges: start -->
[![](https://img.shields.io/badge/lifecycle-maturing-blue.svg)](https://www.tidyverse.org/lifecycle/#maturing) [![R build status](https://github.com/septic-tank/ricu/workflows/check/badge.svg)](https://github.com/septic-tank/ricu/actions) [![Codecov test coverage](https://codecov.io/gh/septic-tank/ricu/branch/master/graph/badge.svg)](https://codecov.io/gh/septic-tank/ricu?branch=master) <!-- badges: end -->

Working with ICU datasets, especially with publicly available ones as provided by [Physionet](https://physionet.org) in R is facilitated by `ricu`, which provides data access, a level of abstraction to encode clinical concepts in a data source agnostic way, as well as classes and utilities for working with the arising types of time series datasets.

Installation
------------

Currently, installation is only possible from github directly, using the `remotes` if installed

``` r
remotes::install_github("septic-tank/ricu")
```

or by sourcing the required code for installation from github by running

``` r
rem <- source(
  paste0("https://raw.githubusercontent.com/r-lib/remotes/master/",
         "install-github.R"
)
rem$value("septic-tank/ricu")
```

In order to make sure that some useful utility packages are installed as well, consider installing the packages marked as `Suggests` as well by running

``` r
remotes::install_github("septic-tank/ricu", dependencies = TRUE)
```

instead, or by installing some of the utility packages (relevant for downloading and preprocessing Physionet datasets)

``` r
install.packages(c("getPass", "keyring", "openssl", "xml2"))
```

and demo dataset packages

``` r
install.packages(c("mimic.demo", "eicu.demo"),
                 repos = "https://septic-tank.github.io/physionet-demo")
```

explicitly.
