# ErrorFORBIDDEN

The error information

## Example Usage

```typescript
import { ErrorFORBIDDEN } from "payvra/models/errors";

// No examples available for this model
```

## Fields

| Field                                                               | Type                                                                | Required                                                            | Description                                                         | Example                                                             |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `message`                                                           | *string*                                                            | :heavy_check_mark:                                                  | The error message                                                   | Insufficient access                                                 |
| `code`                                                              | *string*                                                            | :heavy_check_mark:                                                  | The error code                                                      | FORBIDDEN                                                           |
| `issues`                                                            | [models.ErrorFORBIDDENIssue](../../models/errorforbiddenissue.md)[] | :heavy_minus_sign:                                                  | An array of issues that were responsible for the error              | []                                                                  |