
# Customer Vault Payment Tokens Response

Collection of payment tokens saved for a given customer.

## Structure

`CustomerVaultPaymentTokensResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `totalItems` | `number \| undefined` | Optional | Total number of items.<br><br>**Constraints**: `>= 1`, `<= 50` |
| `totalPages` | `number \| undefined` | Optional | Total number of pages.<br><br>**Constraints**: `>= 1`, `<= 10` |
| `customer` | [`VaultResponseCustomer \| undefined`](../../doc/models/vault-response-customer.md) | Optional | This object defines a customer in your system. Use it to manage customer profiles, save payment methods and contact details. |
| `paymentTokens` | [`PaymentTokenResponse[] \| undefined`](../../doc/models/payment-token-response.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `64` |
| `links` | [`LinkDescription[] \| undefined`](../../doc/models/link-description.md) | Optional, Read-only | An array of related [HATEOAS links](/api/rest/responses/#hateoas).<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `32` |

## Example

```ts
import {
  CardBrand,
  CardType,
  CustomerVaultPaymentTokensResponse,
  FulfillmentType,
  LinkHttpMethod,
  PaypalPaymentTokenUsageType,
  UsagePattern,
} from 'paypal-server-sdklib';

const customerVaultPaymentTokensResponse: CustomerVaultPaymentTokensResponse = {
  totalItems: 50,
  totalPages: 10,
  customer: {
    id: 'id0',
    merchantCustomerId: 'merchant_customer_id2',
    links: [
      { 'key1': 'val1', 'key2': 'val2' },
      { 'key1': 'val1', 'key2': 'val2' }
    ],
  },
  paymentTokens: [
    {
      id: 'id4',
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
        },
        {
          href: 'href6',
          rel: 'rel0',
          method: LinkHttpMethod.Head,
        }
      ],
    },
    {
      id: 'id4',
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
        },
        {
          href: 'href6',
          rel: 'rel0',
          method: LinkHttpMethod.Head,
        }
      ],
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
    }
  ],
};
```

