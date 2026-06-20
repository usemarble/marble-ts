# UpdateFieldBody

## Example Usage

```typescript
import { UpdateFieldBody } from "@usemarble/sdk/models";

let value: UpdateFieldBody = {
  key: "audience",
  name: "Audience",
  description: "Who this post is for",
  required: false,
  options: [
    {
      value: "developers",
      label: "Developers",
    },
    {
      value: "founders",
      label: "Founders",
    },
  ],
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        | Example                                                                                            |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `key`                                                                                              | *string*                                                                                           | :heavy_minus_sign:                                                                                 | N/A                                                                                                | audience                                                                                           |
| `name`                                                                                             | *string*                                                                                           | :heavy_minus_sign:                                                                                 | N/A                                                                                                | Audience                                                                                           |
| `description`                                                                                      | *string*                                                                                           | :heavy_minus_sign:                                                                                 | N/A                                                                                                | Who this post is for                                                                               |
| `type`                                                                                             | [models.FieldType](../models/fieldtype.md)                                                         | :heavy_minus_sign:                                                                                 | N/A                                                                                                |                                                                                                    |
| `required`                                                                                         | *boolean*                                                                                          | :heavy_minus_sign:                                                                                 | N/A                                                                                                | false                                                                                              |
| `options`                                                                                          | [models.FieldOptionInput](../models/fieldoptioninput.md)[]                                         | :heavy_minus_sign:                                                                                 | Replacement option list. Only valid for select and multiselect fields.                             | [<br/>{<br/>"value": "developers",<br/>"label": "Developers"<br/>},<br/>{<br/>"value": "founders",<br/>"label": "Founders"<br/>}<br/>] |