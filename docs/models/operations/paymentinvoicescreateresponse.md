# PaymentInvoicesCreateResponse

Successful response

## Example Usage

```typescript
import { PaymentInvoicesCreateResponse } from "payvra/models/operations";

let value: PaymentInvoicesCreateResponse = {
  id: "<id>",
  walletId: "<id>",
  merchantId: "<id>",
  status: "failed",
  underPaidCover: "<value>",
  feePaidByPayer: false,
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
  callbackUrl: "https://serene-tuxedo.net/",
  returnUrl: "https://metallic-tributary.com/",
  finishedAt: "<value>",
  expiredAt: "1713848472800",
  createdAt: "1717502054896",
  updatedAt: "1735673244566",
  payCurrency: {
    id: "<id>",
    code: "<value>",
    name: "<value>",
    enabled: true,
    walletRegex: "<value>",
    priority: 274266,
    extraIdExists: true,
    extraIdRegex: null,
    usdPrice: "<value>",
    minPaymentAmount: "<value>",
    minPayoutAmount: "<value>",
    minWithdrawalFeeEstimate: "<value>",
    logoUrl: "https://internal-sarong.name/",
    track: false,
    cgId: "<id>",
    isMaxlimit: false,
    network: "<value>",
    smartContract: null,
    networkPrecision: "<value>",
    explorerLinkHash: "<value>",
    precision: 254157,
    ticker: "<value>",
    isDefi: true,
    isPopular: false,
    isStable: true,
    availableForToConversion: false,
    createdAt: "1730086371108",
    updatedAt: "1735603490075",
  },
  acceptedCoins: [
    {
      id: "<id>",
      code: "<value>",
      name: "<value>",
      enabled: false,
      walletRegex: "<value>",
      priority: 321004,
      extraIdExists: true,
      extraIdRegex: "<value>",
      usdPrice: "<value>",
      minPaymentAmount: "<value>",
      minPayoutAmount: "<value>",
      minWithdrawalFeeEstimate: "<value>",
      logoUrl: "https://imaginative-blowgun.com/",
      track: false,
      cgId: "<id>",
      isMaxlimit: false,
      network: "<value>",
      smartContract: "<value>",
      networkPrecision: "<value>",
      explorerLinkHash: "<value>",
      precision: 717596,
      ticker: "<value>",
      isDefi: false,
      isPopular: true,
      isStable: false,
      availableForToConversion: false,
      createdAt: "1731986171041",
      updatedAt: "1735675047730",
    },
  ],
  paymentUrl: "https://amused-kick.org",
};
```

## Fields

| Field                                                                                                          | Type                                                                                                           | Required                                                                                                       | Description                                                                                                    |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                           | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `walletId`                                                                                                     | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `merchantId`                                                                                                   | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `status`                                                                                                       | [operations.PaymentInvoicesCreateStatus](../../models/operations/paymentinvoicescreatestatus.md)               | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `underPaidCover`                                                                                               | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `feePaidByPayer`                                                                                               | *boolean*                                                                                                      | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `isWhiteLabel`                                                                                                 | *boolean*                                                                                                      | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `priceAmount`                                                                                                  | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `priceCurrency`                                                                                                | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `payAmount`                                                                                                    | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `paidAmount`                                                                                                   | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `receivedAmount`                                                                                               | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `payAddress`                                                                                                   | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `payinExtraId`                                                                                                 | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `payinHash`                                                                                                    | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `orderId`                                                                                                      | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `orderDescription`                                                                                             | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `callbackUrl`                                                                                                  | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `returnUrl`                                                                                                    | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `finishedAt`                                                                                                   | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `expiredAt`                                                                                                    | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `createdAt`                                                                                                    | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `updatedAt`                                                                                                    | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `payCurrency`                                                                                                  | [operations.PaymentInvoicesCreatePayCurrency](../../models/operations/paymentinvoicescreatepaycurrency.md)     | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `acceptedCoins`                                                                                                | [operations.PaymentInvoicesCreateAcceptedCoin](../../models/operations/paymentinvoicescreateacceptedcoin.md)[] | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `paymentUrl`                                                                                                   | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |