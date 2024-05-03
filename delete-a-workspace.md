[service-crawlr](../../../../README.md) / [API](../README.md) / [domains](./README.md) / Delete a workspace

# Delete a workspace

Delete a workspace to stop all domains refresh.

```text
DELETE /domains/
```

## Body

| Name          | Description             |
|---------------|-------------------------|
| `user`        | User doing the request. |

## Example

```text
DELETE /domains/

{
  "user": {
    "id": 1,
    "workspaces": [5],
    "role": "customer"
  }
}
```

Response

```text
200 Ok
```
