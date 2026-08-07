# Check Min RStudio Version

Return error if minimum version requirement not met.

## Usage

``` r
check_min_rstudio_version(version)
```

## Arguments

- version:

  string of min required version number

## Value

path string to RStudio `rstudio-prefs.json` file

## Author

Daniel D. Sjoberg

## Examples

``` r
if (interactive()) {
  check_min_rstudio_version()
}
```
