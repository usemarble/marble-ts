# PatchV1TagsIdentifierRequest

## Example Usage

```typescript
import { PatchV1TagsIdentifierRequest } from "@usemarble/sdk/models/operations";

let value: PatchV1TagsIdentifierRequest = {
  identifier: "javascript",
  body: {
    name: "TypeScript",
    slug: "typescript",
    description: "TypeScript tutorials and guides",
  },
};
```

## Fields

| Field                                                 | Type                                                  | Required                                              | Description                                           | Example                                               |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `identifier`                                          | *string*                                              | :heavy_check_mark:                                    | Tag ID or slug                                        | javascript                                            |
| `body`                                                | [models.UpdateTagBody](../../models/updatetagbody.md) | :heavy_check_mark:                                    | N/A                                                   |                                                       |