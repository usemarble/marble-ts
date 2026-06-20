# Field

## Example Usage

```typescript
import { Field } from "@usemarble/sdk/models";

let value: Field = {
  id: "cryitfjp7890yz12abcdefg",
  key: "audience",
  name: "Audience",
  description: "Who this post is for",
  type: "boolean",
  required: false,
  position: 0,
  options: [
    {
      id: "cryitfjp9012ab34cdefghij",
      value: "developers",
      label: "Developers",
      position: 0,
      createdAt: new Date("2024-01-15T10:00:00Z"),
      updatedAt: new Date("2024-01-16T12:00:00Z"),
    },
  ],
  createdAt: new Date("2024-01-15T10:00:00Z"),
  updatedAt: new Date("2024-01-16T12:00:00Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | cryitfjp7890yz12abcdefg                                                                       |
| `key`                                                                                         | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | audience                                                                                      |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | Audience                                                                                      |
| `description`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | Who this post is for                                                                          |
| `type`                                                                                        | [models.FieldType](../models/fieldtype.md)                                                    | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `required`                                                                                    | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           | false                                                                                         |
| `position`                                                                                    | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           | 0                                                                                             |
| `options`                                                                                     | [models.FieldOption](../models/fieldoption.md)[]                                              | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           | 2024-01-15T10:00:00Z                                                                          |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           | 2024-01-16T12:00:00Z                                                                          |