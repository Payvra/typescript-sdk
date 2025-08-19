# PayoutsCreateResponse

Successful response

## Example Usage

```typescript
import { PayoutsCreateResponse } from "payvra/models/operations";

let value: PayoutsCreateResponse = {
  id: "<id>",
  walletId: "<id>",
  merchantId: "<id>",
  currencyId: "<id>",
  status: "creating",
  amount: "267.79",
  address: "424 Well Lane",
  extraId: "<id>",
  txHash: "<value>",
  fee: "<value>",
  callbackUrl: "https://lost-tackle.org/",
  createdAt: "1705335513171",
  updatedAt: "1735621592610",
  currency: {
    id: "<id>",
    code: "<value>",
    name: "<value>",
    enabled: false,
    walletRegex: "<value>",
    priority: 246901,
    extraIdExists: false,
    extraIdRegex: null,
    usdPrice: "<value>",
    minPaymentAmount: "<value>",
    minPayoutAmount: "<value>",
    minWithdrawalFeeEstimate: "<value>",
    logoUrl: "https://smoggy-flat.name",
    track: false,
    cgId: "<id>",
    isMaxlimit: true,
    network: "<value>",
    smartContract: "<value>",
    networkPrecision: "<value>",
    explorerLinkHash: "<value>",
    precision: 149795,
    ticker: "<value>",
    isDefi: true,
    isPopular: true,
    isStable: true,
    availableForToConversion: false,
    createdAt: "1717243999348",
    updatedAt: "1735668388796",
  },
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `id`                                                                                 | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `walletId`                                                                           | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `merchantId`                                                                         | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `currencyId`                                                                         | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `status`                                                                             | [operations.PayoutsCreateStatus](../../models/operations/payoutscreatestatus.md)     | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `amount`                                                                             | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `address`                                                                            | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `extraId`                                                                            | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `txHash`                                                                             | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `fee`                                                                                | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `callbackUrl`                                                                        | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `createdAt`                                                                          | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `updatedAt`                                                                          | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `currency`                                                                           | [operations.PayoutsCreateCurrency](../../models/operations/payoutscreatecurrency.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |