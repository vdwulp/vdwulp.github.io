# Inspect the most recent codriver request

Returns the prompts and raw assistant response recorded for the most
recent codriver request in the current R session.

## Usage

``` r
codriver_last_request()
```

## Value

A `codriver_last_request` object or `NULL` if no request has been
recorded. The object is a named list that may contain:

- system_prompt:

  The system prompt used for the request.

- user_prompt:

  The user prompt sent to the language model.

- assistant_response:

  The raw response returned by the language model.
