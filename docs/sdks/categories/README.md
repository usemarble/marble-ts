# Categories

## Overview

### Available Operations

* [list](#list) - List categories
* [create](#create) - Create category
* [get](#get) - Get category
* [update](#update) - Update category
* [delete](#delete) - Delete category

## list

Get a paginated list of categories

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_/v1/categories" method="get" path="/v1/categories" -->
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const result = await marble.categories.list({});

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
import { categoriesList } from "@usemarble/sdk/funcs/categoriesList.js";

// Use `MarbleCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const marble = new MarbleCore({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const res = await categoriesList(marble, {});
  if (res.ok) {
    const { value: result } = res;
    for await (const page of result) {
    console.log(page);
  }
  } else {
    console.log("categoriesList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetV1CategoriesRequest](../../models/operations/getv1categoriesrequest.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetV1CategoriesResponse](../../models/operations/getv1categoriesresponse.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.ErrorT             | 400                       | application/json          |
| errors.PageNotFoundError  | 400                       | application/json          |
| errors.ServerError        | 500                       | application/json          |
| errors.MarbleDefaultError | 4XX, 5XX                  | \*/\*                     |

## create

Create a new category. Requires a private API key.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="post_/v1/categories" method="post" path="/v1/categories" -->
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const result = await marble.categories.create({
    name: "Technology",
    slug: "technology",
    description: "Tech news and tutorials",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { MarbleCore } from "@usemarble/sdk/core.js";
import { categoriesCreate } from "@usemarble/sdk/funcs/categoriesCreate.js";

// Use `MarbleCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const marble = new MarbleCore({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const res = await categoriesCreate(marble, {
    name: "Technology",
    slug: "technology",
    description: "Tech news and tutorials",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("categoriesCreate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.CreateCategoryBody](../../models/createcategorybody.md)                                                                                                                | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CreateCategoryResponse](../../models/createcategoryresponse.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.ErrorT             | 400                       | application/json          |
| errors.ForbiddenError     | 403                       | application/json          |
| errors.ConflictError      | 409                       | application/json          |
| errors.ServerError        | 500                       | application/json          |
| errors.MarbleDefaultError | 4XX, 5XX                  | \*/\*                     |

## get

Get a single category by ID or slug

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_/v1/categories/{identifier}" method="get" path="/v1/categories/{identifier}" -->
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const result = await marble.categories.get({
    identifier: "technology",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { MarbleCore } from "@usemarble/sdk/core.js";
import { categoriesGet } from "@usemarble/sdk/funcs/categoriesGet.js";

// Use `MarbleCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const marble = new MarbleCore({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const res = await categoriesGet(marble, {
    identifier: "technology",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("categoriesGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetV1CategoriesIdentifierRequest](../../models/operations/getv1categoriesidentifierrequest.md)                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CategoryResponse](../../models/categoryresponse.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.NotFoundError      | 404                       | application/json          |
| errors.ServerError        | 500                       | application/json          |
| errors.MarbleDefaultError | 4XX, 5XX                  | \*/\*                     |

## update

Update an existing category by ID or slug. Requires a private API key.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="patch_/v1/categories/{identifier}" method="patch" path="/v1/categories/{identifier}" -->
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const result = await marble.categories.update({
    identifier: "technology",
    body: {
      name: "Engineering",
      slug: "engineering",
      description: "Engineering articles and tutorials",
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
import { categoriesUpdate } from "@usemarble/sdk/funcs/categoriesUpdate.js";

// Use `MarbleCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const marble = new MarbleCore({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const res = await categoriesUpdate(marble, {
    identifier: "technology",
    body: {
      name: "Engineering",
      slug: "engineering",
      description: "Engineering articles and tutorials",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("categoriesUpdate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PatchV1CategoriesIdentifierRequest](../../models/operations/patchv1categoriesidentifierrequest.md)                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CreateCategoryResponse](../../models/createcategoryresponse.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.ErrorT             | 400                       | application/json          |
| errors.ForbiddenError     | 403                       | application/json          |
| errors.NotFoundError      | 404                       | application/json          |
| errors.ConflictError      | 409                       | application/json          |
| errors.ServerError        | 500                       | application/json          |
| errors.MarbleDefaultError | 4XX, 5XX                  | \*/\*                     |

## delete

Delete a category by ID or slug. Requires a private API key. Cannot delete a category that has posts assigned to it.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="delete_/v1/categories/{identifier}" method="delete" path="/v1/categories/{identifier}" -->
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const result = await marble.categories.delete({
    identifier: "technology",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { MarbleCore } from "@usemarble/sdk/core.js";
import { categoriesDelete } from "@usemarble/sdk/funcs/categoriesDelete.js";

// Use `MarbleCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const marble = new MarbleCore({
  apiKey: process.env["MARBLE_API_KEY"] ?? "",
});

async function run() {
  const res = await categoriesDelete(marble, {
    identifier: "technology",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("categoriesDelete failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.DeleteV1CategoriesIdentifierRequest](../../models/operations/deletev1categoriesidentifierrequest.md)                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.DeleteResponse](../../models/deleteresponse.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.ErrorT             | 400                       | application/json          |
| errors.ForbiddenError     | 403                       | application/json          |
| errors.NotFoundError      | 404                       | application/json          |
| errors.ServerError        | 500                       | application/json          |
| errors.MarbleDefaultError | 4XX, 5XX                  | \*/\*                     |