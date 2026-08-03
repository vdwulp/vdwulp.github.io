# Context-aware AI assistant for RStudio

Inspects the current editor context — cursor position and any selection
— and automatically chooses and executes one of five modes: complete,
continue, generate, edit, or comment. Results are presented as ghost
text or an edit suggestion directly in the source editor.

## Usage

``` r
codriver()
```

## Value

Returns `TRUE` invisibly on success. Returns `FALSE` invisibly if
RStudio is not available, no configuration is found, or the mode cannot
be resolved.

## Details

Codriver is intended to be invoked via a keyboard shortcut **Ctrl+/**
(default) or the RStudio **Addins** menu, not called directly. Use
[`codriver_configure()`](https://vdwulp.github.io/codriver/reference/codriver_configure.md)
to set up a provider and register the recommended shortcut before first
use.

## See also

- [`codriver_configure()`](https://vdwulp.github.io/codriver/reference/codriver_configure.md)
  to set up the LLM provider and recommended keyboard shortcut

- [`vignette("getting-started-with-codriver")`](https://vdwulp.github.io/codriver/articles/getting-started-with-codriver.md)
  for extended information on configuring codriver

- [`vignette("start-using-codriver")`](https://vdwulp.github.io/codriver/articles/start-using-codriver.md)
  for an overview of modes and result presentation
