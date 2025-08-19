# Wallets
(*wallets*)

## Overview

### Available Operations

* [list](#list) - Query wallets
* [get](#get) - Retrieve a wallet
* [listOwned](#listowned) - Get all wallets
* [stats](#stats) - Get wallet stats

## list

Query wallets

### Example Usage

<!-- UsageSnippet language="typescript" operationID="wallets-listOwned" method="post" path="/v1/wallets/list" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.wallets.list();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PayvraCore } from "payvra/core.js";
import { walletsList } from "payvra/funcs/walletsList.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await walletsList(payvra);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("walletsList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.WalletsListOwnedRequest](../../models/operations/walletslistownedrequest.md)                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.WalletsListOwnedResponse](../../models/operations/walletslistownedresponse.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorBADREQUEST          | 400                             | application/json                |
| errors.ErrorUNAUTHORIZED        | 401                             | application/json                |
| errors.ErrorFORBIDDEN           | 403                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |

## get

Retrieve a wallet by its ID for the authenticated merchant

### Example Usage

<!-- UsageSnippet language="typescript" operationID="wallets-getById" method="get" path="/v1/wallets/{id}" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.wallets.get({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PayvraCore } from "payvra/core.js";
import { walletsGet } from "payvra/funcs/walletsGet.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await walletsGet(payvra, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("walletsGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.WalletsGetByIdRequest](../../models/operations/walletsgetbyidrequest.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.WalletsGetByIdResponse](../../models/operations/walletsgetbyidresponse.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorBADREQUEST          | 400                             | application/json                |
| errors.ErrorUNAUTHORIZED        | 401                             | application/json                |
| errors.ErrorFORBIDDEN           | 403                             | application/json                |
| errors.ErrorNOTFOUND            | 404                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |

## listOwned

Get all wallets for the authenticated merchant.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="wallets-getAllOwned" method="get" path="/v1/wallets" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.wallets.listOwned();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PayvraCore } from "payvra/core.js";
import { walletsListOwned } from "payvra/funcs/walletsListOwned.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await walletsListOwned(payvra);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("walletsListOwned failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.WalletsGetAllOwnedResponse[]](../../models/.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorBADREQUEST          | 400                             | application/json                |
| errors.ErrorUNAUTHORIZED        | 401                             | application/json                |
| errors.ErrorFORBIDDEN           | 403                             | application/json                |
| errors.ErrorNOTFOUND            | 404                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |

## stats

Get wallet stats for the authenticated merchant.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="wallets-getStats" method="get" path="/v1/wallets/stats" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.wallets.stats();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PayvraCore } from "payvra/core.js";
import { walletsStats } from "payvra/funcs/walletsStats.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await walletsStats(payvra);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("walletsStats failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.WalletsGetStatsResponse](../../models/operations/walletsgetstatsresponse.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorUNAUTHORIZED        | 401                             | application/json                |
| errors.ErrorFORBIDDEN           | 403                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |