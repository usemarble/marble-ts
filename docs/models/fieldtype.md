# FieldType

## Example Usage

```typescript
import { FieldType } from "@usemarble/sdk/models";

let value: FieldType = "select";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"text" | "number" | "boolean" | "date" | "richtext" | "select" | "multiselect" | Unrecognized<string>
```