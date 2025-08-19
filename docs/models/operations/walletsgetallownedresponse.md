# WalletsGetAllOwnedResponse

## Example Usage

```typescript
import { WalletsGetAllOwnedResponse } from "payvra/models/operations";

let value: WalletsGetAllOwnedResponse = {
  id: "<id>",
  merchantId: "<id>",
  currencyId: "<id>",
  balance: "<value>",
  pendingBalance: "<value>",
  createdAt: "1705488704908",
  updatedAt: "1735674472769",
  currency: {
    id: "<id>",
    code: "<value>",
    name: "<value>",
    enabled: true,
    walletRegex: "<value>",
    priority: 157125,
    extraIdExists: true,
    extraIdRegex: "<value>",
    usdPrice: "<value>",
    minPaymentAmount: "<value>",
    minPayoutAmount: "<value>",
    minWithdrawalFeeEstimate: "<value>",
    logoUrl: "https://hidden-bench.org",
    track: true,
    cgId: "<id>",
    isMaxlimit: false,
    network: null,
    smartContract: "<value>",
    networkPrecision: null,
    explorerLinkHash: "<value>",
    precision: 114513,
    ticker: "<value>",
    isDefi: true,
    isPopular: true,
    isStable: false,
    availableForToConversion: true,
    createdAt: "1727035745345",
    updatedAt: "1735648887507",
  },
};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `id`                                                                                           | *string*                                                                                       | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `merchantId`                                                                                   | *string*                                                                                       | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `currencyId`                                                                                   | *string*                                                                                       | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `balance`                                                                                      | *string*                                                                                       | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `pendingBalance`                                                                               | *string*                                                                                       | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `createdAt`                                                                                    | *string*                                                                                       | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `updatedAt`                                                                                    | *string*                                                                                       | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `currency`                                                                                     | [operations.WalletsGetAllOwnedCurrency](../../models/operations/walletsgetallownedcurrency.md) | :heavy_check_mark:                                                                             | N/A                                                                                            |