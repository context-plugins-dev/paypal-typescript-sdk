
# Error 1

The error details.

## Structure

`Error1`

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
import { Error1, LinkHttpMethod } from 'paypal-server-sdklib';

const error1: Error1 = {
  name: 'name8',
  message: 'message8',
  debugId: 'debug_id4',
  details: [
    {
      issue: 'issue6',
      field: 'field4',
      value: 'value2',
      location: 'location4',
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
    },
    {
      issue: 'issue6',
      field: 'field4',
      value: 'value2',
      location: 'location4',
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
    },
    {
      issue: 'issue6',
      field: 'field4',
      value: 'value2',
      location: 'location4',
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
    }
  ],
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
    },
    {
      href: 'href6',
      rel: 'rel0',
      method: LinkHttpMethod.Head,
    }
  ],
};
```

