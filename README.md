# payvra

Developer-friendly & type-safe Typescript SDK specifically catered to leverage *payvra* API.

<div align="left">
    <a href="https://www.speakeasy.com/?utm_source=payvra&utm_campaign=typescript"><img src="https://custom-icon-badges.demolab.com/badge/-Built%20By%20Speakeasy-212015?style=for-the-badge&logoColor=FBE331&logo=speakeasy&labelColor=545454" /></a>
    <a href="https://opensource.org/licenses/MIT">
        <img src="https://img.shields.io/badge/License-MIT-blue.svg" style="width: 100px; height: 28px;" />
    </a>
</div>


<br /><br />
<!-- Start Summary [summary] -->
## Summary

More information about the API can be found at /api/openapi
<!-- End Summary [summary] -->

<!-- Start Table of Contents [toc] -->
## Table of Contents
<!-- $toc-max-depth=2 -->
* [payvra](#payvra)
  * [SDK Installation](#sdk-installation)
  * [Requirements](#requirements)
  * [SDK Example Usage](#sdk-example-usage)
  * [Authentication](#authentication)
  * [Available Resources and Operations](#available-resources-and-operations)
  * [Standalone functions](#standalone-functions)
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

The SDK can be installed with either [npm](https://www.npmjs.com/), [pnpm](https://pnpm.io/), [bun](https://bun.sh/) or [yarn](https://classic.yarnpkg.com/en/) package managers.

### NPM

```bash
npm add payvra
```

### PNPM

```bash
pnpm add payvra
```

### Bun

```bash
bun add payvra
```

### Yarn

```bash
yarn add payvra zod

# Note that Yarn does not install peer dependencies automatically. You will need
# to install zod as shown above.
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
<!-- End SDK Example Usage [usage] -->

<!-- Start Authentication [security] -->
## Authentication

### Per-Client Security Schemes

This SDK supports the following security scheme globally:

| Name     | Type   | Scheme  | Environment Variable |
| -------- | ------ | ------- | -------------------- |
| `apiKey` | apiKey | API key | `PAYVRA_API_KEY`     |

To authenticate with the API the `apiKey` parameter must be set when initializing the SDK client instance. For example:
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
<!-- End Authentication [security] -->

<!-- Start Available Resources and Operations [operations] -->
## Available Resources and Operations

<details open>
<summary>Available methods</summary>

### [conversions](docs/sdks/conversions/README.md)

* [list](docs/sdks/conversions/README.md#list) - Query conversions
* [get](docs/sdks/conversions/README.md#get) - Retrieve a conversion
* [estimate](docs/sdks/conversions/README.md#estimate) - Get conversion estimate
* [create](docs/sdks/conversions/README.md#create) - Create a conversion
* [stats](docs/sdks/conversions/README.md#stats) - Get conversion stats

### [currencies](docs/sdks/currencies/README.md)

* [all](docs/sdks/currencies/README.md#all) - Read all currencies

### [paymentInvoices](docs/sdks/paymentinvoices/README.md)

* [list](docs/sdks/paymentinvoices/README.md#list) - Query payment invoices
* [get](docs/sdks/paymentinvoices/README.md#get) - Retrieve a payment invoice
* [stats](docs/sdks/paymentinvoices/README.md#stats) - Get payment invoice stats
* [create](docs/sdks/paymentinvoices/README.md#create) - Create a payment invoice
* [createWhiteLabel](docs/sdks/paymentinvoices/README.md#createwhitelabel) - Create a white label payment invoice

### [payouts](docs/sdks/payouts/README.md)

* [list](docs/sdks/payouts/README.md#list) - Query payouts
* [get](docs/sdks/payouts/README.md#get) - Retrieve a payout
* [minAmount](docs/sdks/payouts/README.md#minamount) - Get minimum payout amount
* [feeEstimate](docs/sdks/payouts/README.md#feeestimate) - Get payout fee estimate
* [stats](docs/sdks/payouts/README.md#stats) - Get payout stats
* [create](docs/sdks/payouts/README.md#create) - Create a payout


### [wallets](docs/sdks/wallets/README.md)

* [list](docs/sdks/wallets/README.md#list) - Query wallets
* [get](docs/sdks/wallets/README.md#get) - Retrieve a wallet
* [listOwned](docs/sdks/wallets/README.md#listowned) - Get all wallets
* [stats](docs/sdks/wallets/README.md#stats) - Get wallet stats

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

- [`conversionsCreate`](docs/sdks/conversions/README.md#create) - Create a conversion
- [`conversionsEstimate`](docs/sdks/conversions/README.md#estimate) - Get conversion estimate
- [`conversionsGet`](docs/sdks/conversions/README.md#get) - Retrieve a conversion
- [`conversionsList`](docs/sdks/conversions/README.md#list) - Query conversions
- [`conversionsStats`](docs/sdks/conversions/README.md#stats) - Get conversion stats
- [`currenciesAll`](docs/sdks/currencies/README.md#all) - Read all currencies
- [`paymentInvoicesCreate`](docs/sdks/paymentinvoices/README.md#create) - Create a payment invoice
- [`paymentInvoicesCreateWhiteLabel`](docs/sdks/paymentinvoices/README.md#createwhitelabel) - Create a white label payment invoice
- [`paymentInvoicesGet`](docs/sdks/paymentinvoices/README.md#get) - Retrieve a payment invoice
- [`paymentInvoicesList`](docs/sdks/paymentinvoices/README.md#list) - Query payment invoices
- [`paymentInvoicesStats`](docs/sdks/paymentinvoices/README.md#stats) - Get payment invoice stats
- [`payoutsCreate`](docs/sdks/payouts/README.md#create) - Create a payout
- [`payoutsFeeEstimate`](docs/sdks/payouts/README.md#feeestimate) - Get payout fee estimate
- [`payoutsGet`](docs/sdks/payouts/README.md#get) - Retrieve a payout
- [`payoutsList`](docs/sdks/payouts/README.md#list) - Query payouts
- [`payoutsMinAmount`](docs/sdks/payouts/README.md#minamount) - Get minimum payout amount
- [`payoutsStats`](docs/sdks/payouts/README.md#stats) - Get payout stats
- [`walletsGet`](docs/sdks/wallets/README.md#get) - Retrieve a wallet
- [`walletsList`](docs/sdks/wallets/README.md#list) - Query wallets
- [`walletsListOwned`](docs/sdks/wallets/README.md#listowned) - Get all wallets
- [`walletsStats`](docs/sdks/wallets/README.md#stats) - Get wallet stats

</details>
<!-- End Standalone functions [standalone-funcs] -->

<!-- Start Retries [retries] -->
## Retries

Some of the endpoints in this SDK support retries.  If you use the SDK without any configuration, it will fall back to the default retry strategy provided by the API.  However, the default retry strategy can be overridden on a per-operation basis, or across the entire SDK.

To change the default retry strategy for a single API call, simply provide a retryConfig object to the call:
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.currencies.all({
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

  console.log(result);
}

run();

```

If you'd like to override the default retry strategy for all operations that support retries, you can provide a retryConfig at SDK initialization:
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
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
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.currencies.all();

  console.log(result);
}

run();

```
<!-- End Retries [retries] -->

<!-- Start Error Handling [errors] -->
## Error Handling

[`PayvraError`](./src/models/errors/payvraerror.ts) is the base class for all HTTP error responses. It has the following properties:

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
import { Payvra } from "payvra";
import * as errors from "payvra/models/errors";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  try {
    const result = await payvra.currencies.all();

    console.log(result);
  } catch (error) {
    // The base class for HTTP error responses
    if (error instanceof errors.PayvraError) {
      console.log(error.message);
      console.log(error.statusCode);
      console.log(error.body);
      console.log(error.headers);

      // Depending on the method different errors may be thrown
      if (error instanceof errors.ErrorBADREQUEST) {
        console.log(error.data$.message); // string
        console.log(error.data$.code); // string
        console.log(error.data$.issues); // ErrorBADREQUESTIssue[]
      }
    }
  }
}

run();

```

### Error Classes
**Primary errors:**
* [`PayvraError`](./src/models/errors/payvraerror.ts): The base class for HTTP error responses.
  * [`Errorinternalservererror`](./src/models/errors/errorinternalservererror.ts): The error information. Status code `500`.
  * [`ErrorUNAUTHORIZED`](./src/models/errors/errorunauthorized.ts): The error information. Status code `401`. *
  * [`ErrorFORBIDDEN`](./src/models/errors/errorforbidden.ts): The error information. Status code `403`. *
  * [`ErrorBADREQUEST`](./src/models/errors/errorbadrequest.ts): The error information. Status code `400`. *

<details><summary>Less common errors (7)</summary>

<br />

**Network errors:**
* [`ConnectionError`](./src/models/errors/httpclienterrors.ts): HTTP client was unable to make a request to a server.
* [`RequestTimeoutError`](./src/models/errors/httpclienterrors.ts): HTTP request timed out due to an AbortSignal signal.
* [`RequestAbortedError`](./src/models/errors/httpclienterrors.ts): HTTP request was aborted by the client.
* [`InvalidRequestError`](./src/models/errors/httpclienterrors.ts): Any input used to create a request is invalid.
* [`UnexpectedClientError`](./src/models/errors/httpclienterrors.ts): Unrecognised or unexpected error.


**Inherit from [`PayvraError`](./src/models/errors/payvraerror.ts)**:
* [`ErrorNOTFOUND`](./src/models/errors/errornotfound.ts): The error information. Status code `404`. Applicable to 9 of 21 methods.*
* [`ResponseValidationError`](./src/models/errors/responsevalidationerror.ts): Type mismatch between the data returned from the server and the structure expected by the SDK. See `error.rawValue` for the raw value and `error.pretty()` for a nicely formatted multi-line string.

</details>

\* Check [the method documentation](#available-resources-and-operations) to see if the error is applicable.
<!-- End Error Handling [errors] -->

<!-- Start Server Selection [server] -->
## Server Selection

### Override Server URL Per-Client

The default server can be overridden globally by passing a URL to the `serverURL: string` optional parameter when initializing the SDK client instance. For example:
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  serverURL: "https://v2.payvra.com/api",
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.currencies.all();

  console.log(result);
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
import { Payvra } from "payvra";
import { HTTPClient } from "payvra/lib/http";

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

const sdk = new Payvra({ httpClient });
```
<!-- End Custom HTTP Client [http-client] -->

<!-- Start Debugging [debug] -->
## Debugging

You can setup your SDK to emit debug logs for SDK requests and responses.

You can pass a logger that matches `console`'s interface as an SDK option.

> [!WARNING]
> Beware that debug logging will reveal secrets, like API tokens in headers, in log messages printed to a console or files. It's recommended to use this feature only during local development and not in production.

```typescript
import { Payvra } from "payvra";

const sdk = new Payvra({ debugLogger: console });
```

You can also enable a default debug logger by setting an environment variable `PAYVRA_DEBUG` to true.
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

### SDK Created by [Speakeasy](https://www.speakeasy.com/?utm_source=payvra&utm_campaign=typescript)
