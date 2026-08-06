
# Subscriber Request

The subscriber request information .

## Structure

`SubscriberRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | [`Name \| undefined`](../../doc/models/name.md) | Optional | The name of the party. |
| `phone` | [`PhoneWithType \| undefined`](../../doc/models/phone-with-type.md) | Optional | The phone information. |
| `shippingAddress` | [`ShippingDetails \| undefined`](../../doc/models/shipping-details.md) | Optional | The shipping details. |
| `paymentSource` | [`SubscriptionPaymentSource \| undefined`](../../doc/models/subscription-payment-source.md) | Optional | The payment source definition. To be eligible to create subscription using debit or credit card, you will need to sign up here (https://www.paypal.com/bizsignup/entry/product/ppcp). Please note, its available only for non-3DS cards and for merchants in US and AU regions. |

## Example

```ts
import {
  CardType,
  FulfillmentType,
  PhoneType,
  ShippingType,
  SubscriberRequest,
} from 'paypal-server-sdklib';

const subscriberRequest: SubscriberRequest = {
  name: {
    givenName: 'given_name2',
    surname: 'surname8',
  },
  phone: {
    phoneNumber: {
      nationalNumber: 'national_number6',
    },
    phoneType: PhoneType.Other,
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
      number: 'number6',
      expiry: 'expiry4',
      securityCode: 'security_code8',
      type: CardType.Unknown,
    },
  },
};
```

