[service-crawlr](../../../../README.md) / [API](../README.md) / [domains](./README.md) / Modify a domain

# Modify a domain

Modify a domain set up, starting a Crawlr process to being able to fetch results with modify settings.

```text
PUT /domains/:id_domain
```

## Parameters

| Name        | Description       |
|-------------|-------------------|
| `id_domain` | ID of the domain. |

## Body

| Name          | Description                               |
|---------------|-------------------------------------------|
| `user`        | User doing the request.                   |
| `refresh`     | Choice for update (now, weekly, monthly). |

## Example

```text
PUT /domains/2JfWcKkRhLxGUXVk2IlK

{
  "user": {
    "id": 1,
    "workspaces": [5],
    "role": "customer"
  },
  "refresh": "now"
}
```

Response

```text
200 Ok
```

```json
{
  "user": {
    "id": 1,
    "workspaces": [
      5
    ],
    "role": "customer"
  },
  "refresh": "now"
}
```
