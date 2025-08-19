# WalletsListOwnedResponse

Successful response

## Example Usage

```typescript
import { WalletsListOwnedResponse } from "payvra/models/operations";

let value: WalletsListOwnedResponse = {
  meta: {
    hasPreviousPage: true,
    hasNextPage: true,
  },
  data: [
    {
      id: "<id>",
      merchantId: "<id>",
      currencyId: "<id>",
      balance: "<value>",
      pendingBalance: "<value>",
      createdAt: "1722483491006",
      updatedAt: "1735621514759",
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
    },
  ],
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `meta`                                                                               | [operations.WalletsListOwnedMeta](../../models/operations/walletslistownedmeta.md)   | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `data`                                                                               | [operations.WalletsListOwnedData](../../models/operations/walletslistowneddata.md)[] | :heavy_check_mark:                                                                   | N/A                                                                                  |