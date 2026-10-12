# Collect codriver diagnostic information

Collects the current package version, active configuration, R/RStudio
environment details, and token usage for the active ellmer session.

## Usage

``` r
codriver_info()
```

## Value

A `codriver_info` object: a named list with elements `version`,
`configuration`, `environment` (a named list with `r`, `rstudio`,
`rstudioapi`, and `ellmer`), and `token_usage` (a tibble, or `NULL` if
ellmer is not installed or no usage has been recorded).
