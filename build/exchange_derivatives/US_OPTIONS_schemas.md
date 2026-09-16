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
| SYMBOL_NAME  | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP    | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| BID_PRICE    | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_PRICE    | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE     | int         | Best bid size                                                                                                                                                                                                                          |
| ASK_SIZE     | int         | Best ask size                                                                                                                                                                                                                          |
| BID_EXCHANGE | string[1]   | Exchange that set the best bid                                                                                                                                                                                                         |
| ASK_EXCHANGE | string[1]   | Exchange that set the best ask                                                                                                                                                                                                         |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_OPTIONS - QTE

Best bid / offer quotes

#### US_OPTIONS - QTE Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| BID_PRICE   | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_PRICE   | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE    | int         | Best bid size                                                                                                                                                                                                                          |
| ASK_SIZE    | int         | Best ask size                                                                                                                                                                                                                          |
| EXCHANGE    | string[1]   | Exchange from which the update originates                                                                                                                                                                                              |
| QUOTE_COND  | string[1]   | Indicates any special conditions applicable to a quote                                                                                                                                                                                 |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_OPTIONS - STAT

Static data, e.g. ISIN, description, security type

#### US_OPTIONS - STAT Table Schema

| Field             | Data Type   | Description                                                                                                                                                                                                                            |
|-------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME       | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP         | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| STRIKE_PRICE      | double      | Exercise price for options / warrants                                                                                                                                                                                                  |
| UNDERLYING_SYMBOL | string[6]   | Symbol of the underlying instrument                                                                                                                                                                                                    |
| ACTIV_SYMBOL      | string[20]  | Ticker symbol used by Activ Financial                                                                                                                                                                                                  |
| EXPIRATION_DATE   | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                              |
| CALL_PUT_IND      | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                        |
| OMDSEQ            | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_OPTIONS - TRD

Trades

#### US_OPTIONS - TRD Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME    | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP      | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| PRICE          | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE           | int         | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| EXCHANGE       | string[1]   | Exchange from which the update originates                                                                                                                                                                                              |
| TRADE_TYPE     | string[1]   | Type of trade                                                                                                                                                                                                                          |
| TRADE_TYPE_EXT | string[4]   | Extended trade type code                                                                                                                                                                                                               |
| TRADE_ID       | string[20]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| DELETED_TIME   | nsectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS    | byte        | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
