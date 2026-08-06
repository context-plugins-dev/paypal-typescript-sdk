
# Capture Status with Details

The status and status details of a captured payment.

## Structure

`CaptureStatusWithDetails`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`CaptureStatus \| undefined`](../../doc/models/capture-status.md) | Optional, Read-only | The status of the captured payment. |
| `statusDetails` | [`CaptureStatusDetails \| undefined`](../../doc/models/capture-status-details.md) | Optional | The details of the captured payment status. |

## Example

```ts
import {
  CaptureIncompleteReason,
  CaptureStatus,
  CaptureStatusWithDetails,
} from 'paypal-server-sdklib';

const captureStatusWithDetails: CaptureStatusWithDetails = {
  status: CaptureStatus.Completed,
  statusDetails: {
    reason: CaptureIncompleteReason.VerificationRequired,
  },
};
```

