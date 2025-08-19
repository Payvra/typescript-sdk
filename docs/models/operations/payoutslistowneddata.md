# PayoutsListOwnedData

## Example Usage

```typescript
import { PayoutsListOwnedData } from "payvra/models/operations";

let value: PayoutsListOwnedData = {
  id: "<id>",
  walletId: "<id>",
  merchantId: "<id>",
  currencyId: "<id>",
  status: "processing",
  amount: "256.17",
  address: "203 Kuhn Meadow",
  extraId: "<id>",
  txHash: null,
  fee: "<value>",
  callbackUrl: "https://winding-duffel.info",
  createdAt: "1715163158035",
  updatedAt: "1735679057521",
  currency: null,
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `id`                                                                                       | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `walletId`                                                                                 | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `merchantId`                                                                               | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `currencyId`                                                                               | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `status`                                                                                   | [operations.PayoutsListOwnedStatus](../../models/operations/payoutslistownedstatus.md)     | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `amount`                                                                                   | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `address`                                                                                  | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `extraId`                                                                                  | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `txHash`                                                                                   | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `fee`                                                                                      | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `callbackUrl`                                                                              | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `createdAt`                                                                                | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `updatedAt`                                                                                | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `currency`                                                                                 | [operations.PayoutsListOwnedCurrency](../../models/operations/payoutslistownedcurrency.md) | :heavy_check_mark:                                                                         | N/A                                                                                        |