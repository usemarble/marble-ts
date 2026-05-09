# GetV1MediaRequest

## Example Usage

```typescript
import { GetV1MediaRequest } from "@usemarble/sdk/models/operations";

let value: GetV1MediaRequest = {
  query: "hero",
  type: "image",
};
```

## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              | Example                                                                  |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `limit`                                                                  | *number*                                                                 | :heavy_minus_sign:                                                       | Number of items per page (1-100)                                         | 10                                                                       |
| `page`                                                                   | *number*                                                                 | :heavy_minus_sign:                                                       | Page number                                                              | 1                                                                        |
| `query`                                                                  | *string*                                                                 | :heavy_minus_sign:                                                       | Search media by name, alt text, URL, or MIME type                        | hero                                                                     |
| `type`                                                                   | [operations.Type](../../models/operations/type.md)                       | :heavy_minus_sign:                                                       | Filter by inferred media type                                            | image                                                                    |
| `order`                                                                  | [operations.GetV1MediaOrder](../../models/operations/getv1mediaorder.md) | :heavy_minus_sign:                                                       | Sort order by creation date                                              | desc                                                                     |