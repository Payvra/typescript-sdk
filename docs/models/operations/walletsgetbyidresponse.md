# WalletsGetByIdResponse

Successful response

## Example Usage

```typescript
import { WalletsGetByIdResponse } from "payvra/models/operations";

let value: WalletsGetByIdResponse = {
  id: "<id>",
  merchantId: "<id>",
  currencyId: "<id>",
  balance: "<value>",
  pendingBalance: "<value>",
  createdAt: "1708506863362",
  updatedAt: "1735639623619",
  currency: {
    id: "<id>",
    code: "<value>",
    name: "<value>",
    enabled: true,
    walletRegex: "<value>",
    priority: 884793,
    extraIdExists: true,
    extraIdRegex: "<value>",
    usdPrice: "<value>",
    minPaymentAmount: "<value>",
    minPayoutAmount: "<value>",
    minWithdrawalFeeEstimate: "<value>",
    logoUrl: "https://stark-angle.org",
    track: true,
    cgId: "<id>",
    isMaxlimit: true,
    network: "<value>",
    smartContract: "<value>",
    networkPrecision: "<value>",
    explorerLinkHash: "<value>",
    precision: 599179,
    ticker: "<value>",
    isDefi: false,
    isPopular: true,
    isStable: false,
    availableForToConversion: false,
    createdAt: "1724474891275",
    updatedAt: "1735652784944",
  },
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `id`                                                                                   | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `merchantId`                                                                           | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `currencyId`                                                                           | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `balance`                                                                              | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `pendingBalance`                                                                       | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `createdAt`                                                                            | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `updatedAt`                                                                            | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `currency`                                                                             | [operations.WalletsGetByIdCurrency](../../models/operations/walletsgetbyidcurrency.md) | :heavy_check_mark:                                                                     | N/A                                                                                    |