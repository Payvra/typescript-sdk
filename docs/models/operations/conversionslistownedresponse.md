# ConversionsListOwnedResponse

Successful response

## Example Usage

```typescript
import { ConversionsListOwnedResponse } from "payvra/models/operations";

let value: ConversionsListOwnedResponse = {
  meta: {
    hasPreviousPage: false,
    hasNextPage: true,
  },
  data: [
    {
      id: "<id>",
      merchantId: "<id>",
      walletFromId: "<id>",
      walletToId: "<id>",
      status: "waiting",
      amountFrom: "<value>",
      amountTo: "<value>",
      callbackUrl: null,
      createdAt: "1718117044921",
      updatedAt: "1735662449617",
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
    },
  ],
};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `meta`                                                                                       | [operations.ConversionsListOwnedMeta](../../models/operations/conversionslistownedmeta.md)   | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `data`                                                                                       | [operations.ConversionsListOwnedData](../../models/operations/conversionslistowneddata.md)[] | :heavy_check_mark:                                                                           | N/A                                                                                          |