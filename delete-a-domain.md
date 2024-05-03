[service-crawlr](../../../../README.md) / [API](../README.md) / [domains](./README.md) / Delete a domain

# Delete a domain

Delete an domain by its id to stop crawling a domain.

```text
DELETE /domains/:id_domain
```

## Parameters

| Name        | Description       |
|-------------|-------------------|
| `id_domain` | ID of the domain. |

## Body

| Name          | Description             |
|---------------|-------------------------|
| `user`        | User doing the request. |

## Example

```text
DELETE /domains/2JfWcKkRhLxGUXVk2IlK

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
204 No Content
```