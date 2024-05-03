[service-crawlr](../../../../README.md) / [API](../README.md) / [domains](./README.md) / Add a domain

# Add a domain

Add a domain, starting a first Crawlr process to being able to fetch results.

```text
POST /domains
```

## Body

| Name          | Description                               |
|---------------|-------------------------------------------|
| `user`        | User doing the request.                   |
| `url`         | Url of the domain to crawl.               |
| `refresh`     | Choice for update (now, weekly, monthly). |

## Example

```text
POST /customers/123/domains

{
  "user": {
    "id": 1,
    "workspaces": [5],
    "role": "customer"
  },
  "name": "eskimoz",
  "url": "https://www.eskimoz.fr",
  "refresh": "now"
}
```

Response

```text
201 Created
```
{
  "user": {
    "id": 1,
    "workspaces": [
      5
    ],
    "role": "customer"
  },
  "url": "https://www.eskimoz.fr",
  "refresh": "now"
}