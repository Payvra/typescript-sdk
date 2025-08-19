# PaymentInvoicesListOwnedResponse

Successful response

## Example Usage

```typescript
import { PaymentInvoicesListOwnedResponse } from "payvra/models/operations";

let value: PaymentInvoicesListOwnedResponse = {
  meta: {
    hasPreviousPage: false,
    hasNextPage: true,
  },
  data: [],
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `meta`                                                                                               | [operations.PaymentInvoicesListOwnedMeta](../../models/operations/paymentinvoiceslistownedmeta.md)   | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `data`                                                                                               | [operations.PaymentInvoicesListOwnedData](../../models/operations/paymentinvoiceslistowneddata.md)[] | :heavy_check_mark:                                                                                   | N/A                                                                                                  |