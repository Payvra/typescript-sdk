# PaymentInvoicesCreateWhiteLabelRequest

## Example Usage

```typescript
import { PaymentInvoicesCreateWhiteLabelRequest } from "payvra/models/operations";

let value: PaymentInvoicesCreateWhiteLabelRequest = {
  amount: 9251.94,
  payAddress: "<value>",
  payinExtraId: "<id>",
  payCurrency: "<value>",
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `feePaidByPayer`   | *boolean*          | :heavy_minus_sign: | N/A                |
| `callbackUrl`      | *string*           | :heavy_minus_sign: | N/A                |
| `amount`           | *number*           | :heavy_check_mark: | N/A                |
| `amountCurrency`   | *string*           | :heavy_minus_sign: | N/A                |
| `underPaidCover`   | *number*           | :heavy_minus_sign: | N/A                |
| `lifeTime`         | *number*           | :heavy_minus_sign: | N/A                |
| `payAddress`       | *string*           | :heavy_check_mark: | N/A                |
| `payinExtraId`     | *string*           | :heavy_check_mark: | N/A                |
| `payCurrency`      | *string*           | :heavy_check_mark: | N/A                |