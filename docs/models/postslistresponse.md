# PostsListResponse

## Example Usage

```typescript
import { PostsListResponse } from "@usemarble/sdk/models";

let value: PostsListResponse = {
  posts: [],
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
| `posts`                                      | [models.Post](../models/post.md)[]           | :heavy_check_mark:                           | N/A                                          |
| `pagination`                                 | [models.Pagination](../models/pagination.md) | :heavy_check_mark:                           | N/A                                          |