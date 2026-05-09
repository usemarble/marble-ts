# Media

## Example Usage

```typescript
import { Media } from "@usemarble/sdk/models";

let value: Media = {
  id: "cryitfjp1234jl04vdnycek8",
  name: "Hero image",
  url: "https://cdn.marblecms.com/media/hero.jpg",
  alt: "A dashboard screenshot",
  size: 382019,
  mimeType: "image/jpeg",
  width: 1600,
  height: 900,
  duration: 12000,
  blurHash: "LEHV6nWB2yk8pyo0adR*.7kCMdnj",
  type: "document",
  createdAt: new Date("2024-01-15T10:00:00Z"),
  updatedAt: new Date("2024-01-16T12:00:00Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | cryitfjp1234jl04vdnycek8                                                                      |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | Hero image                                                                                    |
| `url`                                                                                         | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | https://cdn.marblecms.com/media/hero.jpg                                                      |
| `alt`                                                                                         | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | A dashboard screenshot                                                                        |
| `size`                                                                                        | *number*                                                                                      | :heavy_check_mark:                                                                            | File size in bytes                                                                            | 382019                                                                                        |
| `mimeType`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | image/jpeg                                                                                    |
| `width`                                                                                       | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | 1600                                                                                          |
| `height`                                                                                      | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | 900                                                                                           |
| `duration`                                                                                    | *number*                                                                                      | :heavy_check_mark:                                                                            | Duration in milliseconds                                                                      | 12000                                                                                         |
| `blurHash`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | LEHV6nWB2yk8pyo0adR*.7kCMdnj                                                                  |
| `type`                                                                                        | [models.MediaType](../models/mediatype.md)                                                    | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           | 2024-01-15T10:00:00Z                                                                          |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           | 2024-01-16T12:00:00Z                                                                          |