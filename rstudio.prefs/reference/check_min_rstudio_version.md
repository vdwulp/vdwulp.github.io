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

Called for its side effect; aborts with an error if the version
requirement is not met, otherwise returns invisibly.

## Author

Daniel D. Sjoberg

## Examples

``` r
if (interactive()) {
  check_min_rstudio_version("1.3")
}
```
