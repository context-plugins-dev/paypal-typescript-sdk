
# Token Type

The tokenization method that generated the ID.

## Enumeration

`TokenType`

## Fields

| Name | Description |
|  --- | --- |
| `BillingAgreement` | The PayPal billing agreement ID. References an approved recurring payment for goods or services. |

## Example

```ts
import { TokenType } from 'paypal-server-sdklib';

const tokenType = TokenType.BillingAgreement;
```

