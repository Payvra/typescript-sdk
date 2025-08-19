# PayoutsGetByIdResponse

Successful response

## Example Usage

```typescript
import { PayoutsGetByIdResponse } from "payvra/models/operations";

let value: PayoutsGetByIdResponse = {
  id: "<id>",
  walletId: "<id>",
  merchantId: "<id>",
  currencyId: "<id>",
  status: "sending",
  amount: "797.58",
  address: "602 Evert Ferry",
  extraId: "<id>",
  txHash: "<value>",
  fee: "<value>",
  callbackUrl: null,
  createdAt: "1705441968145",
  updatedAt: "1735651487063",
  currency: {
    id: "<id>",
    code: "<value>",
    name: "<value>",
    enabled: true,
    walletRegex: "<value>",
    priority: 395690,
    extraIdExists: true,
    extraIdRegex: "<value>",
    usdPrice: "<value>",
    minPaymentAmount: "<value>",
    minPayoutAmount: "<value>",
    minWithdrawalFeeEstimate: "<value>",
    logoUrl: "https://tattered-igloo.biz/",
    track: true,
    cgId: "<id>",
    isMaxlimit: true,
    network: "<value>",
    smartContract: "<value>",
    networkPrecision: "<value>",
    explorerLinkHash: null,
    precision: 585413,
    ticker: "<value>",
    isDefi: false,
    isPopular: false,
    isStable: true,
    availableForToConversion: false,
    createdAt: "1721156107167",
    updatedAt: "1735608879517",
  },
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `id`                                                                                   | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `walletId`                                                                             | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `merchantId`                                                                           | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `currencyId`                                                                           | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `status`                                                                               | [operations.PayoutsGetByIdStatus](../../models/operations/payoutsgetbyidstatus.md)     | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `amount`                                                                               | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `address`                                                                              | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `extraId`                                                                              | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `txHash`                                                                               | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `fee`                                                                                  | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `callbackUrl`                                                                          | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `createdAt`                                                                            | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `updatedAt`                                                                            | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `currency`                                                                             | [operations.PayoutsGetByIdCurrency](../../models/operations/payoutsgetbyidcurrency.md) | :heavy_check_mark:                                                                     | N/A                                                                                    |