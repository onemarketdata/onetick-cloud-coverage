# OTC Markets (US OTC Quotes) Schemas

OTC Markets operates trading platforms for over 10,000 OTC securities in the US public and private markets.




## OTCM

Database includes the following tick types:

* BBO - Combined best bid / offer quotes calculated across multiple sources
* OTCM_INSIDE_QTE - OTCM Inside Quote
* STAT - Static data, e.g. ISIN, description, security type



### OTCM - BBO

Combined best bid / offer quotes calculated across multiple sources

#### OTCM - BBO Table Schema

| Field     | Data Type   | Description                                                                                                                                                                                                                            |
|-----------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_MMID  | string[30]  | Ask Market Maker ID                                                                                                                                                                                                                    |
| ASK_PRICE | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE  | long        | Best ask size                                                                                                                                                                                                                          |
| BID_MMID  | string[30]  | Bid Market Maker ID                                                                                                                                                                                                                    |
| BID_PRICE | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE  | long        | Best bid size                                                                                                                                                                                                                          |
| OMDSEQ    | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### OTCM - OTCM_INSIDE_QTE

OTCM Inside Quote

#### OTCM - OTCM_INSIDE_QTE Table Schema

| Field     | Data Type   | Description                                                                                                                                                                                                                            |
|-----------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_PRICE | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE  | long        | Best ask size                                                                                                                                                                                                                          |
| BID_PRICE | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE  | long        | Best bid size                                                                                                                                                                                                                          |
| EXCH_TIME | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ    | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### OTCM - STAT

Static data, e.g. ISIN, description, security type

#### OTCM - STAT Table Schema

| Field   | Data Type   | Description                                                                                                                                                                                                                            |
|---------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CUSIP   | string[9]   | CUSIP code                                                                                                                                                                                                                             |
| NAME    | string[50]  | Description of the instrument                                                                                                                                                                                                          |
| OMDSEQ  | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |



## OTCM_BARS

Database includes the following tick types:

* QTE_1M - 1-minute quote bars



### OTCM_BARS - QTE_1M

1-minute quote bars

#### OTCM_BARS - QTE_1M Table Schema

| Field                 | Data Type   | Description                                                                                                                                                                                                                                       |
|-----------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_PRICE_AT_HIGH_BID | double      | Ask price of the quote that set HIGH_BID.  If there are multiple bid quotes at HIGH_BID, the first one is used.                                                                                                                                   |
| ASK_SIZE_AT_HIGH_BID  | long        | Ask size of the quote that set HIGH_BID.  If there are multiple bid quotes at HIGH_BID, the first one is used.                                                                                                                                    |
| BID_PRICE_AT_LOW_ASK  | double      | Bid price of the quote that set LOW_ASK. If there are multiple ask quotes at LOW_ASK, the first one is used.                                                                                                                                      |
| BID_SIZE_LOW_ASK      | long        | Bid size of the quote that set LOW_ASK.  If there are multiple ask quotes at LOW_ASK, the first one is used.                                                                                                                                      |
| CLOUD_DB              | string[32]  | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.                                                                                        |
| FIRST_ASK_PRICE       | double      | Price of the first best ask update in the current bar interval                                                                                                                                                                                    |
| FIRST_ASK_SIZE        | long        | Size of the first best ask update in the current bar interval                                                                                                                                                                                     |
| FIRST_ASK_TIME        | nsectime    | Time of the first best ask update in the current bar interval                                                                                                                                                                                     |
| FIRST_BID_PRICE       | double      | Price of the first best bid update in the current bar interval                                                                                                                                                                                    |
| FIRST_BID_SIZE        | long        | Size of the first best bid update in the current bar interval                                                                                                                                                                                     |
| FIRST_BID_TIME        | nsectime    | Time of the first best bid update in the current bar interval                                                                                                                                                                                     |
| HIGH_BID              | double      | Highest bid price in the current bar interval                                                                                                                                                                                                     |
| HIGH_BID_SIZE         | long        | Size of the bid quote that set HIGH_BID.  If there are multiple quotes at that price, the first one is used.                                                                                                                                      |
