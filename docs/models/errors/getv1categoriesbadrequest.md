# GetV1CategoriesBadRequest

Invalid query parameters or page number


## Supported Types

### `errors.ErrorT`

```typescript
const value: errors.ErrorT = {
  error: "Invalid query parameters",
  details: [
    {
      field: "limit",
      message: "Expected number, received string",
    },
  ],
  message: "Validation failed",
};
```

### `errors.PageNotFoundError`

```typescript
const value: errors.PageNotFoundError = {
  error: "Invalid page number",
  details: {
    message: "Page 10 does not exist.",
    totalPages: 5,
    requestedPage: 10,
  },
};
```

