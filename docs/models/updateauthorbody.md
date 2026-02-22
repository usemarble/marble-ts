# UpdateAuthorBody

## Example Usage

```typescript
import { UpdateAuthorBody } from "@usemarble/sdk/models";

let value: UpdateAuthorBody = {
  name: "John Doe",
  slug: "john-doe",
  bio: "Updated bio",
  role: "Senior Editor",
  email: "john@example.com",
  image: "https://media.marblecms.com/new-avatar.jpg",
  socials: [
    {
      platform: "x",
      url: "https://x.com/johndoe",
    },
  ],
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      | Example                                                          |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `name`                                                           | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              | John Doe                                                         |
| `slug`                                                           | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              | john-doe                                                         |
| `bio`                                                            | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              | Updated bio                                                      |
| `role`                                                           | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              | Senior Editor                                                    |
| `email`                                                          | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              | john@example.com                                                 |
| `image`                                                          | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              | https://media.marblecms.com/new-avatar.jpg                       |
| `socials`                                                        | [models.SocialInput](../models/socialinput.md)[]                 | :heavy_minus_sign:                                               | Social media links. Replaces all existing socials when provided. |                                                                  |