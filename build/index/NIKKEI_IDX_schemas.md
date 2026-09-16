# Nikkei Indices Schemas

Nikkei Indices are a series of stock market indices for the Tokyo Stock Exchange, including the Nikkei 225, which tracks the top 225 blue-chip companies in Japan.




## NIKKEI_IDX

Database includes the following tick types:

* IDX - Index values
* STAT - Static data, e.g. ISIN, description, security type



### NIKKEI_IDX - IDX

Index values

#### NIKKEI_IDX - IDX Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| PRICE       | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### NIKKEI_IDX - STAT

Static data, e.g. ISIN, description, security type

#### NIKKEI_IDX - STAT Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| NAME        | string[100] | Description of the instrument                                                                                                                                                                                                          |
| EXCH_SYMBOL | string[10]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| SEC_TYPE    | string[10]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| BBG_TICKER  | string[35]  | Bloomberg ticker symbol                                                                                                                                                                                                                |
| FIGI        | string[12]  | Financial Instrument Global Identifier, identifying an individual instrument traded on a specific venue                                                                                                                                |
| CURRENCY    | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
