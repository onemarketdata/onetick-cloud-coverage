# US Consolidated Options (OPRA) Schemas

This refers to consolidated data from all US options exchanges disseminated through the Options Price Reporting Authority (OPRA).




## US_OPTIONS

Database includes the following tick types:

* NBBO - National Best Bid / Offer quotes
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### US_OPTIONS - NBBO

National Best Bid / Offer quotes

#### US_OPTIONS - NBBO Table Schema

| Field        | Data Type   | Description                                                                                                                                                                                                                            |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_EXCHANGE | string[1]   | Exchange that set the best ask                                                                                                                                                                                                         |
| ASK_PRICE    | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE     | int         | Best ask size                                                                                                                                                                                                                          |
| BID_EXCHANGE | string[1]   | Exchange that set the best bid                                                                                                                                                                                                         |
| BID_PRICE    | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE     | int         | Best bid size                                                                                                                                                                                                                          |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_OPTIONS - QTE

Best bid / offer quotes

#### US_OPTIONS - QTE Table Schema

| Field      | Data Type   | Description                                                                                                                                                                                                                            |
|------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_PRICE  | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE   | int         | Best ask size                                                                                                                                                                                                                          |
| BID_PRICE  | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE   | int         | Best bid size                                                                                                                                                                                                                          |
| EXCHANGE   | string[1]   | Exchange from which the update originates                                                                                                                                                                                              |
| OMDSEQ     | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| QUOTE_COND | string[1]   | Indicates any special conditions applicable to a quote                                                                                                                                                                                 |

### US_OPTIONS - STAT

Static data, e.g. ISIN, description, security type

#### US_OPTIONS - STAT Table Schema

| Field             | Data Type   | Description                                                                                                                                                                                                                            |
|-------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTIV_SYMBOL      | string[20]  | Ticker symbol used by Activ Financial                                                                                                                                                                                                  |
| CALL_PUT_IND      | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                        |
| EXPIRATION_DATE   | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                              |
