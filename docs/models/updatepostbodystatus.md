# UpdatePostBodyStatus

Use 'scheduled' with a future publishedAt, sent or already stored, to go live at that time. Publishing a scheduled post early sets publishedAt to now unless you send one.

## Example Usage

```typescript
import { UpdatePostBodyStatus } from "@usemarble/sdk/models";

let value: UpdatePostBodyStatus = "published";
```

## Values

```typescript
"published" | "draft" | "scheduled"
```