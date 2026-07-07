# Instrument Security Master Schemas

Instrument Description Reference and Shares Outstanding




## OQD_SEC

Database includes the following tick types:

* DES - Static data, e.g. ISIN, description, security type
* SHO - Shares Outstanding



### OQD_SEC - DES

Static data, e.g. ISIN, description, security type

#### OQD_SEC - DES Table Schema

| Field        | Data Type   | Description                                                                                                                                                                                                                            |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALENDAR     | string[30]  | Associated Calendar                                                                                                                                                                                                                    |
| COUNTRY      | string[3]   | ISO Country Code                                                                                                                                                                                                                       |
| DELETED_TIME | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| END_DATE     | msectime    | Calendar Event End Date, or Last Valid Date                                                                                                                                                                                            |
| EXCH         | string[10]  | Exchange from which the update originates (Country Code + [MIC or PRIM for Primary, or COMP for Composite])                                                                                                                            |
| IDSYM        | string[10]  | Standard Identifier (CUSIP for US/Canada, otherwise SEDOL)                                                                                                                                                                             |
| ISSUE_CLASS  | string[30]  | Broadest Security Classification                                                                                                                                                                                                       |
| ISSUE_DESC   | string[30]  | Security Description                                                                                                                                                                                                                   |
| ISSUE_STATUS | string[30]  | Security Status                                                                                                                                                                                                                        |
| ISSUE_TYPE   | string[30]  | Detailed Security Type Code                                                                                                                                                                                                            |
| NAME         | string[30]  | Description of the instrument                                                                                                                                                                                                          |
