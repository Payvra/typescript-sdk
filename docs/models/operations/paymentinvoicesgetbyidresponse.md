# PaymentInvoicesGetByIdResponse

Successful response

## Example Usage

```typescript
import { PaymentInvoicesGetByIdResponse } from "payvra/models/operations";

let value: PaymentInvoicesGetByIdResponse = {
  id: "<id>",
  walletId: "<id>",
  merchantId: "<id>",
  status: "waiting",
  underPaidCover: "<value>",
  feePaidByPayer: true,
  isWhiteLabel: true,
  priceAmount: "<value>",
  priceCurrency: "<value>",
  payAmount: "<value>",
  paidAmount: "<value>",
  receivedAmount: "<value>",
  payAddress: "<value>",
  payinExtraId: null,
  payinHash: "<value>",
  orderId: "<id>",
  orderDescription: "<value>",
  callbackUrl: "https://baggy-soliloquy.org",
  returnUrl: "https://primary-safe.net/",
  finishedAt: null,
  expiredAt: "1714200263004",
  createdAt: "1732469454646",
  updatedAt: "1735603881853",
  payCurrency: {
    id: "<id>",
    code: "<value>",
    name: "<value>",
    enabled: true,
    walletRegex: "<value>",
    priority: 809304,
    extraIdExists: true,
    extraIdRegex: "<value>",
    usdPrice: "<value>",
    minPaymentAmount: "<value>",
    minPayoutAmount: "<value>",
    minWithdrawalFeeEstimate: "<value>",
    logoUrl: "https://anguished-corporation.org",
    track: true,
    cgId: "<id>",
    isMaxlimit: false,
    network: "<value>",
    smartContract: "<value>",
    networkPrecision: "<value>",
    explorerLinkHash: null,
    precision: 998232,
    ticker: "<value>",
    isDefi: false,
    isPopular: false,
    isStable: true,
    availableForToConversion: true,
    createdAt: "1710068178674",
    updatedAt: "1735660066694",
  },
  acceptedCoins: [
    {
      id: "<id>",
      code: "<value>",
      name: "<value>",
      enabled: true,
      walletRegex: "<value>",
      priority: 650578,
      extraIdExists: false,
      extraIdRegex: "<value>",
      usdPrice: "<value>",
      minPaymentAmount: "<value>",
      minPayoutAmount: "<value>",
      minWithdrawalFeeEstimate: "<value>",
      logoUrl: "https://spanish-galoshes.com/",
      track: false,
      cgId: "<id>",
      isMaxlimit: true,
      network: "<value>",
      smartContract: "<value>",
      networkPrecision: "<value>",
      explorerLinkHash: "<value>",
      precision: 21120,
      ticker: null,
      isDefi: true,
      isPopular: true,
      isStable: true,
      availableForToConversion: true,
      createdAt: "1716665454365",
      updatedAt: "1735644801945",
    },
  ],
};
```

## Fields

| Field                                                                                                            | Type                                                                                                             | Required                                                                                                         | Description                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                             | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `walletId`                                                                                                       | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `merchantId`                                                                                                     | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `status`                                                                                                         | [operations.PaymentInvoicesGetByIdStatus](../../models/operations/paymentinvoicesgetbyidstatus.md)               | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `underPaidCover`                                                                                                 | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `feePaidByPayer`                                                                                                 | *boolean*                                                                                                        | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `isWhiteLabel`                                                                                                   | *boolean*                                                                                                        | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `priceAmount`                                                                                                    | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `priceCurrency`                                                                                                  | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `payAmount`                                                                                                      | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `paidAmount`                                                                                                     | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `receivedAmount`                                                                                                 | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `payAddress`                                                                                                     | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `payinExtraId`                                                                                                   | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `payinHash`                                                                                                      | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `orderId`                                                                                                        | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `orderDescription`                                                                                               | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `callbackUrl`                                                                                                    | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `returnUrl`                                                                                                      | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `finishedAt`                                                                                                     | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `expiredAt`                                                                                                      | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `createdAt`                                                                                                      | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `updatedAt`                                                                                                      | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `payCurrency`                                                                                                    | [operations.PaymentInvoicesGetByIdPayCurrency](../../models/operations/paymentinvoicesgetbyidpaycurrency.md)     | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `acceptedCoins`                                                                                                  | [operations.PaymentInvoicesGetByIdAcceptedCoin](../../models/operations/paymentinvoicesgetbyidacceptedcoin.md)[] | :heavy_check_mark:                                                                                               | N/A                                                                                                              |