# GetV1TagsResponse

## Example Usage

```typescript
import { GetV1TagsResponse } from "@usemarble/sdk/models/operations";

let value: GetV1TagsResponse = {
  result: {
    tags: [],
    pagination: {
      limit: 10,
      currentPage: 1,
      nextPage: 2,
      previousPage: null,
      totalPages: 5,
      totalItems: 42,
    },
  },
};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `result`                                                    | [models.TagsListResponse](../../models/tagslistresponse.md) | :heavy_check_mark:                                          | N/A                                                         |