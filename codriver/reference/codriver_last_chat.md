# Inspect the most recent chat

Returns the prompts and raw assistant response recorded for the most
recent codriver request in the current R session.

## Usage

``` r
codriver_last_chat()
```

## Value

A `codriver_last_chat` object or `NULL` if no chat has been recorded.
The object is a named list that may contain:

- system_prompt:

  The system prompt used for the request.

- user_prompt:

  The user prompt sent to the language model.

- assistant_response:

  The raw response returned by the language model.
