# FINRA TRACE - Corporates, Agencies, MBS, ABS, CMO Schemas

The Trade Reporting and Compliance Engine (TRACE) is the FINRA-developed vehicle that facilitates the mandatory reporting of over-the-counter transactions in eligible fixed income securities. All broker-dealers who are FINRA member firms have an obligation to report transactions in TRACE-eligible securities under an SEC-approved set of rules.




## TRACE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### TRACE - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### TRACE - DAY Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOSE       | double      | Closing price                                                                                                                                                                                                                          |
| CLOSE_YIELD | double      | Yield corresponding to the closing price                                                                                                                                                                                               |
| HIGH        | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| HIGH_YIELD  | double      | Yield corresponding to the high price                                                                                                                                                                                                  |
| LOW         | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| LOW_YIELD   | double      | Yield corresponding to the low price                                                                                                                                                                                                   |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN        | double      | Open price for the current trading day                                                                                                                                                                                                 |
| OPEN_YIELD  | double      | Yield corresponding to the opening price                                                                                                                                                                                               |
| TRADE_COUNT | long        | Number of trades on the current trading day                                                                                                                                                                                            |
| VOLUME      | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VWAP        | double      | Volume-weighted average price                                                                                                                                                                                                          |

### TRACE - STAT

Static data, e.g. ISIN, description, security type

#### TRACE - STAT Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CURRENCY      | string[12]  | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| EXCH_SYMBOL   | string[32]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| FIGI          | string[12]  | Financial Instrument Global Identifier, identifying an individual instrument traded on a specific venue                                                                                                                                |
| MIC           | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| NAME          | string[100] | Description of the instrument                                                                                                                                                                                                          |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPERATING_MIC | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| SEC_SUBTYPE   | string[40]  | Security subtype                                                                                                                                                                                                                       |
| SEC_TYPE      | string[40]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| WHEN_ISSUED   | string[1]   | Indicates that the instrument is trading on a When Issued basis (Y - Yes,  - No / unspecified)                                                                                                                                         |

### TRACE - TRD

Trades

#### TRACE - TRD Table Schema

| Field                 | Data Type   | Description                                                                                                                                                                                                                            |
