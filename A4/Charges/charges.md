# Charges API Design Doc

## Decisions

| Ref  | Decision                                                       | Rationale                                                | P0 |
|:---:|:---------------------------------------------------------------|:-------------------------------------------------------- |    |
| 1   |  Pension references to be arrays per rolled-up annual amounts   | If figures are provided at detail level, then it would not be obvious if the annual allowance had been exceed or not  | |

\newpage 

## Issues

| Ref  | Description                                                  | Assigned To                             | Resolution                                                   |
| :---: | :----------------------------------------------------------- | :-------------------------------------- | :----------------------------------------------------------- |
|  1   |  What is the correct address format for the overseas pensions providers | Heidi                         |                                                              |

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

_/charges/pensions/{taxableEntityId}/{taxYear}_

#### Parameters

| Parameter       | Description                      | Example |
|:----------------|:---------------------------------|:--------|
| taxableEntityId | Unique customer identifier       | AB123456|
| taxYear         | The tax year to search within    | 2019-20 |


#### Request Payload Example

N/A

#### Response Payload Schema

### Annual Rolled Up Figures 

```json
{
  "pensionSavingsTaxCharges": {
    "pensionSchemeTaxReference": [
        "00123456RA",
        "00654321RA"
    ],
    "lumpSumBenefitTakenInExcessOfLifetimeAllowance": 123.00,
    "benefitInExcessOfLifetimeAllowance": 123.00,
    "lifetimeAllowanceTaxPaid": 123.00
    },
  "pensionSchemeOverseasTransfers": {
    "overseasSchemeProvider": [
       {
       "providerName": "Overseas Pensions Plc",
       "providerAddress": "111 Main Street, George Town, Grand Cayman", 
       "providerCountryCode": "CYM"
       }
     ],
    "transferCharge": 123.00,
    "transferChargeTaxPaid": 123.00
    },
   "pensionSchemeUnauthorisedPayments": {
   "pensionSchemeTaxReference": [
        "00123456RA",
        "00654321RA"
     ],
      "amountSurcharge":  123.00,
      "amountNoSurcharge": 123.00,
      "foreignTaxPaid": 123.00
   },
    "pensionContributions": {
    "pensionSchemeTaxReference": [
        "00123456RA",
        "00654321RA"
    ],
     "inExcessOfTheAnnualAllowance": 123.00,
     "annualAllowanceTaxPaid": 123.00
  },
  "overseasPensionContributions": {
    "overseasSchemeProvider": [
      {
       "providerName": "Overseas Pensions Plc",
       "providerAddress": "111 Main Street, George Town, Grand Cayman", 
       "providerCountryCode": "CYM"
      }
     ],
    "shortServiceRefund": 123.00,
    "shortServiceRefundTaxPaid": 123.00
   }
}
```
