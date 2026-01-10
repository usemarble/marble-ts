<!-- Start SDK Example Usage [usage] -->
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const result = await marble.posts.list({
    limit: 10,
    page: 1,
    categories: "tech,news",
    excludeCategories: "changelog",
    tags: "javascript,react",
    excludeTags: "outdated",
    query: "nextjs",
    format: "html",
    featured: "true",
  });

  for await (const page of result) {
    console.log(page);
  }
}

run();

```
<!-- End SDK Example Usage [usage] -->