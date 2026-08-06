
# Payment Token Response

Full representation of a saved payment token.

## Structure

`PaymentTokenResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string \| undefined` | Optional | The PayPal-generated ID for the vaulted payment source. This ID should be stored on the merchant's server so the saved payment source can be used for future transactions.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255`, *Pattern*: `^[0-9a-zA-Z_-]+$` |
| `customer` | [`CustomerResponse \| undefined`](../../doc/models/customer-response.md) | Optional | Customer in merchant's or partner's system of records. |
| `paymentSource` | [`PaymentTokenResponsePaymentSource \| undefined`](../../doc/models/payment-token-response-payment-source.md) | Optional | The vaulted payment method details. |
| `links` | [`LinkDescription[] \| undefined`](../../doc/models/link-description.md) | Optional, Read-only | An array of related [HATEOAS links](/api/rest/responses/#hateoas).<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `32` |

## Example

```ts
import {
  CardBrand,
  CardType,
  FulfillmentType,
  LinkHttpMethod,
  PaymentTokenResponse,
  PaypalPaymentTokenUsageType,
  UsagePattern,
} from 'paypal-server-sdklib';

const paymentTokenResponse: PaymentTokenResponse = {
  id: 'id8',
  customer: {
    id: 'id0',
    merchantCustomerId: 'merchant_customer_id2',
  },
  paymentSource: {
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
  },
  links: [
    {
      href: 'href6',
      rel: 'rel0',
      method: LinkHttpMethod.Head,
    }
  ],
};
```

