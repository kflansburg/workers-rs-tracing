# `tracing` with `workers-rs`

Demonstrates using `tracing-web` to enable use of `tracing` crate on Cloudflare Workers.

Output looks like:

```json
➜  workers-rs-tracing git:(main) ✗ cat log | jq '.logs[] | .message[] | fromjson'
{
  "timestamp": "2023-06-13T20:48:44.744999936Z",
  "level": "WARN",
  "fields": {
    "message": "baz",
    "foo": "bar"
  },
  "target": "worker_rust",
  "span": {
    "name": "test"
  },
  "spans": [
    {
      "name": "test"
    }
  ]
}
```
