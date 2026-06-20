# CreateFieldBody

## Example Usage

```typescript
import { CreateFieldBody } from "@usemarble/sdk/models";

let value: CreateFieldBody = {
  key: "audience",
  name: "Audience",
  description: "Who this post is for",
  type: "boolean",
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
| `key`                                                                                              | *string*                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                | audience                                                                                           |
| `name`                                                                                             | *string*                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                | Audience                                                                                           |
| `description`                                                                                      | *string*                                                                                           | :heavy_minus_sign:                                                                                 | N/A                                                                                                | Who this post is for                                                                               |
| `type`                                                                                             | [models.FieldType](../models/fieldtype.md)                                                         | :heavy_check_mark:                                                                                 | N/A                                                                                                |                                                                                                    |
| `required`                                                                                         | *boolean*                                                                                          | :heavy_minus_sign:                                                                                 | N/A                                                                                                | false                                                                                              |
| `options`                                                                                          | [models.FieldOptionInput](../models/fieldoptioninput.md)[]                                         | :heavy_minus_sign:                                                                                 | Required for select and multiselect fields. Not allowed for other field types.                     | [<br/>{<br/>"value": "developers",<br/>"label": "Developers"<br/>},<br/>{<br/>"value": "founders",<br/>"label": "Founders"<br/>}<br/>] |