# Conversions
(*conversions*)

## Overview

### Available Operations

* [list](#list) - Query conversions
* [get](#get) - Retrieve a conversion
* [estimate](#estimate) - Get conversion estimate
* [create](#create) - Create a conversion
* [stats](#stats) - Get conversion stats

## list

Query conversions for the authenticated merchant.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="conversions-listOwned" method="post" path="/v1/conversions/list" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.conversions.list();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PayvraCore } from "payvra/core.js";
import { conversionsList } from "payvra/funcs/conversionsList.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await conversionsList(payvra);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("conversionsList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ConversionsListOwnedRequest](../../models/operations/conversionslistownedrequest.md)                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ConversionsListOwnedResponse](../../models/operations/conversionslistownedresponse.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorBADREQUEST          | 400                             | application/json                |
| errors.ErrorUNAUTHORIZED        | 401                             | application/json                |
| errors.ErrorFORBIDDEN           | 403                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |

## get

Retrieve a conversion by its ID for the authenticated merchant.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="conversions-getById" method="get" path="/v1/conversions/{id}" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.conversions.get({
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
import { conversionsGet } from "payvra/funcs/conversionsGet.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await conversionsGet(payvra, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("conversionsGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ConversionsGetByIdRequest](../../models/operations/conversionsgetbyidrequest.md)                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ConversionsGetByIdResponse](../../models/operations/conversionsgetbyidresponse.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorBADREQUEST          | 400                             | application/json                |
| errors.ErrorUNAUTHORIZED        | 401                             | application/json                |
| errors.ErrorFORBIDDEN           | 403                             | application/json                |
| errors.ErrorNOTFOUND            | 404                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |

## estimate

Get the fee estimate for a currency.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="conversions-getEstimate" method="get" path="/v1/conversions/estimate/{currencyFrom}/{currencyTo}/{amountFrom}" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.conversions.estimate({
    amountFrom: "<value>",
    currencyFrom: "<value>",
    currencyTo: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PayvraCore } from "payvra/core.js";
import { conversionsEstimate } from "payvra/funcs/conversionsEstimate.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await conversionsEstimate(payvra, {
    amountFrom: "<value>",
    currencyFrom: "<value>",
    currencyTo: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("conversionsEstimate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ConversionsGetEstimateRequest](../../models/operations/conversionsgetestimaterequest.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ConversionsGetEstimateResponse](../../models/operations/conversionsgetestimateresponse.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorBADREQUEST          | 400                             | application/json                |
| errors.ErrorUNAUTHORIZED        | 401                             | application/json                |
| errors.ErrorFORBIDDEN           | 403                             | application/json                |
| errors.ErrorNOTFOUND            | 404                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |

## create

Create a conversion for the authenticated merchant.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="conversions-create" method="post" path="/v1/conversions" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.conversions.create({
    amountFrom: "<value>",
    currencyFrom: "<value>",
    currencyTo: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PayvraCore } from "payvra/core.js";
import { conversionsCreate } from "payvra/funcs/conversionsCreate.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await conversionsCreate(payvra, {
    amountFrom: "<value>",
    currencyFrom: "<value>",
    currencyTo: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("conversionsCreate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ConversionsCreateRequest](../../models/operations/conversionscreaterequest.md)                                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ConversionsCreateResponse](../../models/operations/conversionscreateresponse.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorBADREQUEST          | 400                             | application/json                |
| errors.ErrorUNAUTHORIZED        | 401                             | application/json                |
| errors.ErrorFORBIDDEN           | 403                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |

## stats

Get conversion stats for the authenticated merchant.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="conversions-getStats" method="get" path="/v1/conversions/stats" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.conversions.stats();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PayvraCore } from "payvra/core.js";
import { conversionsStats } from "payvra/funcs/conversionsStats.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await conversionsStats(payvra);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("conversionsStats failed:", res.error);
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

**Promise\<[operations.ConversionsGetStatsResponse](../../models/operations/conversionsgetstatsresponse.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorUNAUTHORIZED        | 401                             | application/json                |
| errors.ErrorFORBIDDEN           | 403                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |