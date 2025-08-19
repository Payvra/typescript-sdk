# ErrorNOTFOUND

The error information

## Example Usage

```typescript
import { ErrorNOTFOUND } from "payvra/models/errors";

// No examples available for this model
```

## Fields

| Field                                                             | Type                                                              | Required                                                          | Description                                                       | Example                                                           |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `message`                                                         | *string*                                                          | :heavy_check_mark:                                                | The error message                                                 | Not found                                                         |
| `code`                                                            | *string*                                                          | :heavy_check_mark:                                                | The error code                                                    | NOT_FOUND                                                         |
| `issues`                                                          | [models.ErrorNOTFOUNDIssue](../../models/errornotfoundissue.md)[] | :heavy_minus_sign:                                                | An array of issues that were responsible for the error            | []                                                                |