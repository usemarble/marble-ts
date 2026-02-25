# CreateAuthorResponseAuthor

## Example Usage

```typescript
import { CreateAuthorResponseAuthor } from "@usemarble/sdk/models";

let value: CreateAuthorResponseAuthor = {
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
};
```

## Fields

| Field                                  | Type                                   | Required                               | Description                            | Example                                |
| -------------------------------------- | -------------------------------------- | -------------------------------------- | -------------------------------------- | -------------------------------------- |
| `id`                                   | *string*                               | :heavy_check_mark:                     | N/A                                    | cryitfjp3456lm06xfpzcgl0               |
| `name`                                 | *string*                               | :heavy_check_mark:                     | N/A                                    | John Doe                               |
| `slug`                                 | *string*                               | :heavy_check_mark:                     | N/A                                    | john-doe                               |
| `bio`                                  | *string*                               | :heavy_check_mark:                     | N/A                                    | Technical writer and developer         |
| `role`                                 | *string*                               | :heavy_check_mark:                     | N/A                                    | Editor                                 |
| `image`                                | *string*                               | :heavy_check_mark:                     | N/A                                    | https://media.marblecms.com/avatar.jpg |
| `socials`                              | [models.Social](../models/social.md)[] | :heavy_check_mark:                     | N/A                                    |                                        |