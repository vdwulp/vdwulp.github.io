# Collect codriver diagnostic information

Collects the current package version, active configuration, and
R/RStudio environment details.

## Usage

``` r
codriver_info()
```

## Value

A `codriver_info` object: a named list with elements `version`,
`configuration`, and `environment` (a named list with `r`, `rstudio`,
`rstudioapi`, and `ellmer`).
