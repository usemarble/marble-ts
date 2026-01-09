# Pagination

## Example Usage

```typescript
import { Pagination } from "@usemarble/sdk/models";

let value: Pagination = {
  limit: 10,
  currentPage: 1,
  nextPage: 2,
  previousPage: null,
  totalPages: 5,
  totalItems: 42,
};
```

## Fields

| Field              | Type               | Required           | Description        | Example            |
| ------------------ | ------------------ | ------------------ | ------------------ | ------------------ |
| `limit`            | *number*           | :heavy_check_mark: | N/A                | 10                 |
| `currentPage`      | *number*           | :heavy_check_mark: | N/A                | 1                  |
| `nextPage`         | *number*           | :heavy_check_mark: | N/A                | 2                  |
| `previousPage`     | *number*           | :heavy_check_mark: | N/A                | <nil>              |
| `totalPages`       | *number*           | :heavy_check_mark: | N/A                | 5                  |
| `totalItems`       | *number*           | :heavy_check_mark: | N/A                | 42                 |