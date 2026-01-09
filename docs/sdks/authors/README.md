# Authors

## Overview

### Available Operations

* [list](#list) - List authors
* [get](#get) - Get an author

## list

Get a paginated list of authors who have published posts

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_/v1/authors" method="get" path="/v1/authors" -->
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  bearerAuth: process.env["MARBLE_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await marble.authors.list({});

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
import { authorsList } from "@usemarble/sdk/funcs/authorsList.js";

// Use `MarbleCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const marble = new MarbleCore({
  bearerAuth: process.env["MARBLE_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await authorsList(marble, {});
  if (res.ok) {
    const { value: result } = res;
    for await (const page of result) {
    console.log(page);
  }
  } else {
    console.log("authorsList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetV1AuthorsRequest](../../models/operations/getv1authorsrequest.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetV1AuthorsResponse](../../models/operations/getv1authorsresponse.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.ErrorT             | 400                       | application/json          |
| errors.PageNotFoundError  | 400                       | application/json          |
| errors.ServerError        | 500                       | application/json          |
| errors.MarbleDefaultError | 4XX, 5XX                  | \*/\*                     |

## get

Get a single author by ID or slug

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_/v1/authors/{identifier}" method="get" path="/v1/authors/{identifier}" -->
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  bearerAuth: process.env["MARBLE_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await marble.authors.get({
    identifier: "john-doe",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { MarbleCore } from "@usemarble/sdk/core.js";
import { authorsGet } from "@usemarble/sdk/funcs/authorsGet.js";

// Use `MarbleCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const marble = new MarbleCore({
  bearerAuth: process.env["MARBLE_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await authorsGet(marble, {
    identifier: "john-doe",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("authorsGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetV1AuthorsIdentifierRequest](../../models/operations/getv1authorsidentifierrequest.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.SingleAuthorResponse](../../models/singleauthorresponse.md)\>**

### Errors

| Error Type                | Status Code               | Content Type              |
| ------------------------- | ------------------------- | ------------------------- |
| errors.NotFoundError      | 404                       | application/json          |
| errors.ServerError        | 500                       | application/json          |
| errors.MarbleDefaultError | 4XX, 5XX                  | \*/\*                     |