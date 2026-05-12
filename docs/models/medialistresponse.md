# MediaListResponse

## Example Usage

```typescript
import { MediaListResponse } from "@usemarble/sdk/models";

let value: MediaListResponse = {
  media: [],
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
| `media`                                      | [models.Media](../models/media.md)[]         | :heavy_check_mark:                           | N/A                                          |
| `pagination`                                 | [models.Pagination](../models/pagination.md) | :heavy_check_mark:                           | N/A                                          |