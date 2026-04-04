# Post

## Example Usage

```typescript
import { Post } from "@usemarble/sdk/models";

let value: Post = {
  id: "cryitfjp5678mn09qrstuvwx",
  slug: "getting-started-with-nextjs",
  title: "Getting Started with Next.js",
  status: "published",
  featured: false,
  coverImage: "https://media.marblecms.com/cover.jpg",
  description: "A beginner's guide to Next.js",
  publishedAt: new Date("2024-01-15T10:00:00Z"),
  updatedAt: new Date("2024-01-16T12:00:00Z"),
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
  fields: {
    "release_date": "2024-01-15",
    "priority_score": 5,
    "hashtags": [
      "#javascript",
      "#nextjs",
    ],
  },
  content: "<p>Hello world</p>",
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     | Example                                                                                         |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `id`                                                                                            | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             | cryitfjp5678mn09qrstuvwx                                                                        |
| `slug`                                                                                          | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             | getting-started-with-nextjs                                                                     |
| `title`                                                                                         | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             | Getting Started with Next.js                                                                    |
| `status`                                                                                        | [models.PostStatus](../models/poststatus.md)                                                    | :heavy_check_mark:                                                                              | N/A                                                                                             | published                                                                                       |
| `featured`                                                                                      | *boolean*                                                                                       | :heavy_check_mark:                                                                              | N/A                                                                                             | false                                                                                           |
| `coverImage`                                                                                    | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             | https://media.marblecms.com/cover.jpg                                                           |
| `description`                                                                                   | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             | A beginner's guide to Next.js                                                                   |
| `publishedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)   | :heavy_check_mark:                                                                              | N/A                                                                                             | 2024-01-15T10:00:00Z                                                                            |
| `updatedAt`                                                                                     | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)   | :heavy_check_mark:                                                                              | N/A                                                                                             | 2024-01-16T12:00:00Z                                                                            |
| `authors`                                                                                       | [models.AuthorRef](../models/authorref.md)[]                                                    | :heavy_check_mark:                                                                              | N/A                                                                                             |                                                                                                 |
| `category`                                                                                      | [models.CategoryRef](../models/categoryref.md)                                                  | :heavy_check_mark:                                                                              | N/A                                                                                             |                                                                                                 |
| `tags`                                                                                          | [models.TagRef](../models/tagref.md)[]                                                          | :heavy_check_mark:                                                                              | N/A                                                                                             |                                                                                                 |
| `fields`                                                                                        | Record<string, *models.Fields*>                                                                 | :heavy_check_mark:                                                                              | Custom field values keyed by field key                                                          | {<br/>"release_date": "2024-01-15",<br/>"priority_score": 5,<br/>"hashtags": [<br/>"#javascript",<br/>"#nextjs"<br/>]<br/>} |
| `content`                                                                                       | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             | <p>Hello world</p>                                                                              |