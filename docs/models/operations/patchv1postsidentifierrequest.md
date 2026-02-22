# PatchV1PostsIdentifierRequest

## Example Usage

```typescript
import { PatchV1PostsIdentifierRequest } from "@usemarble/sdk/models/operations";

let value: PatchV1PostsIdentifierRequest = {
  identifier: "my-post-slug",
  body: {
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
  },
};
```

## Fields

| Field                                                   | Type                                                    | Required                                                | Description                                             | Example                                                 |
| ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- |
| `identifier`                                            | *string*                                                | :heavy_check_mark:                                      | Post ID or slug                                         | my-post-slug                                            |
| `body`                                                  | [models.UpdatePostBody](../../models/updatepostbody.md) | :heavy_check_mark:                                      | N/A                                                     |                                                         |