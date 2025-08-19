# PayoutsCreateRequest

## Example Usage

```typescript
import { PayoutsCreateRequest } from "payvra/models/operations";

let value: PayoutsCreateRequest = {
  amount: "860.31",
  address: "79415 Hazel Grove",
  currency: "UAE Dirham",
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `amount`           | *string*           | :heavy_check_mark: | N/A                |
| `address`          | *string*           | :heavy_check_mark: | N/A                |
| `extraId`          | *string*           | :heavy_minus_sign: | N/A                |
| `callbackUrl`      | *string*           | :heavy_minus_sign: | N/A                |
| `currency`         | *string*           | :heavy_check_mark: | N/A                |