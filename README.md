# @usemarble/sdk

Developer-friendly & type-safe Typescript SDK specifically catered to leverage *@usemarble/sdk* API.

[![Built by Speakeasy](https://img.shields.io/badge/Built_by-SPEAKEASY-374151?style=for-the-badge&labelColor=f3f4f6)](https://www.speakeasy.com/?utm_source=@usemarble/sdk&utm_campaign=typescript)
[![License: MIT](https://img.shields.io/badge/LICENSE_//_MIT-3b5bdb?style=for-the-badge&labelColor=eff6ff)](https://opensource.org/licenses/MIT)


<br /><br />
> [!IMPORTANT]
> This SDK is not yet ready for production use. To complete setup please follow the steps outlined in your [workspace](https://app.speakeasy.com/org/marblecms/marble-s8w). Delete this section before > publishing to a package manager.

<!-- Start Summary [summary] -->
## Summary

Marble API: Headless CMS API for content delivery. Use your API key in the Authorization header as a Bearer token.
<!-- End Summary [summary] -->

<!-- Start Table of Contents [toc] -->
## Table of Contents
<!-- $toc-max-depth=2 -->
* [@usemarble/sdk](#usemarblesdk)
  * [SDK Installation](#sdk-installation)
  * [Requirements](#requirements)
  * [SDK Example Usage](#sdk-example-usage)
  * [Authentication](#authentication)
  * [Available Resources and Operations](#available-resources-and-operations)
  * [Standalone functions](#standalone-functions)
  * [Pagination](#pagination)
  * [Retries](#retries)
  * [Error Handling](#error-handling)
  * [Server Selection](#server-selection)
  * [Custom HTTP Client](#custom-http-client)
  * [Debugging](#debugging)
* [Development](#development)
  * [Maturity](#maturity)
  * [Contributions](#contributions)

<!-- End Table of Contents [toc] -->

<!-- Start SDK Installation [installation] -->
## SDK Installation

> [!TIP]
> To finish publishing your SDK to npm and others you must [run your first generation action](https://www.speakeasy.com/docs/github-setup#step-by-step-guide).


The SDK can be installed with either [npm](https://www.npmjs.com/), [pnpm](https://pnpm.io/), [bun](https://bun.sh/) or [yarn](https://classic.yarnpkg.com/en/) package managers.

### NPM

```bash
npm add <UNSET>
```

### PNPM

```bash
pnpm add <UNSET>
```

### Bun

```bash
bun add <UNSET>
```

### Yarn

```bash
yarn add <UNSET>
```

> [!NOTE]
> This package is published with CommonJS and ES Modules (ESM) support.
<!-- End SDK Installation [installation] -->

<!-- Start Requirements [requirements] -->
## Requirements

For supported JavaScript runtimes, please consult [RUNTIMES.md](RUNTIMES.md).
<!-- End Requirements [requirements] -->

<!-- Start SDK Example Usage [usage] -->
## SDK Example Usage

### Example

```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  bearerAuth: process.env["MARBLE_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await marble.posts.list({
    limit: 10,
    page: 1,
    categories: "tech,news",
    excludeCategories: "drafts",
    tags: "javascript,react",
    excludeTags: "outdated",
    query: "nextjs",
    format: "html",
  });

  for await (const page of result) {
    console.log(page);
  }
}

run();

```
<!-- End SDK Example Usage [usage] -->

<!-- Start Authentication [security] -->
## Authentication

### Per-Client Security Schemes

This SDK supports the following security scheme globally:

| Name         | Type | Scheme      | Environment Variable |
| ------------ | ---- | ----------- | -------------------- |
| `bearerAuth` | http | HTTP Bearer | `MARBLE_BEARER_AUTH` |

To authenticate with the API the `bearerAuth` parameter must be set when initializing the SDK client instance. For example:
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  bearerAuth: process.env["MARBLE_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await marble.posts.list({
    limit: 10,
    page: 1,
    categories: "tech,news",
    excludeCategories: "drafts",
    tags: "javascript,react",
    excludeTags: "outdated",
    query: "nextjs",
    format: "html",
  });

  for await (const page of result) {
    console.log(page);
  }
}

run();

```
<!-- End Authentication [security] -->

<!-- Start Available Resources and Operations [operations] -->
## Available Resources and Operations

<details open>
<summary>Available methods</summary>

### [Authors](docs/sdks/authors/README.md)

* [list](docs/sdks/authors/README.md#list) - List authors
* [get](docs/sdks/authors/README.md#get) - Get an author

### [Categories](docs/sdks/categories/README.md)

* [list](docs/sdks/categories/README.md#list) - List categories
* [get](docs/sdks/categories/README.md#get) - Get a category

### [Posts](docs/sdks/posts/README.md)

* [list](docs/sdks/posts/README.md#list) - List posts
* [get](docs/sdks/posts/README.md#get) - Get a post

### [Tags](docs/sdks/tags/README.md)

* [list](docs/sdks/tags/README.md#list) - List tags
* [get](docs/sdks/tags/README.md#get) - Get a tag

</details>
<!-- End Available Resources and Operations [operations] -->

<!-- Start Standalone functions [standalone-funcs] -->
## Standalone functions

All the methods listed above are available as standalone functions. These
functions are ideal for use in applications running in the browser, serverless
runtimes or other environments where application bundle size is a primary
concern. When using a bundler to build your application, all unused
functionality will be either excluded from the final bundle or tree-shaken away.

To read more about standalone functions, check [FUNCTIONS.md](./FUNCTIONS.md).

<details>

<summary>Available standalone functions</summary>

- [`authorsGet`](docs/sdks/authors/README.md#get) - Get an author
- [`authorsList`](docs/sdks/authors/README.md#list) - List authors
- [`categoriesGet`](docs/sdks/categories/README.md#get) - Get a category
- [`categoriesList`](docs/sdks/categories/README.md#list) - List categories
- [`postsGet`](docs/sdks/posts/README.md#get) - Get a post
- [`postsList`](docs/sdks/posts/README.md#list) - List posts
- [`tagsGet`](docs/sdks/tags/README.md#get) - Get a tag
- [`tagsList`](docs/sdks/tags/README.md#list) - List tags

</details>
<!-- End Standalone functions [standalone-funcs] -->

<!-- Start Pagination [pagination] -->
## Pagination

Some of the endpoints in this SDK support pagination. To use pagination, you
make your SDK calls as usual, but the returned response object will also be an
async iterable that can be consumed using the [`for await...of`][for-await-of]
syntax.

[for-await-of]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for-await...of

Here's an example of one such pagination call:

```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  bearerAuth: process.env["MARBLE_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await marble.posts.list({
    limit: 10,
    page: 1,
    categories: "tech,news",
    excludeCategories: "drafts",
    tags: "javascript,react",
    excludeTags: "outdated",
    query: "nextjs",
    format: "html",
  });

  for await (const page of result) {
    console.log(page);
  }
}

run();

```
<!-- End Pagination [pagination] -->

<!-- Start Retries [retries] -->
## Retries

Some of the endpoints in this SDK support retries.  If you use the SDK without any configuration, it will fall back to the default retry strategy provided by the API.  However, the default retry strategy can be overridden on a per-operation basis, or across the entire SDK.

To change the default retry strategy for a single API call, simply provide a retryConfig object to the call:
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  bearerAuth: process.env["MARBLE_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await marble.posts.list({
    limit: 10,
    page: 1,
    categories: "tech,news",
    excludeCategories: "drafts",
    tags: "javascript,react",
    excludeTags: "outdated",
    query: "nextjs",
    format: "html",
  }, {
    retries: {
      strategy: "backoff",
      backoff: {
        initialInterval: 1,
        maxInterval: 50,
        exponent: 1.1,
        maxElapsedTime: 100,
      },
      retryConnectionErrors: false,
    },
  });

  for await (const page of result) {
    console.log(page);
  }
}

run();

```

If you'd like to override the default retry strategy for all operations that support retries, you can provide a retryConfig at SDK initialization:
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  retryConfig: {
    strategy: "backoff",
    backoff: {
      initialInterval: 1,
      maxInterval: 50,
      exponent: 1.1,
      maxElapsedTime: 100,
    },
    retryConnectionErrors: false,
  },
  bearerAuth: process.env["MARBLE_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await marble.posts.list({
    limit: 10,
    page: 1,
    categories: "tech,news",
    excludeCategories: "drafts",
    tags: "javascript,react",
    excludeTags: "outdated",
    query: "nextjs",
    format: "html",
  });

  for await (const page of result) {
    console.log(page);
  }
}

run();

```
<!-- End Retries [retries] -->

<!-- Start Error Handling [errors] -->
## Error Handling

[`MarbleError`](./src/models/errors/marbleerror.ts) is the base class for all HTTP error responses. It has the following properties:

| Property            | Type       | Description                                                                             |
| ------------------- | ---------- | --------------------------------------------------------------------------------------- |
| `error.message`     | `string`   | Error message                                                                           |
| `error.statusCode`  | `number`   | HTTP response status code eg `404`                                                      |
| `error.headers`     | `Headers`  | HTTP response headers                                                                   |
| `error.body`        | `string`   | HTTP body. Can be empty string if no body is returned.                                  |
| `error.rawResponse` | `Response` | Raw HTTP response                                                                       |
| `error.data$`       |            | Optional. Some errors may contain structured data. [See Error Classes](#error-classes). |

### Example
```typescript
import { Marble } from "@usemarble/sdk";
import * as errors from "@usemarble/sdk/models/errors";

const marble = new Marble({
  bearerAuth: process.env["MARBLE_BEARER_AUTH"] ?? "",
});

async function run() {
  try {
    const result = await marble.posts.list({
      limit: 10,
      page: 1,
      categories: "tech,news",
      excludeCategories: "drafts",
      tags: "javascript,react",
      excludeTags: "outdated",
      query: "nextjs",
      format: "html",
    });

    for await (const page of result) {
      console.log(page);
    }
  } catch (error) {
    // The base class for HTTP error responses
    if (error instanceof errors.MarbleError) {
      console.log(error.message);
      console.log(error.statusCode);
      console.log(error.body);
      console.log(error.headers);

      // Depending on the method different errors may be thrown
      if (error instanceof errors.ErrorT) {
        console.log(error.data$.error); // string
        console.log(error.data$.details); // Detail[]
        console.log(error.data$.message); // string
      }
    }
  }
}

run();

```

### Error Classes
**Primary errors:**
* [`MarbleError`](./src/models/errors/marbleerror.ts): The base class for HTTP error responses.
  * [`ServerError`](./src/models/errors/servererror.ts): Server error. Status code `500`.

<details><summary>Less common errors (9)</summary>

<br />

**Network errors:**
* [`ConnectionError`](./src/models/errors/httpclienterrors.ts): HTTP client was unable to make a request to a server.
* [`RequestTimeoutError`](./src/models/errors/httpclienterrors.ts): HTTP request timed out due to an AbortSignal signal.
* [`RequestAbortedError`](./src/models/errors/httpclienterrors.ts): HTTP request was aborted by the client.
* [`InvalidRequestError`](./src/models/errors/httpclienterrors.ts): Any input used to create a request is invalid.
* [`UnexpectedClientError`](./src/models/errors/httpclienterrors.ts): Unrecognised or unexpected error.


**Inherit from [`MarbleError`](./src/models/errors/marbleerror.ts)**:
* [`ErrorT`](./src/models/errors/errort.ts): Invalid query parameters or page number. Status code `400`. Applicable to 4 of 8 methods.*
* [`PageNotFoundError`](./src/models/errors/pagenotfounderror.ts): Invalid query parameters or page number. Status code `400`. Applicable to 4 of 8 methods.*
* [`NotFoundError`](./src/models/errors/notfounderror.ts): Status code `404`. Applicable to 4 of 8 methods.*
* [`ResponseValidationError`](./src/models/errors/responsevalidationerror.ts): Type mismatch between the data returned from the server and the structure expected by the SDK. See `error.rawValue` for the raw value and `error.pretty()` for a nicely formatted multi-line string.

</details>

\* Check [the method documentation](#available-resources-and-operations) to see if the error is applicable.
<!-- End Error Handling [errors] -->

<!-- Start Server Selection [server] -->
## Server Selection

### Override Server URL Per-Client

The default server can be overridden globally by passing a URL to the `serverURL: string` optional parameter when initializing the SDK client instance. For example:
```typescript
import { Marble } from "@usemarble/sdk";

const marble = new Marble({
  serverURL: "https://api.marblecms.com",
  bearerAuth: process.env["MARBLE_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await marble.posts.list({
    limit: 10,
    page: 1,
    categories: "tech,news",
    excludeCategories: "drafts",
    tags: "javascript,react",
    excludeTags: "outdated",
    query: "nextjs",
    format: "html",
  });

  for await (const page of result) {
    console.log(page);
  }
}

run();

```
<!-- End Server Selection [server] -->

<!-- Start Custom HTTP Client [http-client] -->
## Custom HTTP Client

The TypeScript SDK makes API calls using an `HTTPClient` that wraps the native
[Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API). This
client is a thin wrapper around `fetch` and provides the ability to attach hooks
around the request lifecycle that can be used to modify the request or handle
errors and response.

The `HTTPClient` constructor takes an optional `fetcher` argument that can be
used to integrate a third-party HTTP client or when writing tests to mock out
the HTTP client and feed in fixtures.

The following example shows how to use the `"beforeRequest"` hook to to add a
custom header and a timeout to requests and how to use the `"requestError"` hook
to log errors:

```typescript
import { Marble } from "@usemarble/sdk";
import { HTTPClient } from "@usemarble/sdk/lib/http";

const httpClient = new HTTPClient({
  // fetcher takes a function that has the same signature as native `fetch`.
  fetcher: (request) => {
    return fetch(request);
  }
});

httpClient.addHook("beforeRequest", (request) => {
  const nextRequest = new Request(request, {
    signal: request.signal || AbortSignal.timeout(5000)
  });

  nextRequest.headers.set("x-custom-header", "custom value");

  return nextRequest;
});

httpClient.addHook("requestError", (error, request) => {
  console.group("Request Error");
  console.log("Reason:", `${error}`);
  console.log("Endpoint:", `${request.method} ${request.url}`);
  console.groupEnd();
});

const sdk = new Marble({ httpClient: httpClient });
```
<!-- End Custom HTTP Client [http-client] -->

<!-- Start Debugging [debug] -->
## Debugging

You can setup your SDK to emit debug logs for SDK requests and responses.

You can pass a logger that matches `console`'s interface as an SDK option.

> [!WARNING]
> Beware that debug logging will reveal secrets, like API tokens in headers, in log messages printed to a console or files. It's recommended to use this feature only during local development and not in production.

```typescript
import { Marble } from "@usemarble/sdk";

const sdk = new Marble({ debugLogger: console });
```

You can also enable a default debug logger by setting an environment variable `MARBLE_DEBUG` to true.
<!-- End Debugging [debug] -->

<!-- Placeholder for Future Speakeasy SDK Sections -->

# Development

## Maturity

This SDK is in beta, and there may be breaking changes between versions without a major version update. Therefore, we recommend pinning usage
to a specific package version. This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

## Contributions

While we value open-source contributions to this SDK, this library is generated programmatically. Any manual changes added to internal files will be overwritten on the next generation. 
We look forward to hearing your feedback. Feel free to open a PR or an issue with a proof of concept and we'll do our best to include it in a future release. 

### SDK Created by [Speakeasy](https://www.speakeasy.com/?utm_source=@usemarble/sdk&utm_campaign=typescript)
