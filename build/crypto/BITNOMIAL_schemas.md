# Bitnomial Schemas

Bitnomial offers leveraged spot, perpetuals, futures, options, and prediction markets on a single unified US regulated exchange and clearinghouse




## BITNOMIAL

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* PRL - Market depth data, aggregated by price point (MBP)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### BITNOMIAL - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### BITNOMIAL - DAY Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BUY_VOLUME  | double      | Traded volume originating from incoming buy orders.  Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| CLOSE       | double      | Closing price                                                                                                                                                                                                                          |
| HIGH        | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW         | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN        | double      | Open price for the current trading day                                                                                                                                                                                                 |
| SELL_VOLUME | double      | Traded volume originating from incoming sell orders. Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| TRADE_COUNT | double      | Number of trades on the current trading day                                                                                                                                                                                            |
| UPDATE_TYPE | string[16]  | Type of update                                                                                                                                                                                                                         |
| VOLUME      | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VWAP        | double      | Volume-weighted average price                                                                                                                                                                                                          |

### BITNOMIAL - PRL

Market depth data, aggregated by price point (MBP)

#### BITNOMIAL - PRL Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BUY_SELL_FLAG | int         | Orderbook side (0 - Buy, 1 - Sell)                                                                                                                                                                                                     |
| DELETED_TIME  | nsectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| EXCH_TIME     | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE         | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| RECORD_TYPE   | string[1]   | Type of depth update.                                                                                                                                                                                                                  |
| SIZE          | double      | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| TICK_STATUS   | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |

### BITNOMIAL - QTE

Best bid / offer quotes

#### BITNOMIAL - QTE Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_PRICE   | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE    | double      | Best ask size                                                                                                                                                                                                                          |
| BID_PRICE   | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE    | double      | Best bid size                                                                                                                                                                                                                          |
| EXCH_TIME   | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| QUOTE_VENUE | string[12]  | Venue (MIC) from which a quote originates                                                                                                                                                                                              |

### BITNOMIAL - STAT

Static data, e.g. ISIN, description, security type

#### BITNOMIAL - STAT Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALL_PUT_IND    | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                        |
| CURRENCY        | string[12]  | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| EXCH_SYMBOL     | string[32]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| EXERCISE_TYPE   | string[1]   | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)                                                                                                                                                             |
| EXPIRATION_DATE | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                              |
| NAME            | string[100] | Description of the instrument                                                                                                                                                                                                          |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| SEC_SUBTYPE     | string[40]  | Security subtype                                                                                                                                                                                                                       |
| SEC_TYPE        | string[40]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| STRIKE_PRICE    | double      | Exercise price for options / warrants                                                                                                                                                                                                  |

### BITNOMIAL - TRD

Trades

#### BITNOMIAL - TRD Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AGGRESSOR_SIDE | string[1]   | Indicates whether a trade resulted from an incoming buy or sell order.                                                                                                                                                                 |
| BOOK_TYPE      | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                            |
| BUYER          | string[48]  | ID of the market participant on the buy side of a trade                                                                                                                                                                                |
| DELETED_TIME   | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| EXCH_TIME      | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE          | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SELLER         | string[48]  | ID of the market participant on the sell side of a trade                                                                                                                                                                               |
| SIZE           | double      | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| TICK_STATUS    | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| TRADE_ID       | string[40]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| TRADE_PERIOD   | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                       |
| TRADE_TYPE     | string[4]   | Type of trade                                                                                                                                                                                                                          |
| TRADE_VENUE    | string[12]  | Identifies the venue where a trade was executed.   Typically a MIC, with the special values XOFF for off-exchange and SINT for Systematic Internaliser trades.                                                                         |



## BITNOMIAL_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### BITNOMIAL_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### BITNOMIAL_DAILY - DAY Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BUY_VOLUME  | double      | Traded volume originating from incoming buy orders.  Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| CLOSE       | double      | Closing price                                                                                                                                                                                                                          |
| HIGH        | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW         | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN        | double      | Open price for the current trading day                                                                                                                                                                                                 |
| SELL_VOLUME | double      | Traded volume originating from incoming sell orders. Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| TRADE_COUNT | double      | Number of trades on the current trading day                                                                                                                                                                                            |
| UPDATE_TYPE | string[16]  | Type of update                                                                                                                                                                                                                         |
| VOLUME      | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VWAP        | double      | Volume-weighted average price                                                                                                                                                                                                          |

### BITNOMIAL_DAILY - STAT

Static data, e.g. ISIN, description, security type

#### BITNOMIAL_DAILY - STAT Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CURRENCY        | string[12]  | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| EXCH_SYMBOL     | string[32]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| EXPIRATION_DATE | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                              |
| NAME            | string[100] | Description of the instrument                                                                                                                                                                                                          |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| SEC_SUBTYPE     | string[40]  | Security subtype                                                                                                                                                                                                                       |
| SEC_TYPE        | string[40]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
