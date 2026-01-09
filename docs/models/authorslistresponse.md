# AuthorsListResponse

## Example Usage

```typescript
import { AuthorsListResponse } from "@usemarble/sdk/models";

let value: AuthorsListResponse = {
  authors: [
    {
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
  ],
  pagination: {
    limit: 10,
    currentPage: 1,
    nextPage: 2,
    previousPage: null,
    totalPages: 5,
    totalItems: 42,
  },
};
```

## Fields

| Field                                        | Type                                         | Required                                     | Description                                  |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `authors`                                    | [models.Author](../models/author.md)[]       | :heavy_check_mark:                           | N/A                                          |
| `pagination`                                 | [models.Pagination](../models/pagination.md) | :heavy_check_mark:                           | N/A                                          |