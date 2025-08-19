# PayoutsListOwnedResponse

Successful response

## Example Usage

```typescript
import { PayoutsListOwnedResponse } from "payvra/models/operations";

let value: PayoutsListOwnedResponse = {
  meta: {
    hasPreviousPage: false,
    hasNextPage: true,
  },
  data: [],
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `meta`                                                                               | [operations.PayoutsListOwnedMeta](../../models/operations/payoutslistownedmeta.md)   | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `data`                                                                               | [operations.PayoutsListOwnedData](../../models/operations/payoutslistowneddata.md)[] | :heavy_check_mark:                                                                   | N/A                                                                                  |