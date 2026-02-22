# ForbiddenError

## Example Usage

```typescript
import { ForbiddenError } from "@usemarble/sdk/models/errors";

// No examples available for this model
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      | Example                                                                          |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `error`                                                                          | *string*                                                                         | :heavy_check_mark:                                                               | N/A                                                                              | Forbidden                                                                        |
| `message`                                                                        | *string*                                                                         | :heavy_check_mark:                                                               | N/A                                                                              | Write operations require a private API key (msk_...). Public keys are read-only. |