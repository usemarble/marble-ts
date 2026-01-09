# AuthorRef

## Example Usage

```typescript
import { AuthorRef } from "@usemarble/sdk/models";

let value: AuthorRef = {
  id: "clx123abc",
  name: "John Doe",
  image: "https://cdn.example.com/avatar.jpg",
  bio: "Technical writer and developer",
  role: "Editor",
  slug: "john-doe",
  socials: [],
};
```

## Fields

| Field                                        | Type                                         | Required                                     | Description                                  | Example                                      |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `id`                                         | *string*                                     | :heavy_check_mark:                           | N/A                                          | clx123abc                                    |
| `name`                                       | *string*                                     | :heavy_check_mark:                           | N/A                                          | John Doe                                     |
| `image`                                      | *string*                                     | :heavy_check_mark:                           | N/A                                          | https://cdn.example.com/avatar.jpg           |
| `bio`                                        | *string*                                     | :heavy_check_mark:                           | N/A                                          | Technical writer and developer               |
| `role`                                       | *string*                                     | :heavy_check_mark:                           | N/A                                          | Editor                                       |
| `slug`                                       | *string*                                     | :heavy_check_mark:                           | N/A                                          | john-doe                                     |
| `socials`                                    | [models.SocialRef](../models/socialref.md)[] | :heavy_check_mark:                           | N/A                                          |                                              |