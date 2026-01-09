# Category

## Example Usage

```typescript
import { Category } from "@usemarble/sdk/models";

let value: Category = {
  id: "clx456def",
  name: "Technology",
  slug: "technology",
  description: "Tech news and tutorials",
  count: {
    posts: 15,
  },
};
```

## Fields

| Field                                              | Type                                               | Required                                           | Description                                        | Example                                            |
| -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| `id`                                               | *string*                                           | :heavy_check_mark:                                 | N/A                                                | clx456def                                          |
| `name`                                             | *string*                                           | :heavy_check_mark:                                 | N/A                                                | Technology                                         |
| `slug`                                             | *string*                                           | :heavy_check_mark:                                 | N/A                                                | technology                                         |
| `description`                                      | *string*                                           | :heavy_check_mark:                                 | N/A                                                | Tech news and tutorials                            |
| `count`                                            | [models.CategoryCount](../models/categorycount.md) | :heavy_check_mark:                                 | Number of published posts in this category         |                                                    |