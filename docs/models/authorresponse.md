# AuthorResponse

## Example Usage

```typescript
import { AuthorResponse } from "@usemarble/sdk/models";

let value: AuthorResponse = {
  author: {
    id: "cryitfjp3456lm06xfpzcgl0",
    name: "John Doe",
    image: "https://media.marblecms.com/avatar.jpg",
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