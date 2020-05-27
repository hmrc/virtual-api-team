# A4 Reliefs API Design Doc

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



#### Response Payload Schema


#reliefs 

(new endpoint for pensions)

#### URI

_/reliefs/pensions/{taxableEntityId}/{taxYear}_

#### Parameters

| Parameter       | Description                      | Example |
|:----------------|:---------------------------------|:--------|
| taxableEntityId | Unique customer identifier       | AB123456|
| taxYear         | The tax year to search within    | 2019-20 |


```json
{
  "pensionRelief": {
    "regularPensionContributions:": 123.00,
    "oneOffPensionContributionsPaid": 123.00,
    "retirementAnnuityPayments": 123.00,
    "paymentToEmployersSchemeNoTaxRelief": 123.00,
    "overseasPensionSchemeContributions": 123.00
    }
}
```
// no reliefClaimed?
//     "overseasPensionSchemeContributions": 123.00,  # already in income/pensions?  
