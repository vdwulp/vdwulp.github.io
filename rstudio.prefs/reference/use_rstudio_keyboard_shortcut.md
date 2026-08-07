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
  that will execute. See examples.

- .write_json:

  logical indicating whether to update and overwrite the existing JSON
  file of options. Default is `TRUE`. When `FALSE`, the function will
  return a list of all options, instead of writing them to file.

- .backup:

  logical indicating whether to create a back-up of preferences file
  before it's updated. Default is `TRUE`

## Value

NULL, updates RStudio `addins.json` file

## Author

Daniel D. Sjoberg

## Examples

``` r
if (FALSE) { # interactive()
use_rstudio_keyboard_shortcut(
  "Ctrl+Shift+/" = "rstudio.prefs::make_path_norm"
)
}
```
