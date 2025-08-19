# ErrorUNAUTHORIZED

The error information

## Example Usage

```typescript
import { ErrorUNAUTHORIZED } from "payvra/models/errors";

// No examples available for this model
```

## Fields

| Field                                                                     | Type                                                                      | Required                                                                  | Description                                                               | Example                                                                   |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `message`                                                                 | *string*                                                                  | :heavy_check_mark:                                                        | The error message                                                         | Authorization not provided                                                |
| `code`                                                                    | *string*                                                                  | :heavy_check_mark:                                                        | The error code                                                            | UNAUTHORIZED                                                              |
| `issues`                                                                  | [models.ErrorUNAUTHORIZEDIssue](../../models/errorunauthorizedissue.md)[] | :heavy_minus_sign:                                                        | An array of issues that were responsible for the error                    | []                                                                        |