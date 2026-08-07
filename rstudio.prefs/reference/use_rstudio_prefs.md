# Set RStudio Preferences

This function updates the RStudio preferences saved in the
`rstudio-prefs.json` file. A full listing of preferences that may be
modified are listed here
<https://docs.posit.co/ide/server-pro/admin/reference/session_user_settings.html>

## Usage

``` r
use_rstudio_prefs(...)
```

## Arguments

- ...:

  series of RStudio preferences to update, e.g.
  `always_save_history = FALSE, rainbow_parentheses = TRUE`

## Value

Invisibly returns the updated preferences as a named list on success, or
`NULL` if no updates were made (no changes, user aborted, or not in an

## Author

Daniel D. Sjoberg

## Examples

``` r
if (FALSE) { # interactive()
# pass preferences individually --------------
use_rstudio_prefs(
  always_save_history = FALSE,
  rainbow_parentheses = TRUE
)

# pass a list of preferences -----------------
pref_list <-
  list(always_save_history = FALSE,
       rainbow_parentheses = TRUE)

use_rstudio_prefs(!!!pref_list)
}
```
