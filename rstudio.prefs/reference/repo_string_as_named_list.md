# Convert secondary repo string to named list

The secondary repo string uses `|` to separate the repo names and their
values, as well as two different repos, e.g.
`'ropensci|https://ropensci.r-universe.dev|ddsjoberg|https://ddsjoberg.r-universe.dev'`.

## Usage

``` r
repo_string_as_named_list(x)
```

## Arguments

- x:

  secondary repository string from `"rstudio-prefs.json"` –\>
  `"cran_mirror"` –\> `"secondary"`

## Value

named list

## Author

Daniel D. Sjoberg

## Examples

``` r
repo_string_as_named_list(
  'ropensci|https://ropensci.r-universe.dev|ddsjoberg|https://ddsjoberg.r-universe.dev'
)
#> $ropensci
#> [1] "https://ropensci.r-universe.dev"
#> 
#> $ddsjoberg
#> [1] "https://ddsjoberg.r-universe.dev"
#> 
```
