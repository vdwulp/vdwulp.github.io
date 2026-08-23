# Set RStudio Preferences

Updates RStudio preferences in `rstudio-prefs.json`.

## Usage

``` r
use_rstudio_prefs(...)
```

## Arguments

- ...:

  a series of RStudio preferences to update, e.g.
  `always_save_history = FALSE, rainbow_parentheses = TRUE`

## Value

Invisibly returns the updated preferences as a named list on success, or
`NULL` if no updates were made (no changes, user aborted, or not in an
interactive session).

## Details

Preference names, types, and allowed string values are validated against
the official RStudio preference definitions before applying changes. A
full listing of preferences is available in the [RStudio
documentation](https://docs.posit.co/ide/server-pro/admin/reference/session_user_settings.html).

## Author

Daniel D. Sjoberg (2021-2022)

S.A. van der Wulp (since 2026)

## Examples

``` r
if (FALSE) { # interactive()
# Pass preferences individually
use_rstudio_prefs(
  always_save_history = FALSE,
  rainbow_parentheses = TRUE
)

# Pass a list of preferences
pref_list <-
  list(always_save_history = FALSE,
       rainbow_parentheses = TRUE)

use_rstudio_prefs(!!!pref_list)
}
```
