
# Subscriber

The subscriber response information.

## Structure

`Subscriber`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | [`Name \| undefined`](../../doc/models/name.md) | Optional | The name of the party. |
| `shippingAddress` | [`ShippingDetails \| undefined`](../../doc/models/shipping-details.md) | Optional | The shipping details. |
| `paymentSource` | [`SubscriptionPaymentSourceResponse \| undefined`](../../doc/models/subscription-payment-source-response.md) | Optional | The payment source used to fund the payment. |

## Example

```ts
import {
  FulfillmentType,
  ShippingType,
  Subscriber,
} from 'paypal-server-sdklib';

const subscriber: Subscriber = {
  name: {
    givenName: 'given_name2',
    surname: 'surname8',
  },
  shippingAddress: {
    name: {
      fullName: 'full_name6',
    },
    emailAddress: 'email_address8',
    phoneNumber: {
      countryCode: 'country_code2',
      nationalNumber: 'national_number6',
    },
    type: FulfillmentType.PickupInStore,
    options: [
      {
        id: 'id2',
        label: 'label2',
        selected: false,
        type: ShippingType.Shipping,
        amount: {
          currencyCode: 'currency_code6',
          value: 'value0',
        },
      }
    ],
  },
  paymentSource: {
    card: {
      name: 'name6',
      billingAddress: {
        countryCode: 'country_code8',
        addressLine1: 'address_line_12',
        addressLine2: 'address_line_28',
        adminArea2: 'admin_area_28',
        adminArea1: 'admin_area_14',
        postalCode: 'postal_code0',
      },
      expiry: 'expiry4',
      currencyCode: 'currency_code2',
    },
  },
};
```

