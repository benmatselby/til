# Quotes Matter

I think this is probably always the case in many languages, but it caught me out
today (28th July 2025).

If you have a log line that is something like like:

```text
ERR-ABC-123: Something went wrong
```

Using terraform to show the error. If you use a `'` quote, it would match different things

```terraform
resource "datadog_monitor" "my_new_monitor" {
  name    = "${var.prefix}: Monitor for error"
  type    = "log alert"
  query   = "logs(\"env:test AND 'ERR-ABC-123'\").index(\"*\").rollup(\"count\").last(\"5m\") > 0"
  message = "my alert message"
  ...
}
```

So could match `ERR-A-123` for example.

If you want an exact match, you need to use `"` quotes:

```terraform
resource "datadog_monitor" "my_new_monitor" {
  name    = "${var.prefix}: Monitor for error"
  type    = "log alert"
  query   = "logs(\"env:test AND \"ERR-ABC-123\"\").index(\"*\").rollup(\"count\").last(\"5m\") > 0"
  message = "my alert message"
  ...
}
```
