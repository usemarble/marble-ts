# CreatePostBody

## Example Usage

```typescript
import { CreatePostBody } from "@usemarble/sdk/models";

let value: CreatePostBody = {
  title: "Getting Started with Next.js",
  content: "<p>Hello world</p>",
  description: "A beginner's guide to Next.js",
  slug: "getting-started-with-nextjs",
  categoryId: "cryitfjp2345kl05weoybfk9",
  status: "draft",
  tags: [
    "cryitfjp4567no07ygqadhm1",
  ],
  authors: [
    "cryitfjp3456lm06xfpzcgl0",
  ],
  coverImage: "https://media.marblecms.com/cover.jpg",
  publishedAt: new Date("2024-01-15T10:00:00Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `title`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | Getting Started with Next.js                                                                  |
| `content`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | <p>Hello world</p>                                                                            |
| `description`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | A beginner's guide to Next.js                                                                 |
| `slug`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | getting-started-with-nextjs                                                                   |
| `categoryId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | cryitfjp2345kl05weoybfk9                                                                      |
| `status`                                                                                      | [models.CreatePostBodyStatus](../models/createpostbodystatus.md)                              | :heavy_check_mark:                                                                            | N/A                                                                                           | draft                                                                                         |
| `tags`                                                                                        | *string*[]                                                                                    | :heavy_minus_sign:                                                                            | Array of tag IDs to attach to the post                                                        | [<br/>"cryitfjp4567no07ygqadhm1"<br/>]                                                        |
| `authors`                                                                                     | *string*[]                                                                                    | :heavy_minus_sign:                                                                            | Array of author IDs. If omitted, the first workspace author is used.                          | [<br/>"cryitfjp3456lm06xfpzcgl0"<br/>]                                                        |
| `featured`                                                                                    | *boolean*                                                                                     | :heavy_minus_sign:                                                                            | N/A                                                                                           | false                                                                                         |
| `coverImage`                                                                                  | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           | https://media.marblecms.com/cover.jpg                                                         |
| `publishedAt`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | ISO 8601 datetime. Defaults to current time if omitted.                                       | 2024-01-15T10:00:00Z                                                                          |
| `attribution`                                                                                 | [models.CreatePostBodyAttribution](../models/createpostbodyattribution.md)                    | :heavy_minus_sign:                                                                            | Attribution to original author when republishing content                                      |                                                                                               |