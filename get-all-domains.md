[service-crawlr](../../../../README.md) / [API](../README.md) / [domains](./README.md) / Get all domains

# Get all domains

Fetch domains settings. Query is available to filter, sort and page results

```text
GET /domains
```

## Body

| Name          | Description             |
|---------------|-------------------------|
| `user`        | User doing the request. |

## Example

```text
GET /domains

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
200 OK
```

```json
{
  "data": [
    {
      "refresh": "now",
      "url": "https://www.entrechiens.fr/",
      "lastUpdate": "2024-04-11T12:40:52.748Z",
      "workspace_id": 5,
      "creation_date": "2024-04-09T15:09:03.435000+00:00",
      "deleted_at": null,
      "status": "finished",
      "next_run_at": null,
      "deleted": false,
      "count_issues": 47,
      "last_score": 73.0382,
      "id_domain": "8FkcI898mZtyK1QTQn0s",
      "user_id": 2
    },
    {
      "refresh": "now",
      "url": "https://www.entrechiens.fr/",
      "next_run_at": null,
      "workspace_id": 5,
      "creation_date": "2024-04-15T12:38:03.876000+00:00",
      "deleted_at": null,
      "status": "finished",
      "lastUpdate": "2024-04-15T12:59:49.356Z",
      "deleted": false,
      "count_issues": 44,
      "last_score": 57.394,
      "id_domain": "rG8BEDOUp2eh7gchxTgx",
      "user_id": 2
    }
  ],
  "count": 10,
  "page": 1,
  "total": 1,
  "pageCount": 1
}
```
