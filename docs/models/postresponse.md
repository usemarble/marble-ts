# PostResponse

## Example Usage

```typescript
import { PostResponse } from "@usemarble/sdk/models";

let value: PostResponse = {
  post: {
    id: "cryitfjp5678mn09qrstuvwx",
    slug: "getting-started-with-nextjs",
    title: "Getting Started with Next.js",
    content: "<p>Hello world</p>",
    featured: false,
    coverImage: "https://media.marblecms.com/cover.jpg",
    description: "A beginner's guide to Next.js",
    publishedAt: new Date("2024-01-15T10:00:00Z"),
    updatedAt: new Date("2024-01-16T12:00:00Z"),
    attribution: {
      author: "John Doe",
      url: "https://original-source.com/article",
    },
    authors: [
      {
        id: "cryitfjp1234jl04vdnycek8",
        name: "John Doe",
        image: "https://media.marblecms.com/avatar.jpg",
        bio: "Technical writer and developer",
        role: "Editor",
        slug: "john-doe",
        socials: [],
      },
    ],
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
  },
};
```

## Fields

| Field                            | Type                             | Required                         | Description                      |
| -------------------------------- | -------------------------------- | -------------------------------- | -------------------------------- |
| `post`                           | [models.Post](../models/post.md) | :heavy_check_mark:               | N/A                              |