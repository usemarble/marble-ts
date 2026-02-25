# Posts

## Overview

### Available Operations

* [list](#list) - List posts
* [postV1Posts](#postv1posts) - Create post
* [get](#get) - Get post
* [patchV1PostsIdentifier](#patchv1postsidentifier) - Update post
* [deleteV1PostsIdentifier](#deletev1postsidentifier) - Delete post

## list

Get a paginated list of published posts with optional filtering

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_/v1/posts" method="get" path="/v1/posts" -->
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const result = await marble.posts.list({
    limit: 10,
    page: 1,
    categories: [
      "tech",
      "news",
    ],
    excludeCategories: [
      "changelog",
    ],
    tags: [
      "javascript",
      "react",
    ],
    excludeTags: [
      "outdated",
    ],
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

### Standalone function

The standalone function version of this method:

```typescript
import { MarbleCore } from "@usemarble/sdk/core.js";
import { postsList } from "@usemarble/sdk/funcs/postsList.js";

// Use `MarbleCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const marble = new MarbleCore({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const res = await postsList(marble, {
    limit: 10,
    page: 1,
    categories: [
      "tech",
      "news",
    ],
    excludeCategories: [
      "changelog",
    ],
    tags: [
      "javascript",
      "react",
    ],
    excludeTags: [
      "outdated",
    ],
    query: "nextjs",
    format: "html",
    featured: "true",
  });
  if (res.ok) {
    const { value: result } = res;
    for await (const page of result) {
    console.log(page);
  }
  } else {
    console.log("postsList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetV1PostsRequest](../../models/operations/getv1postsrequest.md)                                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetV1PostsResponse](../../models/operations/getv1postsresponse.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.ErrorT             | 400                       | application/json          |
| errors.PageNotFoundError  | 400                       | application/json          |
| errors.ServerError        | 500                       | application/json          |
| errors.MarbleDefaultError | 4XX, 5XX                  | \*/\*                     |

## postV1Posts

Create a new post. Requires a private API key. Category is required. If authors are not provided, the first workspace author is used.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="post_/v1/posts" method="post" path="/v1/posts" -->
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const result = await marble.posts.postV1Posts({
    title: "Getting Started with Next.js",
    content: "<p>Hello world</p>",
    description: "A beginner's guide to Next.js",
    slug: "getting-started-with-nextjs",
    categoryId: "cryitfjp2345kl05weoybfk9",
    status: "draft",
    tags: [
      "cryitfjp4567no07ygqadhm1",
    ],
    authors: [
      "cryitfjp3456lm06xfpzcgl0",
    ],
    coverImage: "https://media.marblecms.com/cover.jpg",
    publishedAt: new Date("2024-01-15T10:00:00Z"),
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { MarbleCore } from "@usemarble/sdk/core.js";
import { postsPostV1Posts } from "@usemarble/sdk/funcs/postsPostV1Posts.js";

// Use `MarbleCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const marble = new MarbleCore({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const res = await postsPostV1Posts(marble, {
    title: "Getting Started with Next.js",
    content: "<p>Hello world</p>",
    description: "A beginner's guide to Next.js",
    slug: "getting-started-with-nextjs",
    categoryId: "cryitfjp2345kl05weoybfk9",
    status: "draft",
    tags: [
      "cryitfjp4567no07ygqadhm1",
    ],
    authors: [
      "cryitfjp3456lm06xfpzcgl0",
    ],
    coverImage: "https://media.marblecms.com/cover.jpg",
    publishedAt: new Date("2024-01-15T10:00:00Z"),
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postsPostV1Posts failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.CreatePostBody](../../models/createpostbody.md)                                                                                                                        | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CreatePostResponse](../../models/createpostresponse.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.ErrorT             | 400                       | application/json          |
| errors.ForbiddenError     | 403                       | application/json          |
| errors.ConflictError      | 409                       | application/json          |
| errors.ServerError        | 500                       | application/json          |
| errors.MarbleDefaultError | 4XX, 5XX                  | \*/\*                     |

## get

Get a single post by ID or slug, with optional status filtering

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_/v1/posts/{identifier}" method="get" path="/v1/posts/{identifier}" -->
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const result = await marble.posts.get({
    identifier: "my-post-slug",
    format: "html",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { MarbleCore } from "@usemarble/sdk/core.js";
import { postsGet } from "@usemarble/sdk/funcs/postsGet.js";

// Use `MarbleCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const marble = new MarbleCore({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const res = await postsGet(marble, {
    identifier: "my-post-slug",
    format: "html",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postsGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetV1PostsIdentifierRequest](../../models/operations/getv1postsidentifierrequest.md)                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.PostResponse](../../models/postresponse.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.NotFoundError      | 404                       | application/json          |
| errors.ServerError        | 500                       | application/json          |
| errors.MarbleDefaultError | 4XX, 5XX                  | \*/\*                     |

## patchV1PostsIdentifier

Update an existing post by ID or slug. All fields are optional — only provided fields are updated. Requires a private API key.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="patch_/v1/posts/{identifier}" method="patch" path="/v1/posts/{identifier}" -->
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const result = await marble.posts.patchV1PostsIdentifier({
    identifier: "my-post-slug",
    body: {
      title: "Updated Post Title",
      content: "<p>Updated content</p>",
      description: "Updated description",
      slug: "updated-post-slug",
      categoryId: "cryitfjp2345kl05weoybfk9",
      status: "published",
      tags: [
        "cryitfjp4567no07ygqadhm1",
      ],
      authors: [
        "cryitfjp3456lm06xfpzcgl0",
      ],
      featured: true,
      coverImage: "https://media.marblecms.com/new-cover.jpg",
      publishedAt: new Date("2024-02-01T10:00:00Z"),
    },
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { MarbleCore } from "@usemarble/sdk/core.js";
import { postsPatchV1PostsIdentifier } from "@usemarble/sdk/funcs/postsPatchV1PostsIdentifier.js";

// Use `MarbleCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const marble = new MarbleCore({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const res = await postsPatchV1PostsIdentifier(marble, {
    identifier: "my-post-slug",
    body: {
      title: "Updated Post Title",
      content: "<p>Updated content</p>",
      description: "Updated description",
      slug: "updated-post-slug",
      categoryId: "cryitfjp2345kl05weoybfk9",
      status: "published",
      tags: [
        "cryitfjp4567no07ygqadhm1",
      ],
      authors: [
        "cryitfjp3456lm06xfpzcgl0",
      ],
      featured: true,
      coverImage: "https://media.marblecms.com/new-cover.jpg",
      publishedAt: new Date("2024-02-01T10:00:00Z"),
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postsPatchV1PostsIdentifier failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PatchV1PostsIdentifierRequest](../../models/operations/patchv1postsidentifierrequest.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.UpdatePostResponse](../../models/updatepostresponse.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.ErrorT             | 400                       | application/json          |
| errors.ForbiddenError     | 403                       | application/json          |
| errors.NotFoundError      | 404                       | application/json          |
| errors.ConflictError      | 409                       | application/json          |
| errors.ServerError        | 500                       | application/json          |
| errors.MarbleDefaultError | 4XX, 5XX                  | \*/\*                     |

## deleteV1PostsIdentifier

Delete a post by ID or slug. Requires a private API key.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="delete_/v1/posts/{identifier}" method="delete" path="/v1/posts/{identifier}" -->
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const result = await marble.posts.deleteV1PostsIdentifier({
    identifier: "my-post-slug",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { MarbleCore } from "@usemarble/sdk/core.js";
import { postsDeleteV1PostsIdentifier } from "@usemarble/sdk/funcs/postsDeleteV1PostsIdentifier.js";

// Use `MarbleCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const marble = new MarbleCore({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const res = await postsDeleteV1PostsIdentifier(marble, {
    identifier: "my-post-slug",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postsDeleteV1PostsIdentifier failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.DeleteV1PostsIdentifierRequest](../../models/operations/deletev1postsidentifierrequest.md)                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.DeleteResponse](../../models/deleteresponse.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.ForbiddenError     | 403                       | application/json          |
| errors.NotFoundError      | 404                       | application/json          |
| errors.ServerError        | 500                       | application/json          |
| errors.MarbleDefaultError | 4XX, 5XX                  | \*/\*                     |