
# Setup Token Response Payment Source

The setup payment method details.

## Structure

`SetupTokenResponsePaymentSource`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `card` | [`SetupTokenResponseCard \| undefined`](../../doc/models/setup-token-response-card.md) | Optional | - |
| `paypal` | [`PaypalPaymentToken \| undefined`](../../doc/models/paypal-payment-token.md) | Optional, Read-only | Full representation of a PayPal Payment Token. |
| `venmo` | [`VenmoPaymentToken \| undefined`](../../doc/models/venmo-payment-token.md) | Optional, Read-only | Full representation of a Venmo Payment Token. |

## Example

```ts
import {
  CardBrand,
  FulfillmentType,
  PaypalPaymentTokenUsageType,
  SetupTokenResponsePaymentSource,
  UsagePattern,
} from 'paypal-server-sdklib';

const setupTokenResponsePaymentSource: SetupTokenResponsePaymentSource = {
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
};
```

