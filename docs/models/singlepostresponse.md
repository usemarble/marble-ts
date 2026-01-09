# SinglePostResponse

## Example Usage

```typescript
import { SinglePostResponse } from "@usemarble/sdk/models";

let value: SinglePostResponse = {
  post: {
    id: "clx000post",
    slug: "getting-started-with-nextjs",
    title: "Getting Started with Next.js",
    content: "<p>Hello world</p>",
    featured: false,
    coverImage: "https://cdn.example.com/cover.jpg",
    description: "A beginner's guide to Next.js",
    publishedAt: new Date("2024-01-15T10:00:00Z"),
    updatedAt: new Date("2024-01-16T12:00:00Z"),
    attribution: {
      author: "John Doe",
      url: "https://original-source.com/article",
    },
    authors: [],
    category: {
      id: "clx456def",
      name: "Technology",
      slug: "technology",
      description: "Tech news and tutorials",
    },
    tags: [
      {
        id: "clx789ghi",
        name: "JavaScript",
        slug: "javascript",
        description: "JavaScript tutorials",
      },
    ],
  },
};
```

## Fields

| Field                            | Type                             | Required                         | Description                      |
| -------------------------------- | -------------------------------- | -------------------------------- | -------------------------------- |
| `post`                           | [models.Post](../models/post.md) | :heavy_check_mark:               | N/A                              |