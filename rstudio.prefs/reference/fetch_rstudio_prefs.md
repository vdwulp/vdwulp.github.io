# Fetch table of RStudio Preferences

Preferences are fetched from
<https://docs.rstudio.com/ide/server-pro/session-user-settings.html>

## Usage

``` r
fetch_rstudio_prefs()
```

## Value

tibble

## Details

Only preferences of type `"boolean"`, `"string"`, `"number"`,
`"integer"`, and `"array"` are fetched from the table. TODO: Research
how type `"object"` are passed and include in the fetched preferences
table.

## Examples

``` r

fetch_rstudio_prefs()
#> ✔ Downloading list of available RStudio settings
#> 
#> # A tibble: 224 × 6
#>    property                           description  type  default class is_scalar
#>    <chr>                              <chr>        <chr> <chr>   <chr> <lgl>    
#>  1 allow_source_columns               Whether to … bool… true    logi… TRUE     
#>  2 always_enable_rnw_concordance      Whether to … bool… true    logi… TRUE     
#>  3 always_save_history                Whether to … bool… true    logi… TRUE     
#>  4 ansi_console_mode                  How to trea… stri… on      char… TRUE     
#>  5 auto_append_newline                Whether to … bool… false   logi… TRUE     
#>  6 auto_detect_indentation            Whether to … bool… false   logi… TRUE     
#>  7 auto_discover_package_dependencies Whether to … bool… true    logi… TRUE     
#>  8 auto_expand_error_tracebacks       Whether to … bool… false   logi… TRUE     
#>  9 auto_run_setup_chunk               Whether to … bool… true    logi… TRUE     
#> 10 auto_save_idle_ms                  The idle pe… inte… 1000    inte… TRUE     
#> # ℹ 214 more rows
```
