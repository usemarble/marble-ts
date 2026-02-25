# Tags

## Overview

### Available Operations

* [list](#list) - List tags
* [postV1Tags](#postv1tags) - Create tag
* [get](#get) - Get tag
* [patchV1TagsIdentifier](#patchv1tagsidentifier) - Update tag
* [deleteV1TagsIdentifier](#deletev1tagsidentifier) - Delete tag

## list

Get a paginated list of tags

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_/v1/tags" method="get" path="/v1/tags" -->
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const result = await marble.tags.list({});

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
import { tagsList } from "@usemarble/sdk/funcs/tagsList.js";

// Use `MarbleCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const marble = new MarbleCore({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const res = await tagsList(marble, {});
  if (res.ok) {
    const { value: result } = res;
    for await (const page of result) {
    console.log(page);
  }
  } else {
    console.log("tagsList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetV1TagsRequest](../../models/operations/getv1tagsrequest.md)                                                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetV1TagsResponse](../../models/operations/getv1tagsresponse.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.ErrorT             | 400                       | application/json          |
| errors.PageNotFoundError  | 400                       | application/json          |
| errors.ServerError        | 500                       | application/json          |
| errors.MarbleDefaultError | 4XX, 5XX                  | \*/\*                     |

## postV1Tags

Create a new tag. Requires a private API key.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="post_/v1/tags" method="post" path="/v1/tags" -->
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const result = await marble.tags.postV1Tags({
    name: "JavaScript",
    slug: "javascript",
    description: "JavaScript tutorials and guides",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { MarbleCore } from "@usemarble/sdk/core.js";
import { tagsPostV1Tags } from "@usemarble/sdk/funcs/tagsPostV1Tags.js";

// Use `MarbleCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const marble = new MarbleCore({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const res = await tagsPostV1Tags(marble, {
    name: "JavaScript",
    slug: "javascript",
    description: "JavaScript tutorials and guides",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("tagsPostV1Tags failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.CreateTagBody](../../models/createtagbody.md)                                                                                                                          | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CreateTagResponse](../../models/createtagresponse.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.ErrorT             | 400                       | application/json          |
| errors.ForbiddenError     | 403                       | application/json          |
| errors.ConflictError      | 409                       | application/json          |
| errors.ServerError        | 500                       | application/json          |
| errors.MarbleDefaultError | 4XX, 5XX                  | \*/\*                     |

## get

Get a single tag by ID or slug

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_/v1/tags/{identifier}" method="get" path="/v1/tags/{identifier}" -->
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const result = await marble.tags.get({
    identifier: "javascript",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { MarbleCore } from "@usemarble/sdk/core.js";
import { tagsGet } from "@usemarble/sdk/funcs/tagsGet.js";

// Use `MarbleCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const marble = new MarbleCore({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const res = await tagsGet(marble, {
    identifier: "javascript",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("tagsGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetV1TagsIdentifierRequest](../../models/operations/getv1tagsidentifierrequest.md)                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.TagResponse](../../models/tagresponse.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.NotFoundError      | 404                       | application/json          |
| errors.ServerError        | 500                       | application/json          |
| errors.MarbleDefaultError | 4XX, 5XX                  | \*/\*                     |

## patchV1TagsIdentifier

Update an existing tag by ID or slug. Requires a private API key.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="patch_/v1/tags/{identifier}" method="patch" path="/v1/tags/{identifier}" -->
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const result = await marble.tags.patchV1TagsIdentifier({
    identifier: "javascript",
    body: {
      name: "TypeScript",
      slug: "typescript",
      description: "TypeScript tutorials and guides",
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
import { tagsPatchV1TagsIdentifier } from "@usemarble/sdk/funcs/tagsPatchV1TagsIdentifier.js";

// Use `MarbleCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const marble = new MarbleCore({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const res = await tagsPatchV1TagsIdentifier(marble, {
    identifier: "javascript",
    body: {
      name: "TypeScript",
      slug: "typescript",
      description: "TypeScript tutorials and guides",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("tagsPatchV1TagsIdentifier failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PatchV1TagsIdentifierRequest](../../models/operations/patchv1tagsidentifierrequest.md)                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CreateTagResponse](../../models/createtagresponse.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.ErrorT             | 400                       | application/json          |
| errors.ForbiddenError     | 403                       | application/json          |
| errors.NotFoundError      | 404                       | application/json          |
| errors.ConflictError      | 409                       | application/json          |
| errors.ServerError        | 500                       | application/json          |
| errors.MarbleDefaultError | 4XX, 5XX                  | \*/\*                     |

## deleteV1TagsIdentifier

Delete a tag by ID or slug. Requires a private API key.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="delete_/v1/tags/{identifier}" method="delete" path="/v1/tags/{identifier}" -->
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const result = await marble.tags.deleteV1TagsIdentifier({
    identifier: "javascript",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { MarbleCore } from "@usemarble/sdk/core.js";
import { tagsDeleteV1TagsIdentifier } from "@usemarble/sdk/funcs/tagsDeleteV1TagsIdentifier.js";

// Use `MarbleCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const marble = new MarbleCore({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const res = await tagsDeleteV1TagsIdentifier(marble, {
    identifier: "javascript",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("tagsDeleteV1TagsIdentifier failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.DeleteV1TagsIdentifierRequest](../../models/operations/deletev1tagsidentifierrequest.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
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