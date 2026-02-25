# PatchV1CategoriesIdentifierRequest

## Example Usage

```typescript
import { PatchV1CategoriesIdentifierRequest } from "@usemarble/sdk/models/operations";

let value: PatchV1CategoriesIdentifierRequest = {
  identifier: "technology",
  body: {
    name: "Engineering",
    slug: "engineering",
    description: "Engineering articles and tutorials",
  },
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     | Example                                                         |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `identifier`                                                    | *string*                                                        | :heavy_check_mark:                                              | Category ID or slug                                             | technology                                                      |
| `body`                                                          | [models.UpdateCategoryBody](../../models/updatecategorybody.md) | :heavy_check_mark:                                              | N/A                                                             |                                                                 |