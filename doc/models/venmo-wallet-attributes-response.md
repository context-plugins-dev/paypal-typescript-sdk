
# Venmo Wallet Attributes Response

Additional attributes associated with the use of a Venmo Wallet.

## Structure

`VenmoWalletAttributesResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vault` | [`VenmoVaultResponse \| undefined`](../../doc/models/venmo-vault-response.md) | Optional | The details about a saved venmo payment source. |

## Example

```ts
import {
  LinkHttpMethod,
  PhoneType,
  VenmoVaultResponseStatus,
  VenmoWalletAttributesResponse,
} from 'paypal-server-sdklib';

const venmoWalletAttributesResponse: VenmoWalletAttributesResponse = {
  vault: {
    id: 'id6',
    status: VenmoVaultResponseStatus.Approved,
    links: [
      {
        href: 'href6',
        rel: 'rel0',
        method: LinkHttpMethod.Head,
      }
    ],
    customer: {
      id: 'id0',
      emailAddress: 'email_address2',
      phone: {
        phoneNumber: {
          nationalNumber: 'national_number6',
        },
        phoneType: PhoneType.Other,
      },
      name: {
        givenName: 'given_name2',
        surname: 'surname8',
      },
    },
  },
};
```

