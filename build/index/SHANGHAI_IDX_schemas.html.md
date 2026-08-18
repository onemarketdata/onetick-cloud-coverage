# Shanghai Stock Exchange - Indices Schemas

The Shanghai Stock Exchange provides indices tracking the performance of Chinese equities, including the SSE Composite Index and sector-specific indices.




## SHANGHAI_IDX

Database includes the following tick types:

* IDX - Index values
* STAT - Static data, e.g. ISIN, description, security type



### SHANGHAI_IDX - IDX

Index values

#### SHANGHAI_IDX - IDX Table Schema

| Field     | Data Type   | Description                                                                                                                                                                                                                            |
|-----------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ    | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE     | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| VOLUME    | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |

### SHANGHAI_IDX - STAT

Static data, e.g. ISIN, description, security type

#### SHANGHAI_IDX - STAT Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CURRENCY      | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| EXCH_SYMBOL   | string[25]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| ISIN          | string[12]  | ISIN code                                                                                                                                                                                                                              |
| MIC           | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| NAME          | string[120] | Description of the instrument                                                                                                                                                                                                          |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPERATING_MIC | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| SEC_TYPE      | string[20]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
