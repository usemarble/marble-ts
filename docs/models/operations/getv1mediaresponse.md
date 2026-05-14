# GetV1MediaResponse

## Example Usage

```typescript
import { GetV1MediaResponse } from "@usemarble/sdk/models/operations";

let value: GetV1MediaResponse = {
  result: {
    media: [
      {
        id: "cryitfjp1234jl04vdnycek8",
        name: "Hero image",
        url: "https://cdn.marblecms.com/media/hero.jpg",
        alt: "A dashboard screenshot",
        size: 382019,
        mimeType: "image/jpeg",
        width: 1600,
        height: 900,
        duration: 12000,
        blurHash: "LEHV6nWB2yk8pyo0adR*.7kCMdnj",
        type: "audio",
        createdAt: new Date("2024-01-15T10:00:00Z"),
        updatedAt: new Date("2024-01-16T12:00:00Z"),
      },
    ],
    pagination: {
      limit: 10,
      currentPage: 1,
      nextPage: 2,
      previousPage: null,
      totalPages: 5,
      totalItems: 42,
    },
  },
};
```

## Fields

| Field                                                         | Type                                                          | Required                                                      | Description                                                   |
| ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| `result`                                                      | [models.MediaListResponse](../../models/medialistresponse.md) | :heavy_check_mark:                                            | N/A                                                           |