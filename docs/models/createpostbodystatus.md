# CreatePostBodyStatus

Use 'scheduled' with a future publishedAt to go live at that time. A 'published' post is live immediately, even with a future publishedAt.

## Example Usage

```typescript
import { CreatePostBodyStatus } from "@usemarble/sdk/models";

let value: CreatePostBodyStatus = "draft";
```

## Values

```typescript
"published" | "draft" | "scheduled"
```