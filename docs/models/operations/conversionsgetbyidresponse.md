# ConversionsGetByIdResponse

Successful response

## Example Usage

```typescript
import { ConversionsGetByIdResponse } from "payvra/models/operations";

let value: ConversionsGetByIdResponse = {
  id: "<id>",
  merchantId: "<id>",
  walletFromId: "<id>",
  walletToId: "<id>",
  status: "waiting",
  amountFrom: "<value>",
  amountTo: "<value>",
  callbackUrl: "https://nippy-recommendation.com/",
  createdAt: "1731072018788",
  updatedAt: "1735631766022",
  currencyFrom: {
    id: "<id>",
    code: "<value>",
    name: "<value>",
    enabled: false,
    walletRegex: "<value>",
    priority: 869832,
    extraIdExists: true,
    extraIdRegex: "<value>",
    usdPrice: "<value>",
    minPaymentAmount: "<value>",
    minPayoutAmount: "<value>",
    minWithdrawalFeeEstimate: "<value>",
    logoUrl: "https://lined-doing.com",
    track: true,
    cgId: "<id>",
    isMaxlimit: true,
    network: "<value>",
    smartContract: "<value>",
    networkPrecision: "<value>",
    explorerLinkHash: "<value>",
    precision: 85044,
    ticker: "<value>",
    isDefi: true,
    isPopular: true,
    isStable: false,
    availableForToConversion: true,
    createdAt: "1715354688328",
    updatedAt: "1735679748823",
  },
  currencyTo: {
    id: "<id>",
    code: "<value>",
    name: "<value>",
    enabled: false,
    walletRegex: "<value>",
    priority: 683574,
    extraIdExists: false,
    extraIdRegex: "<value>",
    usdPrice: "<value>",
    minPaymentAmount: "<value>",
    minPayoutAmount: "<value>",
    minWithdrawalFeeEstimate: "<value>",
    logoUrl: "https://qualified-grandson.name/",
    track: true,
    cgId: "<id>",
    isMaxlimit: true,
    network: "<value>",
    smartContract: null,
    networkPrecision: "<value>",
    explorerLinkHash: "<value>",
    precision: 453469,
    ticker: "<value>",
    isDefi: true,
    isPopular: false,
    isStable: false,
    availableForToConversion: true,
    createdAt: "1713485212365",
    updatedAt: "1735652916963",
  },
};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                   | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `merchantId`                                                                                           | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `walletFromId`                                                                                         | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `walletToId`                                                                                           | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `status`                                                                                               | [operations.ConversionsGetByIdStatus](../../models/operations/conversionsgetbyidstatus.md)             | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `amountFrom`                                                                                           | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `amountTo`                                                                                             | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `callbackUrl`                                                                                          | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `createdAt`                                                                                            | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `updatedAt`                                                                                            | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `currencyFrom`                                                                                         | [operations.ConversionsGetByIdCurrencyFrom](../../models/operations/conversionsgetbyidcurrencyfrom.md) | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `currencyTo`                                                                                           | [operations.ConversionsGetByIdCurrencyTo](../../models/operations/conversionsgetbyidcurrencyto.md)     | :heavy_check_mark:                                                                                     | N/A                                                                                                    |