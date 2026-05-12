# MediaResponse

## Example Usage

```typescript
import { MediaResponse } from "@usemarble/sdk/models";

let value: MediaResponse = {
  media: {
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
    type: "video",
    createdAt: new Date("2024-01-15T10:00:00Z"),
    updatedAt: new Date("2024-01-16T12:00:00Z"),
  },
};
```

## Fields

| Field                              | Type                               | Required                           | Description                        |
| ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- |
| `media`                            | [models.Media](../models/media.md) | :heavy_check_mark:                 | N/A                                |