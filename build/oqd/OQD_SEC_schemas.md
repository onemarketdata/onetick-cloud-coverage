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
| SYMBOL_NAME  | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP    | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| OID          | string[14]  | OneMarketData ID                                                                                                                                                                                                                       |
| END_DATE     | msectime    | Calendar Event End Date, or Last Valid Date                                                                                                                                                                                            |
| COUNTRY      | string[3]   | ISO Country Code                                                                                                                                                                                                                       |
| EXCH         | string[10]  | Exchange from which the update originates (Country Code + [MIC or PRIM for Primary, or COMP for Composite])                                                                                                                            |
| NAME         | string[30]  | Description of the instrument                                                                                                                                                                                                          |
| ISSUE_DESC   | string[30]  | Security Description                                                                                                                                                                                                                   |
| ISSUE_CLASS  | string[30]  | Broadest Security Classification                                                                                                                                                                                                       |
| ISSUE_TYPE   | string[30]  | Detailed Security Type Code                                                                                                                                                                                                            |
| ISSUE_STATUS | string[30]  | Security Status                                                                                                                                                                                                                        |
| SIC_CODE     | string[4]   | Standard Industrial Classfication Code                                                                                                                                                                                                 |
| IDSYM        | string[10]  | Standard Identifier (CUSIP for US/Canada, otherwise SEDOL)                                                                                                                                                                             |
| TICKER       | string[30]  | Ticker symbol, as specified by the data source                                                                                                                                                                                         |
| CALENDAR     | string[30]  | Associated Calendar                                                                                                                                                                                                                    |
| DELETED_TIME | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS  | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### OQD_SEC - SHO

Shares Outstanding

#### OQD_SEC - SHO Table Schema

| Field        | Data Type   | Description                                                                                                                                                                                                                            |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME  | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP    | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| OID          | string[14]  | OneMarketData ID                                                                                                                                                                                                                       |
| END_DATE     | msectime    | Calendar Event End Date, or Last Valid Date                                                                                                                                                                                            |
| REPORT_MONTH | string[6]   | The reporting month for shares outstanding                                                                                                                                                                                             |
| SHARES       | double      | Shares / quantity outstanding                                                                                                                                                                                                          |
| DELETED_TIME | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS  | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
