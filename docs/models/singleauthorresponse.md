# SingleAuthorResponse

## Example Usage

```typescript
import { SingleAuthorResponse } from "@usemarble/sdk/models";

let value: SingleAuthorResponse = {
  author: {
    id: "clx123abc",
    name: "John Doe",
    image: "https://cdn.example.com/avatar.jpg",
    slug: "john-doe",
    bio: "Technical writer and developer",
    role: "Editor",
    socials: [],
    count: {
      posts: 12,
    },
  },
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `author`                             | [models.Author](../models/author.md) | :heavy_check_mark:                   | N/A                                  |