# Lumpsums API Design Doc

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
  

}
```
