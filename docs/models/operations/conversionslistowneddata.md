# ConversionsListOwnedData

## Example Usage

```typescript
import { ConversionsListOwnedData } from "payvra/models/operations";

let value: ConversionsListOwnedData = {
  id: "<id>",
  merchantId: "<id>",
  walletFromId: "<id>",
  walletToId: "<id>",
  status: "waiting",
  amountFrom: "<value>",
  amountTo: "<value>",
  callbackUrl: "https://naughty-hovel.biz/",
  createdAt: "1722483692967",
  updatedAt: "1735642628397",
  currencyFrom: {
    id: "<id>",
    code: "<value>",
    name: "<value>",
    enabled: false,
    walletRegex: "<value>",
    priority: 728247,
    extraIdExists: true,
    extraIdRegex: "<value>",
    usdPrice: "<value>",
    minPaymentAmount: "<value>",
    minPayoutAmount: "<value>",
    minWithdrawalFeeEstimate: "<value>",
    logoUrl: "https://sick-horst.com",
    track: false,
    cgId: "<id>",
    isMaxlimit: true,
    network: "<value>",
    smartContract: "<value>",
    networkPrecision: "<value>",
    explorerLinkHash: "<value>",
    precision: 602993,
    ticker: "<value>",
    isDefi: true,
    isPopular: true,
    isStable: true,
    availableForToConversion: true,
    createdAt: "1705370826134",
    updatedAt: "1735613252256",
  },
  currencyTo: {
    id: "<id>",
    code: "<value>",
    name: "<value>",
    enabled: true,
    walletRegex: "<value>",
    priority: 279448,
    extraIdExists: false,
    extraIdRegex: "<value>",
    usdPrice: "<value>",
    minPaymentAmount: "<value>",
    minPayoutAmount: "<value>",
    minWithdrawalFeeEstimate: "<value>",
    logoUrl: "https://oval-mortise.biz/",
    track: false,
    cgId: "<id>",
    isMaxlimit: true,
    network: "<value>",
    smartContract: "<value>",
    networkPrecision: "<value>",
    explorerLinkHash: "<value>",
    precision: 500345,
    ticker: "<value>",
    isDefi: false,
    isPopular: true,
    isStable: false,
    availableForToConversion: true,
    createdAt: "1735508860136",
    updatedAt: "1735682843634",
  },
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                       | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `merchantId`                                                                                               | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `walletFromId`                                                                                             | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `walletToId`                                                                                               | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `status`                                                                                                   | [operations.ConversionsListOwnedStatus](../../models/operations/conversionslistownedstatus.md)             | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `amountFrom`                                                                                               | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `amountTo`                                                                                                 | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `callbackUrl`                                                                                              | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `createdAt`                                                                                                | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `updatedAt`                                                                                                | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `currencyFrom`                                                                                             | [operations.ConversionsListOwnedCurrencyFrom](../../models/operations/conversionslistownedcurrencyfrom.md) | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `currencyTo`                                                                                               | [operations.ConversionsListOwnedCurrencyTo](../../models/operations/conversionslistownedcurrencyto.md)     | :heavy_check_mark:                                                                                         | N/A                                                                                                        |