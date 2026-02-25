# Post

## Example Usage

```typescript
import { Post } from "@usemarble/sdk/models";

let value: Post = {
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
  tags: [],
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | cryitfjp5678mn09qrstuvwx                                                                      |
| `slug`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | getting-started-with-nextjs                                                                   |
| `title`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | Getting Started with Next.js                                                                  |
| `content`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | <p>Hello world</p>                                                                            |
| `featured`                                                                                    | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           | false                                                                                         |
| `coverImage`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | https://media.marblecms.com/cover.jpg                                                         |
| `description`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | A beginner's guide to Next.js                                                                 |
| `publishedAt`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           | 2024-01-15T10:00:00Z                                                                          |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           | 2024-01-16T12:00:00Z                                                                          |
| `attribution`                                                                                 | [models.PostAttribution](../models/postattribution.md)                                        | :heavy_check_mark:                                                                            | Attribution to the original author when republishing content                                  |                                                                                               |
| `authors`                                                                                     | [models.AuthorRef](../models/authorref.md)[]                                                  | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `category`                                                                                    | [models.CategoryRef](../models/categoryref.md)                                                | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `tags`                                                                                        | [models.TagRef](../models/tagref.md)[]                                                        | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |