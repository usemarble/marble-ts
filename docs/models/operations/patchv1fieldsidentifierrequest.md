# PatchV1FieldsIdentifierRequest

## Example Usage

```typescript
import { PatchV1FieldsIdentifierRequest } from "@usemarble/sdk/models/operations";

let value: PatchV1FieldsIdentifierRequest = {
  identifier: "audience",
  body: {
    key: "audience",
    name: "Audience",
    description: "Who this post is for",
    required: false,
    options: [
      {
        value: "developers",
        label: "Developers",
      },
      {
        value: "founders",
        label: "Founders",
      },
    ],
  },
};
```

## Fields

| Field                                                     | Type                                                      | Required                                                  | Description                                               | Example                                                   |
| --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| `identifier`                                              | *string*                                                  | :heavy_check_mark:                                        | Field ID or key                                           | audience                                                  |
| `body`                                                    | [models.UpdateFieldBody](../../models/updatefieldbody.md) | :heavy_check_mark:                                        | N/A                                                       |                                                           |