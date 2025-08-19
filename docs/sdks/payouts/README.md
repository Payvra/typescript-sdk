# Payouts
(*payouts*)

## Overview

### Available Operations

* [list](#list) - Query payouts
* [get](#get) - Retrieve a payout
* [minAmount](#minamount) - Get minimum payout amount
* [feeEstimate](#feeestimate) - Get payout fee estimate
* [stats](#stats) - Get payout stats
* [create](#create) - Create a payout

## list

Query payouts for the authenticated merchant.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="payouts-listOwned" method="post" path="/v1/payouts/list" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.payouts.list();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PayvraCore } from "payvra/core.js";
import { payoutsList } from "payvra/funcs/payoutsList.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await payoutsList(payvra);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("payoutsList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PayoutsListOwnedRequest](../../models/operations/payoutslistownedrequest.md)                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PayoutsListOwnedResponse](../../models/operations/payoutslistownedresponse.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorBADREQUEST          | 400                             | application/json                |
| errors.ErrorUNAUTHORIZED        | 401                             | application/json                |
| errors.ErrorFORBIDDEN           | 403                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |

## get

Retrieve a payout by its ID for the authenticated merchant.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="payouts-getById" method="get" path="/v1/payouts/{id}" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.payouts.get({
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
import { payoutsGet } from "payvra/funcs/payoutsGet.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await payoutsGet(payvra, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("payoutsGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PayoutsGetByIdRequest](../../models/operations/payoutsgetbyidrequest.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PayoutsGetByIdResponse](../../models/operations/payoutsgetbyidresponse.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorBADREQUEST          | 400                             | application/json                |
| errors.ErrorUNAUTHORIZED        | 401                             | application/json                |
| errors.ErrorFORBIDDEN           | 403                             | application/json                |
| errors.ErrorNOTFOUND            | 404                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |

## minAmount

Get the minimum amount for a currency.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="payouts-getMinAmount" method="get" path="/v1/payouts/min-amount/{currency}" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.payouts.minAmount({
    currency: "Manat",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PayvraCore } from "payvra/core.js";
import { payoutsMinAmount } from "payvra/funcs/payoutsMinAmount.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await payoutsMinAmount(payvra, {
    currency: "Manat",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("payoutsMinAmount failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PayoutsGetMinAmountRequest](../../models/operations/payoutsgetminamountrequest.md)                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PayoutsGetMinAmountResponse](../../models/operations/payoutsgetminamountresponse.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorBADREQUEST          | 400                             | application/json                |
| errors.ErrorUNAUTHORIZED        | 401                             | application/json                |
| errors.ErrorFORBIDDEN           | 403                             | application/json                |
| errors.ErrorNOTFOUND            | 404                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |

## feeEstimate

Get the fee estimate for a currency.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="payouts-getFeeEstimate" method="get" path="/v1/payouts/fee-estimate/{currency}/{amount}" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.payouts.feeEstimate({
    currency: "Lek",
    amount: "680.46",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PayvraCore } from "payvra/core.js";
import { payoutsFeeEstimate } from "payvra/funcs/payoutsFeeEstimate.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await payoutsFeeEstimate(payvra, {
    currency: "Lek",
    amount: "680.46",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("payoutsFeeEstimate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PayoutsGetFeeEstimateRequest](../../models/operations/payoutsgetfeeestimaterequest.md)                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PayoutsGetFeeEstimateResponse](../../models/operations/payoutsgetfeeestimateresponse.md)\>**

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

Get payout stats the authenticated merchant.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="payouts-getStats" method="get" path="/v1/payouts/stats" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.payouts.stats();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PayvraCore } from "payvra/core.js";
import { payoutsStats } from "payvra/funcs/payoutsStats.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await payoutsStats(payvra);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("payoutsStats failed:", res.error);
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

**Promise\<[operations.PayoutsGetStatsResponse](../../models/operations/payoutsgetstatsresponse.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorUNAUTHORIZED        | 401                             | application/json                |
| errors.ErrorFORBIDDEN           | 403                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |

## create

Create a payout for the authenticated merchant.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="payouts-create" method="post" path="/v1/payouts" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.payouts.create({
    amount: "312.46",
    address: "691 S Walnut Street",
    currency: "Rial Omani",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PayvraCore } from "payvra/core.js";
import { payoutsCreate } from "payvra/funcs/payoutsCreate.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await payoutsCreate(payvra, {
    amount: "312.46",
    address: "691 S Walnut Street",
    currency: "Rial Omani",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("payoutsCreate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PayoutsCreateRequest](../../models/operations/payoutscreaterequest.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PayoutsCreateResponse](../../models/operations/payoutscreateresponse.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorBADREQUEST          | 400                             | application/json                |
| errors.ErrorUNAUTHORIZED        | 401                             | application/json                |
| errors.ErrorFORBIDDEN           | 403                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |