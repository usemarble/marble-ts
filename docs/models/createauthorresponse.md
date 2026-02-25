# CreateAuthorResponse

## Example Usage

```typescript
import { CreateAuthorResponse } from "@usemarble/sdk/models";

let value: CreateAuthorResponse = {
  author: {
    id: "cryitfjp3456lm06xfpzcgl0",
    name: "John Doe",
    slug: "john-doe",
    bio: "Technical writer and developer",
    role: "Editor",
    image: "https://media.marblecms.com/avatar.jpg",
    socials: [
      {
        url: "https://twitter.com/johndoe",
        platform: "twitter",
      },
    ],
  },
};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `author`                                                                     | [models.CreateAuthorResponseAuthor](../models/createauthorresponseauthor.md) | :heavy_check_mark:                                                           | N/A                                                                          |