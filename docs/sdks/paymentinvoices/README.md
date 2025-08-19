# PaymentInvoices
(*paymentInvoices*)

## Overview

### Available Operations

* [list](#list) - Query payment invoices
* [get](#get) - Retrieve a payment invoice
* [stats](#stats) - Get payment invoice stats
* [create](#create) - Create a payment invoice
* [createWhiteLabel](#createwhitelabel) - Create a white label payment invoice

## list

Query payment invoices

### Example Usage

<!-- UsageSnippet language="typescript" operationID="paymentInvoices-listOwned" method="post" path="/v1/payment-invoices/list" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.paymentInvoices.list();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PayvraCore } from "payvra/core.js";
import { paymentInvoicesList } from "payvra/funcs/paymentInvoicesList.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await paymentInvoicesList(payvra);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("paymentInvoicesList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PaymentInvoicesListOwnedRequest](../../models/operations/paymentinvoiceslistownedrequest.md)                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PaymentInvoicesListOwnedResponse](../../models/operations/paymentinvoiceslistownedresponse.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorBADREQUEST          | 400                             | application/json                |
| errors.ErrorUNAUTHORIZED        | 401                             | application/json                |
| errors.ErrorFORBIDDEN           | 403                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |

## get

Retrieve a payment invoice by its ID for the authenticated merchant.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="paymentInvoices-getById" method="get" path="/v1/payment-invoices/{id}" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.paymentInvoices.get({
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
import { paymentInvoicesGet } from "payvra/funcs/paymentInvoicesGet.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await paymentInvoicesGet(payvra, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("paymentInvoicesGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PaymentInvoicesGetByIdRequest](../../models/operations/paymentinvoicesgetbyidrequest.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PaymentInvoicesGetByIdResponse](../../models/operations/paymentinvoicesgetbyidresponse.md)\>**

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

Get payment invoice stats for the authenticated merchant.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="paymentInvoices-getStats" method="get" path="/v1/payment-invoices/stats" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.paymentInvoices.stats();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PayvraCore } from "payvra/core.js";
import { paymentInvoicesStats } from "payvra/funcs/paymentInvoicesStats.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await paymentInvoicesStats(payvra);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("paymentInvoicesStats failed:", res.error);
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

**Promise\<[operations.PaymentInvoicesGetStatsResponse](../../models/operations/paymentinvoicesgetstatsresponse.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorUNAUTHORIZED        | 401                             | application/json                |
| errors.ErrorFORBIDDEN           | 403                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |

## create

Create a payment invoice

### Example Usage

<!-- UsageSnippet language="typescript" operationID="paymentInvoices-create" method="post" path="/v1/payment-invoices" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.paymentInvoices.create({
    amount: 1787.33,
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PayvraCore } from "payvra/core.js";
import { paymentInvoicesCreate } from "payvra/funcs/paymentInvoicesCreate.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await paymentInvoicesCreate(payvra, {
    amount: 1787.33,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("paymentInvoicesCreate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PaymentInvoicesCreateRequest](../../models/operations/paymentinvoicescreaterequest.md)                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PaymentInvoicesCreateResponse](../../models/operations/paymentinvoicescreateresponse.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorBADREQUEST          | 400                             | application/json                |
| errors.ErrorUNAUTHORIZED        | 401                             | application/json                |
| errors.ErrorFORBIDDEN           | 403                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |

## createWhiteLabel

Create a white label payment invoice

### Example Usage

<!-- UsageSnippet language="typescript" operationID="paymentInvoices-createWhiteLabel" method="post" path="/v1/payment-invoices/white-label" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.paymentInvoices.createWhiteLabel({
    amount: 7262.88,
    payAddress: "<value>",
    payinExtraId: "<id>",
    payCurrency: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PayvraCore } from "payvra/core.js";
import { paymentInvoicesCreateWhiteLabel } from "payvra/funcs/paymentInvoicesCreateWhiteLabel.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await paymentInvoicesCreateWhiteLabel(payvra, {
    amount: 7262.88,
    payAddress: "<value>",
    payinExtraId: "<id>",
    payCurrency: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("paymentInvoicesCreateWhiteLabel failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PaymentInvoicesCreateWhiteLabelRequest](../../models/operations/paymentinvoicescreatewhitelabelrequest.md)                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PaymentInvoicesCreateWhiteLabelResponse](../../models/operations/paymentinvoicescreatewhitelabelresponse.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorBADREQUEST          | 400                             | application/json                |
| errors.ErrorUNAUTHORIZED        | 401                             | application/json                |
| errors.ErrorFORBIDDEN           | 403                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |