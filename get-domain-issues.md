[service-crawlr](../../../../README.md) / [API](../README.md) / [domains](./README.md) / Get domain issues

# Get domain issues

```text
GET /domains/:id_domain/issues
```

Fetch domain issues cards. Query is available to filter, sort and page results.

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
  "data": [
{
      "issue_type": "Opportunity",
      "urls": 41,
      "how_to_fix": "Review the missing anchor text outlinks and where appropriate include useful and descriptive anchor text to help users and search engines.",
      "description": "Pages that have internal links without anchor text or images that are hyperlinked without alt text. Anchor text is the visible text and words used in hyperlinks that provide users and search engines context about the content of the target page. Internal outlinks without anchor text can be seen in the 'Outlinks' tab, with the 'All Link Types' filter set to 'Hyperlinks', where the 'Anchor Text' column is blank, or if an image, the 'Alt Text' column is also blank. Export in bulk via 'Bulk Export > Links > Internal Outlinks With No Anchor Text'.",
      "percent_of_total": 100.0,
      "issue_priority": "Low",
      "score": -4.0,
      "issue_name": "Links: Internal Outlinks With No Anchor Text"
    },
    {
      "issue_type": "Warning",
      "urls": 20,
      "how_to_fix": "Having very similar pages can cause cannibalisation issues and crawling and indexing inefficiencies. Very similar pages should be minimised and high similarity could be a sign of low-quality pages, which haven't received much love - or just shouldn't be separate pages in the first place. Analyse the near duplicates, considering importance of the page and scale. Then improve content to make more unique if necessary, or consolidate, block, remove, or leave as they are where appropriate.",
      "description": "Pages that are near duplicate in content based upon the configured similarity threshold using the minhash algorithm. The threshold can be adjusted under 'Config > Content > Duplicates' and is set at 90% by default. The 'Closest Similarity Match' column displays the highest percentage of similarity to another page. The 'No. Near Duplicates' column displays the number of pages that are similar to the page based upon the similarity threshold. The algorithm is run against text on the page, rather than the full HTML like exact duplicates. The content used for this analysis can be configured under 'Config > Content > Area'. Pages can have a 100% similarity, but only be a 'near duplicate' rather than exact duplicate. This is because exact duplicates are excluded as near duplicates, to avoid them being flagged twice. Similarity scores are also rounded, so 99.5% or higher will be displayed as 100%. To populate this column the 'Enable Near Duplicates' configuration must be selected via 'Config > Content > Duplicates', and post 'Crawl Analysis' must be performed.",
      "percent_of_total": 48.78,
      "issue_priority": "Medium",
      "score": -3.9024,
      "issue_name": "Content: Near Duplicates"
    }
  ],
  "count": 2,
  "page": 1,
  "total": 28,
  "pageCount": 14
}
```
