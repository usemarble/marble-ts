# GetV1CategoriesResponse

## Example Usage

```typescript
import { GetV1CategoriesResponse } from "@usemarble/sdk/models/operations";

let value: GetV1CategoriesResponse = {
  result: {
    categories: [],
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

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `result`                                                                | [models.CategoriesListResponse](../../models/categorieslistresponse.md) | :heavy_check_mark:                                                      | N/A                                                                     |