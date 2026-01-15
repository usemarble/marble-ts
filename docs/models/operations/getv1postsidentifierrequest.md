# GetV1PostsIdentifierRequest

## Example Usage

```typescript
import { GetV1PostsIdentifierRequest } from "@usemarble/sdk/models/operations";

let value: GetV1PostsIdentifierRequest = {
  identifier: "my-post-slug",
  format: "html",
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              | Example                                                                                                  |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `identifier`                                                                                             | *string*                                                                                                 | :heavy_check_mark:                                                                                       | Post ID or slug                                                                                          | my-post-slug                                                                                             |
| `format`                                                                                                 | [models.ContentFormat](../../models/contentformat.md)                                                    | :heavy_minus_sign:                                                                                       | Content format (html or markdown)                                                                        | html                                                                                                     |
| `status`                                                                                                 | [operations.GetV1PostsIdentifierStatus](../../models/operations/getv1postsidentifierstatus.md)           | :heavy_minus_sign:                                                                                       | Filter by post status. Use 'published' for live posts, 'draft' for unpublished posts, or 'all' for both. | published                                                                                                |