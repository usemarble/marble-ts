# FieldResponse

## Example Usage

```typescript
import { FieldResponse } from "@usemarble/sdk/models";

let value: FieldResponse = {
  field: {
    id: "cryitfjp7890yz12abcdefg",
    key: "audience",
    name: "Audience",
    description: "Who this post is for",
    type: "richtext",
    required: false,
    position: 0,
    options: [],
    createdAt: new Date("2024-01-15T10:00:00Z"),
    updatedAt: new Date("2024-01-16T12:00:00Z"),
  },
};
```

## Fields

| Field                              | Type                               | Required                           | Description                        |
| ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- |
| `field`                            | [models.Field](../models/field.md) | :heavy_check_mark:                 | N/A                                |