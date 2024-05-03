[service-crawlr](../../../../README.md) / [API](../README.md) / [domains](./README.md) / Get domain issue file

# Get domain issues file

Fetch detailed results specified on a file.

```text
GET /domains/:id_domain/issue-files/:filename
```

## Parameters

| Name        | Description                           |
|-------------|---------------------------------------|
| `id_domain` | ID of the domain.                     |
| `filename`  | issue_name in the response of domain. |

## Body

| Name          | Description             |
|---------------|-------------------------|
| `user`        | User doing the request. |

## Example

```text
GET /domains/2JfWcKkRhLxGUXVk2IlK/issue-file/response_codes_internal_no_response

{
  "user": {
    "worskpace_id": 123
  }
}
```

Response

```text
200 OK
```

```text

"Address","Content Type","Status Code","Status","Indexability","Indexability Status"
"https://www.eskimoz.fr/politique-de-confidentialite/","text/html; charset=UTF-8","200","OK","Non-Indexable","Blocked by robots.txt"
"https://www.eskimoz.fr/category/data/","text/html; charset=UTF-8","302","Found","Non-Indexable","Blocked by robots.txt"
"https://www.eskimoz.fr/category/content/","text/html; charset=UTF-8","302","Found","Non-Indexable","Blocked by robots.txt"
"https://www.eskimoz.fr/category/seo/","text/html; charset=UTF-8","302","Found","Non-Indexable","Blocked by robots.txt"
"https://www.eskimoz.fr/category/paid/","text/html; charset=UTF-8","302","Found","Non-Indexable","Blocked by robots.txt"
```