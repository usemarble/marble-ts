# CreateAuthorBody

## Example Usage

```typescript
import { CreateAuthorBody } from "@usemarble/sdk/models";

let value: CreateAuthorBody = {
  name: "John Doe",
  slug: "john-doe",
  bio: "Technical writer and developer",
  role: "Editor",
  email: "john@example.com",
  image: "https://media.marblecms.com/avatar.jpg",
  socials: [
    {
      platform: "x",
      url: "https://x.com/johndoe",
    },
  ],
};
```

## Fields

| Field                                            | Type                                             | Required                                         | Description                                      | Example                                          |
| ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ |
| `name`                                           | *string*                                         | :heavy_check_mark:                               | N/A                                              | John Doe                                         |
| `slug`                                           | *string*                                         | :heavy_check_mark:                               | N/A                                              | john-doe                                         |
| `bio`                                            | *string*                                         | :heavy_minus_sign:                               | N/A                                              | Technical writer and developer                   |
| `role`                                           | *string*                                         | :heavy_minus_sign:                               | N/A                                              | Editor                                           |
| `email`                                          | *string*                                         | :heavy_minus_sign:                               | N/A                                              | john@example.com                                 |
| `image`                                          | *string*                                         | :heavy_minus_sign:                               | N/A                                              | https://media.marblecms.com/avatar.jpg           |
| `socials`                                        | [models.SocialInput](../models/socialinput.md)[] | :heavy_minus_sign:                               | Social media links for this author               |                                                  |