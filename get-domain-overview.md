[service-crawlr](../../../../README.md) / [API](../README.md) / [domains](./README.md) / Get domain overview

# Get domain overview

```text
GET /domains/:id_domain/overview
```

Fetch domain results overview. Query is available to filter, sort and page results.

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
GET /domains/zZM37777N1DZnwjIt60t/overview

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
  "data": {
    "ice_graph": {
      "lines": [
        {
          "value": 79.78620000000001,
          "date": "2024-04-15T15:03:45.145049+00:00"
        },
        {
          "value": 79.78620000000001,
          "date": "2024-03-15T15:03:45.145049+00:00"
        }
      ]
    },
    "warning_graph": {
      "lines": [
        {
          "value": 10136.0,
          "date": "2024-04-15T15:03:45.145049+00:00"
        },
        {
          "value": 10136.0,
          "date": "2024-03-15T15:03:45.145049+00:00"
        }
      ]
    },
    "opportunity_graph": {
      "lines": [
        {
          "value": 2415.0,
          "date": "2024-04-15T15:03:45.145049+00:00"
        },
        {
          "value": 2415.0,
          "date": "2024-03-15T15:03:45.145049+00:00"
        }
      ]
    },
    "issue_graph": {
      "lines": [
        {
          "value": 994.0,
          "date": "2024-04-15T15:03:45.145049+00:00"
        },
        {
          "value": 994.0,
          "date": "2024-03-15T15:03:45.145049+00:00"
        }
      ]
    },
    "reponses_codes": [
      {
        "URLs": "194",
        "response_code": "Success (2xx)"
      },
      {
        "URLs": "8",
        "response_code": "Redirection (3xx)"
      },
      {
        "URLs": "5",
        "response_code": "Client Error (4xx)"
      },
      {
        "URLs": "0",
        "response_code": "Server Error (5xx)"
      }
    ],
    "ice_score": 79.78620000000001,
    "domain_id": "zZM37777N1DZnwjIt60t"
  }
}
```
