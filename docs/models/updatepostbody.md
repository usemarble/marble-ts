# UpdatePostBody

## Example Usage

```typescript
import { UpdatePostBody } from "@usemarble/sdk/models";

let value: UpdatePostBody = {
  title: "Updated Post Title",
  content: "<p>Updated content</p>",
  description: "Updated description",
  slug: "updated-post-slug",
  categoryId: "cryitfjp2345kl05weoybfk9",
  status: "published",
  tags: [
    "cryitfjp4567no07ygqadhm1",
  ],
  authors: [
    "cryitfjp3456lm06xfpzcgl0",
  ],
  featured: true,
  coverImage: "https://media.marblecms.com/new-cover.jpg",
  publishedAt: new Date("2024-02-01T10:00:00Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `title`                                                                                       | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           | Updated Post Title                                                                            |
| `content`                                                                                     | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           | <p>Updated content</p>                                                                        |
| `description`                                                                                 | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           | Updated description                                                                           |
| `slug`                                                                                        | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           | updated-post-slug                                                                             |
| `categoryId`                                                                                  | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           | cryitfjp2345kl05weoybfk9                                                                      |
| `status`                                                                                      | [models.UpdatePostBodyStatus](../models/updatepostbodystatus.md)                              | :heavy_minus_sign:                                                                            | N/A                                                                                           | published                                                                                     |
| `tags`                                                                                        | *string*[]                                                                                    | :heavy_minus_sign:                                                                            | Array of tag IDs. Replaces all existing tags when provided.                                   | [<br/>"cryitfjp4567no07ygqadhm1"<br/>]                                                        |
| `authors`                                                                                     | *string*[]                                                                                    | :heavy_minus_sign:                                                                            | Array of author IDs. Replaces all existing authors when provided.                             | [<br/>"cryitfjp3456lm06xfpzcgl0"<br/>]                                                        |
| `featured`                                                                                    | *boolean*                                                                                     | :heavy_minus_sign:                                                                            | N/A                                                                                           | true                                                                                          |
| `coverImage`                                                                                  | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           | https://media.marblecms.com/new-cover.jpg                                                     |
| `publishedAt`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | N/A                                                                                           | 2024-02-01T10:00:00Z                                                                          |
| `attribution`                                                                                 | [models.UpdatePostBodyAttribution](../models/updatepostbodyattribution.md)                    | :heavy_minus_sign:                                                                            | Attribution to original author when republishing content                                      |                                                                                               |