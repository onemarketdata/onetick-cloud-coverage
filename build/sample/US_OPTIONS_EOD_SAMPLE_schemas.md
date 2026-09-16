# US Consolidated Options (OPRA) EOD - OPRA Daily Volume, OI and Greeks Sample Schemas

Daily data providing Option Greek calculations and Open Interest and Closing Trade.  Options on AAPL, NVDA, QQQ, SPY and TSLA are included in the sample covering January 2025.




## US_OPTIONS_EOD_SAMPLE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### US_OPTIONS_EOD_SAMPLE - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### US_OPTIONS_EOD_SAMPLE - DAY Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME      | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP        | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| VOLUME           | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| OPEN_INT         | double      | Open interest for futures / options                                                                                                                                                                                                    |
| UNDERLYING_PRICE | double      | Last price of the underlying instrument                                                                                                                                                                                                |
| BID_CLOSE        | double      | Closing bid price                                                                                                                                                                                                                      |
| ASK_CLOSE        | double      | Closing ask price                                                                                                                                                                                                                      |
| IMP_VOLATILITY   | double      | Implied volatility of an option                                                                                                                                                                                                        |
| DELTA            | double      | Option delta, i.e. the rate of change of an option’s price relative to its underlying                                                                                                                                                  |
| GAMMA            | double      | Option gamma, i.e. the rate of change of an option’s delta relative to the underlying asset price                                                                                                                                      |
| THETA            | double      | Option theta, i.e. the rate of time decay in the value of an option or its premium                                                                                                                                                     |
| VEGA             | double      | Option vega, i.e. the rate of change of an option’s price relative to the implied volatility of its underlying                                                                                                                         |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_OPTIONS_EOD_SAMPLE - STAT

Static data, e.g. ISIN, description, security type

#### US_OPTIONS_EOD_SAMPLE - STAT Table Schema

| Field             | Data Type   | Description                                                                                                                                                                                                                            |
|-------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME       | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP         | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| UNDERLYING_SYMBOL | string[8]   | Symbol of the underlying instrument                                                                                                                                                                                                    |
| EXPIRATION_DATE   | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                              |
| STRIKE_PRICE      | double      | Exercise price for options / warrants                                                                                                                                                                                                  |
| CALL_PUT_IND      | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                        |
| OMDSEQ            | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
