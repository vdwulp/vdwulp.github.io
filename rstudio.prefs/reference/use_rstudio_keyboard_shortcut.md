# Set RStudio Keyboard Shortcuts

This function updates the RStudio keyboard shortcuts saved in the
`addins.json` file.

## Usage

``` r
use_rstudio_keyboard_shortcut(..., .write_json = TRUE, .backup = TRUE)
```

## Arguments

- ...:

  series of RStudio keyboard shortcuts to update. The argument name is
  the keyboard shortcut, and the value is a string of the function name
  that will execute, or `NULL` to remove the shortcut. If a new shortcut
  shares a key or function with an existing one, the previous binding is
  removed.

- .write_json:

  logical indicating whether to update and overwrite the existing JSON
  file of options. Default is `TRUE`. When `FALSE`, the function will
  return a list of all shortcuts, instead of writing them to file.

- .backup:

  logical indicating whether to create a back-up of shortcuts file
  before it's updated. Default is `TRUE`.

## Value

When `.write_json = FALSE`, a named list of all shortcuts including the
updates. Otherwise `NULL` invisibly.

## Author

Daniel D. Sjoberg

## Examples

``` r
if (FALSE) { # interactive()
# Add a shortcut
use_rstudio_keyboard_shortcut(
  "Ctrl+Shift+/" = "rstudio.prefs::make_path_norm"
)

# Remove a shortcut
use_rstudio_keyboard_shortcut(
  "Ctrl+Shift+/" = NULL
)
}
```
