# Fetch RStudio Preferences

Fetches the listing of supported preferences from the [RStudio
documentation](https://docs.posit.co/ide/server-pro/admin/reference/session_user_settings.html).

## Usage

``` r
fetch_rstudio_prefs()
```

## Value

A tibble containing the RStudio preference definitions.

## Details

Only preferences of type `"boolean"`, `"string"`, `"number"` and
`"integer"` are returned. Preferences of type `"array"` and `"object"`
are currently not supported and are ignored.

## Examples

``` r
fetch_rstudio_prefs()
#> ✔ Downloading list of available RStudio settings
#> 
#> # A tibble: 292 × 6
#>    property                      description       type  default class is_scalar
#>    <chr>                         <chr>             <chr> <chr>   <chr> <lgl>    
#>  1 air_formatter_require_toml    When set, Air wi… bool… false   logi… TRUE     
#>  2 allow_source_columns          Whether to enabl… bool… true    logi… TRUE     
#>  3 always_enable_rnw_concordance Whether to alway… bool… true    logi… TRUE     
#>  4 always_save_history           Whether to alway… bool… true    logi… TRUE     
#>  5 ansi_console_mode             How to treat ANS… stri… on      char… TRUE     
#>  6 assistant                     Select which AI … stri… posit   char… TRUE     
#>  7 assistant_completions_delay   The delay (in mi… inte… 300     inte… TRUE     
#>  8 assistant_completions_trigger Control when cod… stri… auto    char… TRUE     
#>  9 assistant_indexing_enabled    When enabled, RS… bool… false   logi… TRUE     
#> 10 assistant_nes_autoshow        When enabled, ne… bool… true    logi… TRUE     
#> # ℹ 282 more rows
```
