
# Error Error 1 Error

The error details.

## Structure

`ErrorError1Error`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | The human-readable, unique name of the error. |
| `message` | `string` | Required | The message that describes the error. |
| `debugId` | `string` | Required | The PayPal internal ID. Used for correlation purposes. |
| `details` | [`ErrorDetails1[] \| undefined`](../../doc/models/error-details-1.md) | Optional | An array of additional details about the error. |
| `links` | [`ErrorLinkDescription[] \| undefined`](../../doc/models/error-link-description.md) | Optional, Read-only | An array of request-related [HATEOAS links](/api/rest/responses/#hateoas-links). |

## Example

```ts
try {
  // make the API call
} catch (error) {
  if (error instanceof ErrorError1Error) {
    console.log(error.result);
  }
}
```

