# AuthorRef

## Example Usage

```typescript
import { AuthorRef } from "@usemarble/sdk/models";

let value: AuthorRef = {
  id: "cryitfjp1234jl04vdnycek8",
  name: "John Doe",
  image: "https://media.marblecms.com/avatar.jpg",
  bio: "Technical writer and developer",
  role: "Editor",
  slug: "john-doe",
  socials: [],
};
```

## Fields

| Field                                        | Type                                         | Required                                     | Description                                  | Example                                      |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `id`                                         | *string*                                     | :heavy_check_mark:                           | N/A                                          | cryitfjp1234jl04vdnycek8                     |
| `name`                                       | *string*                                     | :heavy_check_mark:                           | N/A                                          | John Doe                                     |
| `image`                                      | *string*                                     | :heavy_check_mark:                           | N/A                                          | https://media.marblecms.com/avatar.jpg       |
| `bio`                                        | *string*                                     | :heavy_check_mark:                           | N/A                                          | Technical writer and developer               |
| `role`                                       | *string*                                     | :heavy_check_mark:                           | N/A                                          | Editor                                       |
| `slug`                                       | *string*                                     | :heavy_check_mark:                           | N/A                                          | john-doe                                     |
| `socials`                                    | [models.SocialRef](../models/socialref.md)[] | :heavy_check_mark:                           | N/A                                          |                                              |