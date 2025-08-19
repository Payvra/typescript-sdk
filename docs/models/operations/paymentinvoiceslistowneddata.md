# PaymentInvoicesListOwnedData

## Example Usage

```typescript
import { PaymentInvoicesListOwnedData } from "payvra/models/operations";

let value: PaymentInvoicesListOwnedData = {
  id: "<id>",
  walletId: "<id>",
  merchantId: "<id>",
  status: "waiting",
  underPaidCover: "<value>",
  feePaidByPayer: true,
  isWhiteLabel: false,
  priceAmount: "<value>",
  priceCurrency: "<value>",
  payAmount: "<value>",
  paidAmount: "<value>",
  receivedAmount: "<value>",
  payAddress: "<value>",
  payinExtraId: "<id>",
  payinHash: "<value>",
  orderId: "<id>",
  orderDescription: "<value>",
  callbackUrl: "https://black-and-white-academics.info/",
  returnUrl: "https://wealthy-scarification.com",
  finishedAt: "<value>",
  expiredAt: "1717111793135",
  createdAt: "1720759988575",
  updatedAt: "1735630261827",
  payCurrency: {
    id: "<id>",
    code: "<value>",
    name: "<value>",
    enabled: true,
    walletRegex: "<value>",
    priority: 741946,
    extraIdExists: true,
    extraIdRegex: "<value>",
    usdPrice: "<value>",
    minPaymentAmount: "<value>",
    minPayoutAmount: "<value>",
    minWithdrawalFeeEstimate: "<value>",
    logoUrl: "https://deadly-request.info/",
    track: false,
    cgId: "<id>",
    isMaxlimit: true,
    network: "<value>",
    smartContract: null,
    networkPrecision: "<value>",
    explorerLinkHash: "<value>",
    precision: 556873,
    ticker: "<value>",
    isDefi: false,
    isPopular: true,
    isStable: true,
    availableForToConversion: false,
    createdAt: "1725358069944",
    updatedAt: "1735614107120",
  },
  acceptedCoins: [],
};
```

## Fields

| Field                                                                                                                | Type                                                                                                                 | Required                                                                                                             | Description                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                                 | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `walletId`                                                                                                           | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `merchantId`                                                                                                         | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `status`                                                                                                             | [operations.PaymentInvoicesListOwnedStatus](../../models/operations/paymentinvoiceslistownedstatus.md)               | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `underPaidCover`                                                                                                     | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `feePaidByPayer`                                                                                                     | *boolean*                                                                                                            | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `isWhiteLabel`                                                                                                       | *boolean*                                                                                                            | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `priceAmount`                                                                                                        | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `priceCurrency`                                                                                                      | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `payAmount`                                                                                                          | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `paidAmount`                                                                                                         | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `receivedAmount`                                                                                                     | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `payAddress`                                                                                                         | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `payinExtraId`                                                                                                       | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `payinHash`                                                                                                          | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `orderId`                                                                                                            | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `orderDescription`                                                                                                   | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `callbackUrl`                                                                                                        | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `returnUrl`                                                                                                          | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `finishedAt`                                                                                                         | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `expiredAt`                                                                                                          | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `createdAt`                                                                                                          | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `updatedAt`                                                                                                          | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `payCurrency`                                                                                                        | [operations.PaymentInvoicesListOwnedPayCurrency](../../models/operations/paymentinvoiceslistownedpaycurrency.md)     | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `acceptedCoins`                                                                                                      | [operations.PaymentInvoicesListOwnedAcceptedCoin](../../models/operations/paymentinvoiceslistownedacceptedcoin.md)[] | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |