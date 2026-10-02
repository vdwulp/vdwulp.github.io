# Normalize Path RStudio Addin

Wrapper to execute
[`fs::path_norm()`](https://fs.r-lib.org/reference/path_math.html) as a
shortcut on highlighted text. The updated text will be converted in
place to a path normalized for the environment currently in use. For
instance, \\ or \\ will be converted to / on Windows machines. See below
for process of setting a shortcut.

## Usage

``` r
make_path_norm()
```

## Details

To add a keyboard shortcut for `make_path_norm()` in RStudio, use the
[`use_rstudio_keyboard_shortcut()`](https://vdwulp.github.io/rstudio.prefs/reference/use_rstudio_keyboard_shortcut.md)
function as shown in the example. This demonstrates the use of
`rstudio.prefs` to set a keyboard shortcut.

To add a keyboard shortcut manually, follow these steps:

- Install rstudio.prefs,

- Restart RStudio,

- Select `Tools` \> `Modify Keyboard Shortcuts...`,

- In the `Search` box, type `Make Path Normal`,

- In the `Shortcut` column click on the `Make Path Normal` row,

- Press intended shortcut keys to set shortcut (suggested:
  `Ctrl+Shift+/`).

NOTE: It is possible to override a previously specified key combination
with this selection.

## See also

[fs::path_norm](https://fs.r-lib.org/reference/path_math.html)

## Examples

``` r
if (interactive()) {
  # Set a keyboard shortcut for path normalization
  rstudio.prefs::use_rstudio_keyboard_shortcut(
    "Ctrl+Shift+/" = "rstudio.prefs::make_path_norm"
  )
}
```
