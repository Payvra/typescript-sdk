# WalletsListOwnedData

## Example Usage

```typescript
import { WalletsListOwnedData } from "payvra/models/operations";

let value: WalletsListOwnedData = {
  id: "<id>",
  merchantId: "<id>",
  currencyId: "<id>",
  balance: "<value>",
  pendingBalance: "<value>",
  createdAt: "1728884375087",
  updatedAt: "1735603316093",
  currency: {
    id: "<id>",
    code: "<value>",
    name: "<value>",
    enabled: true,
    walletRegex: "<value>",
    priority: 16704,
    extraIdExists: false,
    extraIdRegex: "<value>",
    usdPrice: "<value>",
    minPaymentAmount: "<value>",
    minPayoutAmount: "<value>",
    minWithdrawalFeeEstimate: "<value>",
    logoUrl: "https://limping-summer.com/",
    track: true,
    cgId: "<id>",
    isMaxlimit: false,
    network: "<value>",
    smartContract: "<value>",
    networkPrecision: "<value>",
    explorerLinkHash: "<value>",
    precision: 657203,
    ticker: "<value>",
    isDefi: false,
    isPopular: false,
    isStable: false,
    availableForToConversion: false,
    createdAt: "1713828163947",
    updatedAt: "1735671726146",
  },
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `id`                                                                                       | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `merchantId`                                                                               | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `currencyId`                                                                               | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `balance`                                                                                  | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `pendingBalance`                                                                           | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `createdAt`                                                                                | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `updatedAt`                                                                                | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `currency`                                                                                 | [operations.WalletsListOwnedCurrency](../../models/operations/walletslistownedcurrency.md) | :heavy_check_mark:                                                                         | N/A                                                                                        |