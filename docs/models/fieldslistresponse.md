# FieldsListResponse

## Example Usage

```typescript
import { FieldsListResponse } from "@usemarble/sdk/models";

let value: FieldsListResponse = {
  fields: [
    {
      id: "cryitfjp7890yz12abcdefg",
      key: "audience",
      name: "Audience",
      description: "Who this post is for",
      type: "multiselect",
      required: false,
      position: 0,
      options: [
        {
          id: "cryitfjp9012ab34cdefghij",
          value: "developers",
          label: "Developers",
          position: 0,
          createdAt: new Date("2024-01-15T10:00:00Z"),
          updatedAt: new Date("2024-01-16T12:00:00Z"),
        },
      ],
      createdAt: new Date("2024-01-15T10:00:00Z"),
      updatedAt: new Date("2024-01-16T12:00:00Z"),
    },
  ],
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `fields`                             | [models.Field](../models/field.md)[] | :heavy_check_mark:                   | N/A                                  |