<!-- Start SDK Example Usage [usage] -->
```typescript
import { Payvra } from "payvra";

const payvra = new Payvra({
  apiKey: process.env["PAYVRA_API_KEY"] ?? "",
});

async function run() {
  const result = await payvra.currencies.all();

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->