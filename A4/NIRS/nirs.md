# Charges API Design Doc

## Decisions

| Ref  | Decision                                                     | Rationale                                                    |P0
| :---: | :----------------------------------------------------------- | :----------------------------------------------------------- |
|  1   |    |   |

\newpage 

## Issues

| Ref  | Description                                                  | Assigned To                             | Resolution                                                   |
| :---: | :----------------------------------------------------------- | :-------------------------------------- | :----------------------------------------------------------- |
|  1   |  |                          |                                                              |

\newpage

## Assumptions

| Ref  | Assumption                                                   | Clarification |
| ---- | ------------------------------------------------------------ | ------------- |
| 1    |  |               |

\newpage

 
## Change Log

| Version | Date | Author | Comments                                         |
| ------- | ---------- | --- | ------------------------------------------------ |
| 1.0     | 27/05/2020 | Toby Porter |Initial version  |

  

\newpage

## APIs

### Get Charges

#### Description

Get all charges that are associated with the supplied taxable entity id and tax year combination that have been active in the tax year.

#### ITSD Realisation

This API will be realised by ... 

#### URI

_/charges/other?/{taxableEntityId}/{taxYear}_
Tax-charges?

#### Parameters

| Parameter       | Description                      | Example |
|:----------------|:---------------------------------|:--------|
| taxableEntityId | Unique customer identifier       | AB123456|
| taxYear         | The tax year to search within    | 2019-20 |


#### Request Payload Example

N/A

#### Response Payload Schema

### Annual Rolled Up Figures 

Or add references for multiples?
```  "UkPensionSchemeTaxReferenceNumber"
     "foreignSchemeReference"
````

```json
{
  "pensionSavingsTaxCharges": {
    "pensionSchemeTaxReferenceNumber": [
        "ABC1234",
        "XYZ4321"
    ],
    "lumpSumBenefitTakenInExcessOfLifetimeAllowance": 123.00,
    "benefitInExcessOfLifetimeAllowance:" 123.00,
    "lifetimeAllowanceTaxPaid": 123.00
    },
  "pensionSchemeOverseasTransfers": {
    "overseasSchemeProvider": [
          {
           "providerName": "",
           "providerAddress": "",
           "providerCountryCode": ""
          }
     ],
    "transferCharge": 123.00,
    "transferChargeTaxPaid": 123.00
    },
   "pensionSchemeUnauthorisedPayments": {
      "pensionSchemeTaxReferenceNumber": [
        "ABC1234",
        "XYZ4321"
      ],
      "amountSurcharge":  123.00,
      "amountNoSurcharge": 123.00,
      "foreignTaxPaid": 123.00
   },
    "pensionContributions": {
        "pensionSchemeTaxReferenceNumber": [
            "ABC1234",
            "XYZ4321"
        ],
        "inExcessOfTheAnnualAllowance" = 123.00,
        "annualAllowanceTaxPaid" = 123.00
  },
  "overseasPensionContributions": {
    "overseasSchemeProvider": [
          {
           "providerName": "",
           "providerAddress": "",
           "providerCountryCode": ""
          }
     ],
    "shortServiceRefund": 123.00,
    "shortServiceRefundTaxPaid": 123.00
   }
}
```
