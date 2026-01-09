# GetV1PostsRequest

## Example Usage

```typescript
import { GetV1PostsRequest } from "@usemarble/sdk/models/operations";

let value: GetV1PostsRequest = {
  limit: 10,
  page: 1,
  categories: "tech,news",
  excludeCategories: "drafts",
  tags: "javascript,react",
  excludeTags: "outdated",
  query: "nextjs",
  format: "html",
};
```

## Fields

| Field                                                 | Type                                                  | Required                                              | Description                                           | Example                                               |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `limit`                                               | *number*                                              | :heavy_minus_sign:                                    | Number of posts per page (1-100)                      | 10                                                    |
| `page`                                                | *number*                                              | :heavy_minus_sign:                                    | Page number                                           | 1                                                     |
| `order`                                               | [operations.Order](../../models/operations/order.md)  | :heavy_minus_sign:                                    | Sort order by publishedAt                             | desc                                                  |
| `categories`                                          | *string*                                              | :heavy_minus_sign:                                    | Comma-separated category slugs to include             | tech,news                                             |
| `excludeCategories`                                   | *string*                                              | :heavy_minus_sign:                                    | Comma-separated category slugs to exclude             | drafts                                                |
| `tags`                                                | *string*                                              | :heavy_minus_sign:                                    | Comma-separated tag slugs to include                  | javascript,react                                      |
| `excludeTags`                                         | *string*                                              | :heavy_minus_sign:                                    | Comma-separated tag slugs to exclude                  | outdated                                              |
| `query`                                               | *string*                                              | :heavy_minus_sign:                                    | Search query for title and content                    | nextjs                                                |
| `format`                                              | [models.ContentFormat](../../models/contentformat.md) | :heavy_minus_sign:                                    | Content format (html or markdown)                     | html                                                  |