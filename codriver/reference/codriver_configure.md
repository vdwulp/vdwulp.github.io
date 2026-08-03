# Configure codriver

Set up the AI provider that codriver uses to generate and edit R code
and comments. The configuration is saved locally and validated
immediately by making a test call to the provider.

## Usage

``` r
codriver_configure(name, ...)
```

## Arguments

- name:

  Character. Provider name passed to
  [`ellmer::chat()`](https://ellmer.tidyverse.org/reference/chat-any.html),
  in the form `"provider"` or `"provider/model"`. Supported providers
  are listed on <https://ellmer.tidyverse.org/index.html#providers>.

- ...:

  Named arguments passed to the ellmer constructor, such as `model` or
  `base_url`.

## Value

Returns `TRUE` invisibly on successful provider configuration. Returns
`FALSE` invisibly if RStudio is not available or provider validation
fails.

## Details

Pass any arguments supported by the underlying
[`ellmer::chat()`](https://ellmer.tidyverse.org/reference/chat-any.html)
constructor directly via `name` and `...`.

If no keyboard shortcut is registered for codriver, the function offers
to register the default shortcut `Ctrl+/`. Shortcut registration is
strongly recommended but can be skipped or changed later via `Tools` \>
`Modify Keyboard Shortcuts` in RStudio.

## See also

- [`vignette("getting-started-with-codriver")`](https://vdwulp.github.io/codriver/articles/getting-started-with-codriver.md)
  for extended information on configuring codriver

- [`vignette("start-using-codriver")`](https://vdwulp.github.io/codriver/articles/start-using-codriver.md)
  for an overview of modes and result presentation

- [`ellmer::chat()`](https://ellmer.tidyverse.org/reference/chat-any.html)
  and supported providers at
  <https://ellmer.tidyverse.org/index.html#providers>

## Examples

``` r
if (FALSE) { # \dontrun{
  codriver_configure("openai", model = "gpt-4o")
  codriver_configure("openai_compatible/mistral", base_url = "http://localhost:1234/v1")
} # }
```
