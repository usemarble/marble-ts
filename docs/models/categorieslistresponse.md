# CategoriesListResponse

## Example Usage

```typescript
import { CategoriesListResponse } from "@usemarble/sdk/models";

let value: CategoriesListResponse = {
  categories: [],
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
| `categories`                                 | [models.Category](../models/category.md)[]   | :heavy_check_mark:                           | N/A                                          |
| `pagination`                                 | [models.Pagination](../models/pagination.md) | :heavy_check_mark:                           | N/A                                          |