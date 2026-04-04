# PostResponse

## Example Usage

```typescript
import { PostResponse } from "@usemarble/sdk/models";

let value: PostResponse = {
  post: {
    id: "cryitfjp5678mn09qrstuvwx",
    slug: "getting-started-with-nextjs",
    title: "Getting Started with Next.js",
    status: "published",
    featured: false,
    coverImage: "https://media.marblecms.com/cover.jpg",
    description: "A beginner's guide to Next.js",
    publishedAt: new Date("2024-01-15T10:00:00Z"),
    updatedAt: new Date("2024-01-16T12:00:00Z"),
    authors: [],
    category: {
      id: "cryitfjp1234jl04vdnycek8",
      name: "Technology",
      slug: "technology",
      description: "Tech news and tutorials",
    },
    tags: [
      {
        id: "cryitfjp1234jl04vdnycek8",
        name: "JavaScript",
        slug: "javascript",
        description: "JavaScript tutorials",
      },
    ],
    fields: {
      "release_date": "2024-01-15",
      "priority_score": 5,
      "hashtags": [
        "#javascript",
        "#nextjs",
      ],
    },
    content: "<p>Hello world</p>",
  },
};
```

## Fields

| Field                            | Type                             | Required                         | Description                      |
| -------------------------------- | -------------------------------- | -------------------------------- | -------------------------------- |
| `post`                           | [models.Post](../models/post.md) | :heavy_check_mark:               | N/A                              |