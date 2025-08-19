# ConversionsCreateResponse

Successful response

## Example Usage

```typescript
import { ConversionsCreateResponse } from "payvra/models/operations";

let value: ConversionsCreateResponse = {
  id: "<id>",
  merchantId: "<id>",
  walletFromId: "<id>",
  walletToId: "<id>",
  status: "processing",
  amountFrom: "<value>",
  amountTo: null,
  callbackUrl: "https://mundane-thorn.com/",
  createdAt: "1718678521550",
  updatedAt: "1735671813128",
  currencyFrom: {
    id: "<id>",
    code: "<value>",
    name: "<value>",
    enabled: true,
    walletRegex: "<value>",
    priority: 441299,
    extraIdExists: false,
    extraIdRegex: "<value>",
    usdPrice: "<value>",
    minPaymentAmount: "<value>",
    minPayoutAmount: "<value>",
    minWithdrawalFeeEstimate: "<value>",
    logoUrl: "https://cloudy-giant.info/",
    track: true,
    cgId: "<id>",
    isMaxlimit: true,
    network: "<value>",
    smartContract: "<value>",
    networkPrecision: "<value>",
    explorerLinkHash: "<value>",
    precision: 265187,
    ticker: "<value>",
    isDefi: false,
    isPopular: true,
    isStable: true,
    availableForToConversion: true,
    createdAt: "1705100756946",
    updatedAt: "1735621284213",
  },
  currencyTo: {
    id: "<id>",
    code: "<value>",
    name: "<value>",
    enabled: true,
    walletRegex: "<value>",
    priority: 278104,
    extraIdExists: true,
    extraIdRegex: "<value>",
    usdPrice: "<value>",
    minPaymentAmount: "<value>",
    minPayoutAmount: "<value>",
    minWithdrawalFeeEstimate: "<value>",
    logoUrl: "https://impressionable-jump.net",
    track: true,
    cgId: "<id>",
    isMaxlimit: true,
    network: "<value>",
    smartContract: "<value>",
    networkPrecision: "<value>",
    explorerLinkHash: "<value>",
    precision: 251429,
    ticker: "<value>",
    isDefi: true,
    isPopular: true,
    isStable: false,
    availableForToConversion: false,
    createdAt: "1714144209604",
    updatedAt: "1735634944418",
  },
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `id`                                                                                                 | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `merchantId`                                                                                         | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `walletFromId`                                                                                       | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `walletToId`                                                                                         | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `status`                                                                                             | [operations.ConversionsCreateStatus](../../models/operations/conversionscreatestatus.md)             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `amountFrom`                                                                                         | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `amountTo`                                                                                           | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `callbackUrl`                                                                                        | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `createdAt`                                                                                          | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `updatedAt`                                                                                          | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `currencyFrom`                                                                                       | [operations.ConversionsCreateCurrencyFrom](../../models/operations/conversionscreatecurrencyfrom.md) | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `currencyTo`                                                                                         | [operations.ConversionsCreateCurrencyTo](../../models/operations/conversionscreatecurrencyto.md)     | :heavy_check_mark:                                                                                   | N/A                                                                                                  |