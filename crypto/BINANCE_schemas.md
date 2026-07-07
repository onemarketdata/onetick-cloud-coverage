# Binance Schemas

Binance Holdings Ltd., branded Binance, is the largest cryptocurrency exchange in terms of daily trading volume of cryptocurrencies.




## BINANCE

Database includes the following tick types:

* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### BINANCE - QTE

Best bid / offer quotes

#### BINANCE - QTE Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_PRICE   | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE    | double      | Best ask size                                                                                                                                                                                                                          |
| BID_PRICE   | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE    | double      | Best bid size                                                                                                                                                                                                                          |
| EXCH_TIME   | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| QUOTE_VENUE | string[12]  | Venue (MIC) from which a quote originates                                                                                                                                                                                              |

### BINANCE - STAT

Static data, e.g. ISIN, description, security type

#### BINANCE - STAT Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CURRENCY        | string[12]  | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| EXCH_SYMBOL     | string[32]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| EXPIRATION_DATE | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                              |
| NAME            | string[100] | Description of the instrument                                                                                                                                                                                                          |
