
# Payment Token Response Payment Source

The vaulted payment method details.

## Structure

`PaymentTokenResponsePaymentSource`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `card` | [`CardPaymentTokenEntity \| undefined`](../../doc/models/card-payment-token-entity.md) | Optional | Full representation of a Card Payment Token including network token. |
| `paypal` | [`PaypalPaymentToken \| undefined`](../../doc/models/paypal-payment-token.md) | Optional, Read-only | Full representation of a PayPal Payment Token. |
| `venmo` | [`VenmoPaymentToken \| undefined`](../../doc/models/venmo-payment-token.md) | Optional, Read-only | Full representation of a Venmo Payment Token. |
| `applePay` | [`ApplePayPaymentToken \| undefined`](../../doc/models/apple-pay-payment-token.md) | Optional | A resource representing a response for Apple Pay. |

## Example

```ts
import {
  CardBrand,
  CardType,
  FulfillmentType,
  PaymentTokenResponsePaymentSource,
  PaypalPaymentTokenUsageType,
  UsagePattern,
} from 'paypal-server-sdklib';

const paymentTokenResponsePaymentSource: PaymentTokenResponsePaymentSource = {
  card: {
    name: 'name6',
    lastDigits: 'last_digits0',
    brand: CardBrand.CbNationale,
    expiry: 'expiry4',
    billingAddress: {
      countryCode: 'country_code8',
      addressLine1: 'address_line_12',
      addressLine2: 'address_line_28',
      adminArea2: 'admin_area_28',
      adminArea1: 'admin_area_14',
      postalCode: 'postal_code0',
    },
  },
  paypal: {
    description: 'description2',
    usagePattern: UsagePattern.ThresholdPrepaid,
    shipping: {
      name: {
        fullName: 'full_name6',
      },
      emailAddress: 'email_address2',
      phoneNumber: {
        countryCode: 'country_code2',
        nationalNumber: 'national_number6',
      },
      type: FulfillmentType.Shipping,
      address: {
        countryCode: 'country_code6',
        addressLine1: 'address_line_16',
        addressLine2: 'address_line_26',
        adminArea2: 'admin_area_20',
        adminArea1: 'admin_area_12',
        postalCode: 'postal_code8',
      },
    },
    permitMultiplePaymentTokens: false,
    usageType: PaypalPaymentTokenUsageType.Merchant,
  },
  venmo: {
    description: 'description6',
    usagePattern: UsagePattern.UnscheduledPrepaid,
    shipping: {
      name: {
        fullName: 'full_name6',
      },
      emailAddress: 'email_address2',
      phoneNumber: {
        countryCode: 'country_code2',
        nationalNumber: 'national_number6',
      },
      type: FulfillmentType.Shipping,
      address: {
        countryCode: 'country_code6',
        addressLine1: 'address_line_16',
        addressLine2: 'address_line_26',
        adminArea2: 'admin_area_20',
        adminArea1: 'admin_area_12',
        postalCode: 'postal_code8',
      },
    },
    permitMultiplePaymentTokens: false,
    usageType: PaypalPaymentTokenUsageType.Merchant,
  },
  applePay: {
    card: {
      name: 'name6',
      lastDigits: 'last_digits0',
      type: CardType.Unknown,
      brand: CardBrand.CbNationale,
      billingAddress: {
        countryCode: 'country_code8',
        addressLine1: 'address_line_12',
        addressLine2: 'address_line_28',
        adminArea2: 'admin_area_28',
        adminArea1: 'admin_area_14',
        postalCode: 'postal_code0',
      },
    },
  },
};
```

