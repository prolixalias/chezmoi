# `promptString` *prompt* [*default*]

`promptString` prompts the user with *prompt* and returns the user's response
with all leading and trailing spaces stripped. If *default* is passed and the
user's response is empty then it returns *default*. It is only available when
generating the initial config file.

!!! example

    ```
    {{ $email := promptString "email" -}}
    [data]
        email = {{ $email | quote }}
    ```
