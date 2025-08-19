# PaymentInvoicesCreateWhiteLabelResponse

Successful response

## Example Usage

```typescript
import { PaymentInvoicesCreateWhiteLabelResponse } from "payvra/models/operations";

let value: PaymentInvoicesCreateWhiteLabelResponse = {
  id: "<id>",
  walletId: "<id>",
  merchantId: "<id>",
  status: "partially_paid",
  underPaidCover: "<value>",
  feePaidByPayer: true,
  isWhiteLabel: true,
  priceAmount: "<value>",
  priceCurrency: "<value>",
  payAmount: "<value>",
  paidAmount: "<value>",
  receivedAmount: "<value>",
  payAddress: null,
  payinExtraId: "<id>",
  payinHash: null,
  orderId: "<id>",
  orderDescription: "<value>",
  callbackUrl: "https://comfortable-jump.org",
  finishedAt: null,
  expiredAt: "1730795293555",
  createdAt: "1728662768057",
  updatedAt: "1735678041938",
  payCurrency: {
    id: "<id>",
    code: "<value>",
    name: "<value>",
    enabled: false,
    walletRegex: "<value>",
    priority: 278752,
    extraIdExists: true,
    extraIdRegex: null,
    usdPrice: "<value>",
    minPaymentAmount: "<value>",
    minPayoutAmount: "<value>",
    minWithdrawalFeeEstimate: "<value>",
    logoUrl: "https://lost-synergy.net",
    track: false,
    cgId: "<id>",
    isMaxlimit: true,
    network: "<value>",
    smartContract: "<value>",
    networkPrecision: "<value>",
    explorerLinkHash: "<value>",
    precision: 416982,
    ticker: "<value>",
    isDefi: true,
    isPopular: false,
    isStable: true,
    availableForToConversion: true,
    createdAt: "1734142459650",
    updatedAt: "1735627473522",
  },
  acceptedCoins: [],
};
```

## Fields

| Field                                                                                                                              | Type                                                                                                                               | Required                                                                                                                           | Description                                                                                                                        |
| ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                                               | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `walletId`                                                                                                                         | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `merchantId`                                                                                                                       | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `status`                                                                                                                           | [operations.PaymentInvoicesCreateWhiteLabelStatus](../../models/operations/paymentinvoicescreatewhitelabelstatus.md)               | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `underPaidCover`                                                                                                                   | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `feePaidByPayer`                                                                                                                   | *boolean*                                                                                                                          | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `isWhiteLabel`                                                                                                                     | *boolean*                                                                                                                          | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `priceAmount`                                                                                                                      | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `priceCurrency`                                                                                                                    | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `payAmount`                                                                                                                        | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `paidAmount`                                                                                                                       | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `receivedAmount`                                                                                                                   | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `payAddress`                                                                                                                       | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `payinExtraId`                                                                                                                     | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `payinHash`                                                                                                                        | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `orderId`                                                                                                                          | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `orderDescription`                                                                                                                 | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `callbackUrl`                                                                                                                      | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `finishedAt`                                                                                                                       | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `expiredAt`                                                                                                                        | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `createdAt`                                                                                                                        | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `updatedAt`                                                                                                                        | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `payCurrency`                                                                                                                      | [operations.PaymentInvoicesCreateWhiteLabelPayCurrency](../../models/operations/paymentinvoicescreatewhitelabelpaycurrency.md)     | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `acceptedCoins`                                                                                                                    | [operations.PaymentInvoicesCreateWhiteLabelAcceptedCoin](../../models/operations/paymentinvoicescreatewhitelabelacceptedcoin.md)[] | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |