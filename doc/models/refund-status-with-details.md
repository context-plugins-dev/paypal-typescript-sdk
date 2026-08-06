
# Refund Status with Details

The refund status with details.

## Structure

`RefundStatusWithDetails`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`RefundStatus \| undefined`](../../doc/models/refund-status.md) | Optional, Read-only | The status of the refund. |
| `statusDetails` | [`RefundStatusDetails \| undefined`](../../doc/models/refund-status-details.md) | Optional | The details of the refund status. |

## Example

```ts
import {
  RefundIncompleteReason,
  RefundStatus,
  RefundStatusWithDetails,
} from 'paypal-server-sdklib';

const refundStatusWithDetails: RefundStatusWithDetails = {
  status: RefundStatus.Cancelled,
  statusDetails: {
    reason: RefundIncompleteReason.Echeck,
  },
};
```

