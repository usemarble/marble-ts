# SingleTagResponse

## Example Usage

```typescript
import { SingleTagResponse } from "@usemarble/sdk/models";

let value: SingleTagResponse = {
  tag: {
    id: "clx789ghi",
    name: "JavaScript",
    slug: "javascript",
    description: "JavaScript tutorials",
    count: {
      posts: 8,
    },
  },
};
```

## Fields

| Field                          | Type                           | Required                       | Description                    |
| ------------------------------ | ------------------------------ | ------------------------------ | ------------------------------ |
| `tag`                          | [models.Tag](../models/tag.md) | :heavy_check_mark:             | N/A                            |