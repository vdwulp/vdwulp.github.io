# Set RStudio Secondary Repository

Updates the secondary repositories in `rstudio-prefs.json`.

## Usage

``` r
use_rstudio_secondary_repo(...)
```

## Arguments

- ...:

  a series of named secondary repositories, e.g.
  `ropensci = "https://ropensci.r-universe.dev"`. Pass `NULL` to remove
  a repository, e.g. `ropensci = NULL`. If a URL is passed under a new
  name, the old name is removed.

## Value

Invisibly returns the updated `cran_mirror` preference as a named list
on success, or `NULL` if no updates were made (no changes, user aborted,
or not in an interactive session).

## Author

Daniel D. Sjoberg (2021-2022)

S.A. van der Wulp (since 2026)

## Examples

``` r
if (FALSE) { # interactive()
# Add a repository
use_rstudio_secondary_repo(
  ropensci = "https://ropensci.r-universe.dev",
  username = "https://username.r-universe.dev"
)

# Remove a repository
use_rstudio_secondary_repo(ropensci = NULL)
}
```
