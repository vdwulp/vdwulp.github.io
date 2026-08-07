# Set RStudio Secondary Repository

This function updates the RStudio preferences saved in the
`rstudio-prefs.json` file to include the secondary repositories passed
by the user. If a new name for an existing repository is passed by the
user, the name will be updated in the JSON file.

## Usage

``` r
use_rstudio_secondary_repo(...)
```

## Arguments

- ...:

  series of named secondary repositories, e.g.
  `ropensci = "https://ropensci.r-universe.dev"`

## Value

Invisibly returns the updated `cran_mirror` preference as a named list
on success, or `NULL` if no updates were made (no changes, user aborted,
or not in an interactive session).

## Details

A note for users outside of the USA. If the country in
`.$cran_mirror$country` has not been previously recorded in the JSON
preferences file (typically, auto set by RStudio), the
`use_rstudio_secondary_repo()` function will set `"country" = "us"`.

## Author

Daniel D. Sjoberg

## Examples

``` r
if (FALSE) { # interactive()
use_rstudio_secondary_repo(
  ropensci = "https://ropensci.r-universe.dev",
  ddsjoberg = "https://ddsjoberg.r-universe.dev"
)
}
```
