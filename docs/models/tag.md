# Tag

## Example Usage

```typescript
import { Tag } from "@usemarble/sdk/models";

let value: Tag = {
  id: "clx789ghi",
  name: "JavaScript",
  slug: "javascript",
  description: "JavaScript tutorials",
  count: {
    posts: 8,
  },
};
```

## Fields

| Field                                    | Type                                     | Required                                 | Description                              | Example                                  |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| `id`                                     | *string*                                 | :heavy_check_mark:                       | N/A                                      | clx789ghi                                |
| `name`                                   | *string*                                 | :heavy_check_mark:                       | N/A                                      | JavaScript                               |
| `slug`                                   | *string*                                 | :heavy_check_mark:                       | N/A                                      | javascript                               |
| `description`                            | *string*                                 | :heavy_check_mark:                       | N/A                                      | JavaScript tutorials                     |
| `count`                                  | [models.TagCount](../models/tagcount.md) | :heavy_check_mark:                       | Number of published posts with this tag  |                                          |