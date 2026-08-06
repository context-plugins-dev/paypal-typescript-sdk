
# Error Link Description

The error-related [HATEOAS link](/api/rest/responses/#hateoas-links) information. Identical to `link_description` except that `rel` is optional: the live API omits `rel` on the documentation link it returns with `RESOURCE_NOT_FOUND` errors, so a client that requires it cannot read the error at all.

## Structure

`ErrorLinkDescription`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `string` | Required | The complete target URL. To make the related call, combine the method with this [URI Template-formatted](https://tools.ietf.org/html/rfc6570) link. For pre-processing, include the `$`, `(`, and `)` characters. The `href` is the key HATEOAS component that links a completed call with a subsequent call. |
| `rel` | `string \| undefined` | Optional | The [link relation type](https://tools.ietf.org/html/rfc5988#section-4), which serves as an ID for a link that unambiguously describes the semantics of the link. See [Link Relations](https://www.iana.org/assignments/link-relations/link-relations.xhtml). |
| `method` | [`LinkHttpMethod \| undefined`](../../doc/models/link-http-method.md) | Optional | The HTTP method required to make the related call. |

## Example

```ts
import { ErrorLinkDescription, LinkHttpMethod } from 'paypal-server-sdklib';

const errorLinkDescription: ErrorLinkDescription = {
  href: 'href2',
  rel: 'rel6',
  method: LinkHttpMethod.Options,
};
```

