# SingleCategoryResponse

## Example Usage

```typescript
import { SingleCategoryResponse } from "@usemarble/sdk/models";

let value: SingleCategoryResponse = {
  category: {
    id: "clx456def",
    name: "Technology",
    slug: "technology",
    description: "Tech news and tutorials",
    count: {
      posts: 15,
    },
  },
};
```

## Fields

| Field                                    | Type                                     | Required                                 | Description                              |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| `category`                               | [models.Category](../models/category.md) | :heavy_check_mark:                       | N/A                                      |