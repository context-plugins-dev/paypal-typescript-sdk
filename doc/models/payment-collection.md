
# Payment Collection

The collection of payments, or transactions, for a purchase unit in an order. For example, authorized payments, captured payments, and refunds.

## Structure

`PaymentCollection`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorizations` | [`AuthorizationWithAdditionalData[] \| undefined`](../../doc/models/authorization-with-additional-data.md) | Optional | An array of authorized payments for a purchase unit. A purchase unit can have zero or more authorized payments. |
| `captures` | [`OrdersCapture[] \| undefined`](../../doc/models/orders-capture.md) | Optional | An array of captured payments for a purchase unit. A purchase unit can have zero or more captured payments. |
| `refunds` | [`Refund[] \| undefined`](../../doc/models/refund.md) | Optional | An array of refunds for a purchase unit. A purchase unit can have zero or more refunds. |

## Example

```ts
import {
  AuthorizationIncompleteReason,
  AuthorizationStatus,
  CaptureIncompleteReason,
  CaptureStatus,
  PaymentCollection,
  RefundIncompleteReason,
  RefundStatus,
} from 'paypal-server-sdklib';

const paymentCollection: PaymentCollection = {
  authorizations: [
    {
      status: AuthorizationStatus.Denied,
      statusDetails: {
        reason: AuthorizationIncompleteReason.PendingReview,
      },
      id: 'id2',
      amount: {
        currencyCode: 'currency_code6',
        value: 'value0',
      },
      invoiceId: 'invoice_id2',
    }
  ],
  captures: [
    {
      status: CaptureStatus.Refunded,
      statusDetails: {
        reason: CaptureIncompleteReason.VerificationRequired,
      },
      id: 'id4',
      amount: {
        currencyCode: 'currency_code6',
        value: 'value0',
      },
      invoiceId: 'invoice_id4',
    },
    {
      status: CaptureStatus.Refunded,
      statusDetails: {
        reason: CaptureIncompleteReason.VerificationRequired,
      },
      id: 'id4',
      amount: {
        currencyCode: 'currency_code6',
        value: 'value0',
      },
      invoiceId: 'invoice_id4',
    },
    {
      status: CaptureStatus.Refunded,
      statusDetails: {
        reason: CaptureIncompleteReason.VerificationRequired,
      },
      id: 'id4',
      amount: {
        currencyCode: 'currency_code6',
        value: 'value0',
      },
      invoiceId: 'invoice_id4',
    }
  ],
  refunds: [
    {
      status: RefundStatus.Cancelled,
      statusDetails: {
        reason: RefundIncompleteReason.Echeck,
      },
      id: 'id8',
      amount: {
        currencyCode: 'currency_code6',
        value: 'value0',
      },
      invoiceId: 'invoice_id8',
    }
  ],
};
```

