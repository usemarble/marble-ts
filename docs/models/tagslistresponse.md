# TagsListResponse

## Example Usage

```typescript
import { TagsListResponse } from "@usemarble/sdk/models";

let value: TagsListResponse = {
  tags: [
    {
      id: "cryitfjp4567no07ygqadhm1",
      name: "JavaScript",
      slug: "javascript",
      description: "JavaScript tutorials",
      count: {
        posts: 8,
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
| `tags`                                       | [models.Tag](../models/tag.md)[]             | :heavy_check_mark:                           | N/A                                          |
| `pagination`                                 | [models.Pagination](../models/pagination.md) | :heavy_check_mark:                           | N/A                                          |