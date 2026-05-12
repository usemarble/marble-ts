# PatchV1MediaIdRequest

## Example Usage

```typescript
import { PatchV1MediaIdRequest } from "@usemarble/sdk/models/operations";

let value: PatchV1MediaIdRequest = {
  id: "cryitfjp1234jl04vdnycek8",
  body: {
    name: "Updated hero image",
    alt: "Dashboard with a post editor open",
  },
};
```

## Fields

| Field                                                     | Type                                                      | Required                                                  | Description                                               | Example                                                   |
| --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| `id`                                                      | *string*                                                  | :heavy_check_mark:                                        | Media asset ID                                            | cryitfjp1234jl04vdnycek8                                  |
| `body`                                                    | [models.UpdateMediaBody](../../models/updatemediabody.md) | :heavy_check_mark:                                        | N/A                                                       |                                                           |