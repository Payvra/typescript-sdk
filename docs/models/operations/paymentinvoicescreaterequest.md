# PaymentInvoicesCreateRequest

## Example Usage

```typescript
import { PaymentInvoicesCreateRequest } from "payvra/models/operations";

let value: PaymentInvoicesCreateRequest = {
  amount: 6259.25,
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
| `acceptedCoins`    | *string*[]         | :heavy_minus_sign: | N/A                |
| `returnUrl`        | *string*           | :heavy_minus_sign: | N/A                |