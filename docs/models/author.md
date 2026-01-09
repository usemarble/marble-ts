# Author

## Example Usage

```typescript
import { Author } from "@usemarble/sdk/models";

let value: Author = {
  id: "cryitfjp3456lm06xfpzcgl0",
  name: "John Doe",
  image: "https://media.marblecms.com/avatar.jpg",
  slug: "john-doe",
  bio: "Technical writer and developer",
  role: "Editor",
  socials: [
    {
      url: "https://twitter.com/johndoe",
      platform: "twitter",
    },
  ],
  count: {
    posts: 12,
  },
};
```

## Fields

| Field                                          | Type                                           | Required                                       | Description                                    | Example                                        |
| ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- |
| `id`                                           | *string*                                       | :heavy_check_mark:                             | N/A                                            | cryitfjp3456lm06xfpzcgl0                       |
| `name`                                         | *string*                                       | :heavy_check_mark:                             | N/A                                            | John Doe                                       |
| `image`                                        | *string*                                       | :heavy_check_mark:                             | N/A                                            | https://media.marblecms.com/avatar.jpg         |
| `slug`                                         | *string*                                       | :heavy_check_mark:                             | N/A                                            | john-doe                                       |
| `bio`                                          | *string*                                       | :heavy_check_mark:                             | N/A                                            | Technical writer and developer                 |
| `role`                                         | *string*                                       | :heavy_check_mark:                             | N/A                                            | Editor                                         |
| `socials`                                      | [models.Social](../models/social.md)[]         | :heavy_check_mark:                             | N/A                                            |                                                |
| `count`                                        | [models.AuthorCount](../models/authorcount.md) | :heavy_minus_sign:                             | Number of published posts by this author       |                                                |