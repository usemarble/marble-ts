# GetV1PostsRequest

## Example Usage

```typescript
import { GetV1PostsRequest } from "@usemarble/sdk/models/operations";

let value: GetV1PostsRequest = {
  limit: 10,
  page: 1,
  categories: [
    "tech",
    "news",
  ],
  excludeCategories: [
    "changelog",
  ],
  tags: [
    "javascript",
    "react",
  ],
  excludeTags: [
    "outdated",
  ],
  query: "nextjs",
  format: "html",
  featured: "true",
};
```

## Fields

| Field                                                      | Type                                                       | Required                                                   | Description                                                | Example                                                    |
| ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| `limit`                                                    | *number*                                                   | :heavy_minus_sign:                                         | Number of posts per page (1-100)                           | 10                                                         |
| `page`                                                     | *number*                                                   | :heavy_minus_sign:                                         | Page number                                                | 1                                                          |
| `order`                                                    | [operations.Order](../../models/operations/order.md)       | :heavy_minus_sign:                                         | Sort order by publishedAt                                  | desc                                                       |
| `categories`                                               | *string*[]                                                 | :heavy_minus_sign:                                         | Category slugs to include                                  | [<br/>"tech",<br/>"news"<br/>]                             |
| `excludeCategories`                                        | *string*[]                                                 | :heavy_minus_sign:                                         | Category slugs to exclude                                  | [<br/>"changelog"<br/>]                                    |
| `tags`                                                     | *string*[]                                                 | :heavy_minus_sign:                                         | Tag slugs to include                                       | [<br/>"javascript",<br/>"react"<br/>]                      |
| `excludeTags`                                              | *string*[]                                                 | :heavy_minus_sign:                                         | Tag slugs to exclude                                       | [<br/>"outdated"<br/>]                                     |
| `query`                                                    | *string*                                                   | :heavy_minus_sign:                                         | Search query for title and content                         | nextjs                                                     |
| `format`                                                   | [models.ContentFormat](../../models/contentformat.md)      | :heavy_minus_sign:                                         | Content format (html or markdown)                          | html                                                       |
| `featured`                                                 | [operations.Featured](../../models/operations/featured.md) | :heavy_minus_sign:                                         | Filter by featured status                                  | true                                                       |