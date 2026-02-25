# PatchV1AuthorsIdentifierRequest

## Example Usage

```typescript
import { PatchV1AuthorsIdentifierRequest } from "@usemarble/sdk/models/operations";

let value: PatchV1AuthorsIdentifierRequest = {
  identifier: "john-doe",
  body: {
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
  },
};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 | Example                                                     |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `identifier`                                                | *string*                                                    | :heavy_check_mark:                                          | Author ID or slug                                           | john-doe                                                    |
| `body`                                                      | [models.UpdateAuthorBody](../../models/updateauthorbody.md) | :heavy_check_mark:                                          | N/A                                                         |                                                             |