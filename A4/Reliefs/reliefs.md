# A4 Pension Reliefs 

## Decisions

| Ref  | Decision                                                     | Rationale                                                    |P0
| :---: | :----------------------------------------------------------- | :----------------------------------------------------------- |
|  1   |    |   |

\newpage 

## Issues

| Ref  | Description                                                  | Assigned To                             | Resolution                                                   |
| :---: | :----------------------------------------------------------- | :-------------------------------------- | :----------------------------------------------------------- |
|  1   |  |  Which items should be pre-populated (and from what source)?              |  Heidi                                                            |

\newpage

## Assumptions

| Ref  | Assumption                                                   | Clarification |
| ---- | ------------------------------------------------------------ | ------------- |
| 1    |  |               |

\newpage

 
## Change Log

| Version | Date | Author | Comments                                         |
| ------- | ---------- | --- | ------------------------------------------------ |
| 1.0     | 28/05/2020 | Toby Porter |Initial version  |

  

\newpage



#### Response Payload Schema

#### URI

(new endpoint for pension reliefs)

_/reliefs/pensions/{taxableEntityId}/{taxYear}_

#### Parameters

| Parameter       | Description                      | Example |
|:----------------|:---------------------------------|:--------|
| taxableEntityId | Unique customer identifier       | AB123456|
| taxYear         | The tax year to search within    | 2019-20 |


```json
{
  "statePension": {
      "annualAmount": 123.00,
      "lumpSumAmount": 123.00, 
      "lumpSumTaxPaid": 123.00
  },
  "incapacityBenefit": {  
      "amount": 123.00,
      "taxPaid": 123.00
  },
   "employmentSupportAllowance": {  
       "amount": 123.00
  },
   "jobseekersAllowance": {
        "amount": 123.00
  },
    "bereavementAllowance": { 
        "amount":  123.00
  },
    "widowedParentsAllowance": {
      "amount":  123.00
  },
    "industrialDeathBenefit": {
      "amount":  123.00
  },
    "carersAllowance": {
      "amount":  123.00
  },
    "otherStatutoryBenefits": {
      "amount": 123.00
  }          
}
```
