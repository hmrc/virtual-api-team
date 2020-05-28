# A4 NIRS

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
| 1.0     | 28/05/2020 | Toby Porter |Initial version  |

  

\newpage



#### Response Payload Schema


#

(new endpoint for pensions)

#### URI

_//{taxableEntityId}/{taxYear}_

#### Parameters

| Parameter       | Description                      | Example |
|:----------------|:---------------------------------|:--------|
| taxableEntityId | Unique customer identifier       | AB123456|
| taxYear         | The tax year to search within    | 2019-20 |


```json
{
  "statePension": {
      "annualAmount": 123.00, //pre-pop
      "lumpSumAmount": 123.00,  //pre-pop 
      "lumpSumTaxPaid": 123.00  //pre-pop
  },
  "incapacityBenefit": {  //pre-pop P14?
      "amount": 123.00,
      "taxPaid": 123.00
  },
   "employmentSupportAllowance": {  //pre-pop P45? 
       "amount": 123.00
  },
   "jobseekersAllowance": {    //pre-pop?
        amount: 123.00
  },
    "bereavementAllowance": { 
        "amount":  123.00
  },
    "widowedParentsAllowance": {
      "amount":  123.00
  }
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
