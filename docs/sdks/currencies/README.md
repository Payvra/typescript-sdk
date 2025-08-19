# Currencies
(*currencies*)

## Overview

### Available Operations

* [all](#all) - Read all currencies

## all

Read all currencies

### Example Usage

<!-- UsageSnippet language="typescript" operationID="currencies-getAll" method="get" path="/v1/currencies" -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.currencies.all();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PayvraCore } from "payvra/core.js";
import { currenciesAll } from "payvra/funcs/currenciesAll.js";

// Use `PayvraCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const payvra = new PayvraCore({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const res = await currenciesAll(payvra);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("currenciesAll failed:", res.error);
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

**Promise\<[operations.CurrenciesGetAllResponse[]](../../models/.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.ErrorBADREQUEST          | 400                             | application/json                |
| errors.ErrorNOTFOUND            | 404                             | application/json                |
| errors.Errorinternalservererror | 500                             | application/json                |
| errors.PayvraDefaultError       | 4XX, 5XX                        | \*/\*                           |