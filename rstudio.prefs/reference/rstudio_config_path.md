# RStudio Config Path

Copy of the internal function `usethis:::rstudio_config_path()`

## Usage

``` r
rstudio_config_path(...)
```

## Arguments

- ...:

  strings added to the RStudio config path

## Value

path string to RStudio `rstudio-prefs.json` file

## Author

Daniel D. Sjoberg

## Examples

``` r
if (interactive()) {
  rstudio_config_path()
}
```
