# Global Daily Interest Rates Schemas

Daily fixings of key global interest rate benchmarks, with history from January 2008, including US SOFR, EFFR and BGCR, euro EURIBOR, UK SONIA and Japan TONA. Use it to build discount curves, compare funding rates across currencies, or study the transition from LIBOR to risk-free rates.




## RATES

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### RATES - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### RATES - DAY Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| CLOSE       | double      | Closing price                                                                                                                                                                                                                          |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### RATES - STAT

Static data, e.g. ISIN, description, security type

#### RATES - STAT Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| NAME        | string[64]  | Description of the instrument                                                                                                                                                                                                          |
| OID         | string[14]  | OneMarketData ID                                                                                                                                                                                                                       |
| SEC_TYPE    | string[30]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
