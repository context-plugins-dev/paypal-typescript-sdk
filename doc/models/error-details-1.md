
# Error Details 1

The error details. Required for client-side `4XX` errors.

## Structure

`ErrorDetails1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `field` | `string \| undefined` | Optional | The field that caused the error. If this field is in the body, set this value to the field's JSON pointer value. Required for client-side errors. |
| `value` | `string \| undefined` | Optional | The value of the field that caused the error. |
| `location` | `string \| undefined` | Optional | The location of the field that caused the error. Value is `body`, `path`, or `query`.<br><br>**Default**: `'body'` |
| `issue` | `string` | Required | The unique, fine-grained application-level error code. |
| `links` | [`ErrorLinkDescription[] \| undefined`](../../doc/models/error-link-description.md) | Optional, Read-only | An array of request-related [HATEOAS links](/api/rest/responses/#hateoas-links) that are either relevant to the issue by providing additional information or offering potential resolutions.<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `4` |
| `description` | `string \| undefined` | Optional | The human-readable description for an issue. The description can change over the lifetime of an API, so clients must not depend on this value. |

## Example

```ts
import { ErrorDetails1, LinkHttpMethod } from 'paypal-server-sdklib';

const errorDetails1: ErrorDetails1 = {
  issue: 'issue6',
  field: 'field4',
  value: 'value2',
  location: 'body',
  links: [
    {
      href: 'href6',
      rel: 'rel0',
      method: LinkHttpMethod.Head,
    },
    {
      href: 'href6',
      rel: 'rel0',
      method: LinkHttpMethod.Head,
    }
  ],
  description: 'description0',
};
```

