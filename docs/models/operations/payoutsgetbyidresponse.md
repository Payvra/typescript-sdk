# PayoutsGetByIdResponse

Successful response

## Example Usage

```typescript
import { PayoutsGetByIdResponse } from "payvra/models/operations";

let value: PayoutsGetByIdResponse = {
  id: "<id>",
  walletId: "<id>",
  merchantId: "<id>",
  status: "failed",
  underPaidCover: "<value>",
  feePaidByPayer: false,
  isWhiteLabel: false,
  priceAmount: "<value>",
  priceCurrency: "<value>",
  payAmount: null,
  paidAmount: "<value>",
  receivedAmount: "<value>",
  payAddress: "<value>",
  payinExtraId: null,
  payinHash: "<value>",
  orderId: "<id>",
  orderDescription: "<value>",
  callbackUrl: "https://abandoned-anticodon.name/",
  returnUrl: "https://immense-digit.net/",
  finishedAt: "<value>",
  expiredAt: "1709117833032",
  createdAt: "1730564563842",
  updatedAt: "1735642321170",
  payCurrency: {
    id: "<id>",
    code: "<value>",
    name: "<value>",
    enabled: true,
    walletRegex: "<value>",
    priority: 217753,
    extraIdExists: true,
    extraIdRegex: "<value>",
    usdPrice: "<value>",
    minPaymentAmount: "<value>",
    minPayoutAmount: "<value>",
    minWithdrawalFeeEstimate: "<value>",
    logoUrl: "https://bustling-monster.info/",
    track: false,
    cgId: "<id>",
    isMaxlimit: true,
    network: "<value>",
    smartContract: "<value>",
    networkPrecision: null,
    explorerLinkHash: "<value>",
    precision: 263414,
    ticker: "<value>",
    isDefi: false,
    isPopular: false,
    isStable: true,
    availableForToConversion: true,
    createdAt: "1717990184385",
    updatedAt: "1735625369071",
  },
  acceptedCoins: [
    {
      id: "<id>",
      code: "<value>",
      name: "<value>",
      enabled: true,
      walletRegex: "<value>",
      priority: 628736,
      extraIdExists: true,
      extraIdRegex: "<value>",
      usdPrice: "<value>",
      minPaymentAmount: "<value>",
      minPayoutAmount: "<value>",
      minWithdrawalFeeEstimate: "<value>",
      logoUrl: "https://easy-formula.org",
      track: true,
      cgId: "<id>",
      isMaxlimit: true,
      network: "<value>",
      smartContract: "<value>",
      networkPrecision: "<value>",
      explorerLinkHash: "<value>",
      precision: 90846,
      ticker: "<value>",
      isDefi: true,
      isPopular: true,
      isStable: false,
      availableForToConversion: true,
      createdAt: "1705937427630",
      updatedAt: "1735626133668",
    },
  ],
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `id`                                                                                             | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `walletId`                                                                                       | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `merchantId`                                                                                     | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `status`                                                                                         | [operations.PayoutsGetByIdStatus](../../models/operations/payoutsgetbyidstatus.md)               | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `underPaidCover`                                                                                 | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `feePaidByPayer`                                                                                 | *boolean*                                                                                        | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `isWhiteLabel`                                                                                   | *boolean*                                                                                        | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `priceAmount`                                                                                    | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `priceCurrency`                                                                                  | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `payAmount`                                                                                      | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `paidAmount`                                                                                     | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `receivedAmount`                                                                                 | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `payAddress`                                                                                     | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `payinExtraId`                                                                                   | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `payinHash`                                                                                      | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `orderId`                                                                                        | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `orderDescription`                                                                               | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `callbackUrl`                                                                                    | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `returnUrl`                                                                                      | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `finishedAt`                                                                                     | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `expiredAt`                                                                                      | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `createdAt`                                                                                      | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `updatedAt`                                                                                      | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `payCurrency`                                                                                    | [operations.PayoutsGetByIdPayCurrency](../../models/operations/payoutsgetbyidpaycurrency.md)     | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `acceptedCoins`                                                                                  | [operations.PayoutsGetByIdAcceptedCoin](../../models/operations/payoutsgetbyidacceptedcoin.md)[] | :heavy_check_mark:                                                                               | N/A                                                                                              |