# Taiwan Futures Exchange (TAIFEX) Schemas

The Taiwan Futures Exchange was established in 1998. It offers futures and options on major Taiwan stock indices, government bond futures, equity options and 30-day CP interest rate futures.




## TAIFEX

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### TAIFEX - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### TAIFEX - DAY Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOSE           | double      | Closing price                                                                                                                                                                                                                          |
| HIGH            | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW             | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OFF_BOOK_VOLUME | double      | Total volume traded off-book                                                                                                                                                                                                           |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| ON_BOOK_VOLUME  | double      | Total volume traded through the orderbook                                                                                                                                                                                              |
| OPEN            | double      | Open price for the current trading day                                                                                                                                                                                                 |
| OPEN_INT        | double      | Open interest for futures / options                                                                                                                                                                                                    |
| OPEN_INT_DATE   | string[8]   | Trading date to which the open interest relates (YYYYMMDD)                                                                                                                                                                             |
| SESSION         | string[8]   | Trading session to which the update relates, e.g. Day, Night, T, T+1                                                                                                                                                                   |
| SETTLE_DATE     | string[8]   | Trading date to which the settlement price relates (YYYYMMDD)                                                                                                                                                                          |
| SETTLE_PRICE    | double      | Settlement price                                                                                                                                                                                                                       |
| SPREAD_VOLUME   | double      | Total volume originating from spread executions  [i.e. strategy leg trades reported in each outright leg when two spread orders are matched]                                                                                           |
| TRADE_COUNT     | double      | Number of trades on the current trading day                                                                                                                                                                                            |
| UPDATE_TYPE     | string[16]  | Type of update                                                                                                                                                                                                                         |
| VOLUME          | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VWAP            | double      | Volume-weighted average price                                                                                                                                                                                                          |

### TAIFEX - IND

Indicative pricing, e.g. indicative auction prices and imbalance

#### TAIFEX - IND Table Schema

| Field        | Data Type   | Description                                                                                                                                                                                                                            |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AUCTION_TYPE | string[1]   | Type of auction from which an indicative auction price / auction imbalance originates.                                                                                                                                                 |
| EXCH_TIME    | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE        | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SESSION      | string[8]   | Trading session to which the update relates, e.g. Day, Night, T, T+1                                                                                                                                                                   |
| SIZE         | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |

### TAIFEX - LULD

Limit Up / Limit Down price levels

#### TAIFEX - LULD Table Schema

| Field        | Data Type   | Description                                                                                                                                                                                                                            |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME    | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| HIGH_LIMIT   | double      | Upper trading limit / circuit breaker level                                                                                                                                                                                            |
| HIGH_LIMIT_2 | double      | Second upper trading limit / circuit breaker level                                                                                                                                                                                     |
| HIGH_LIMIT_3 | double      | Third upper trading limit / circuit breaker level                                                                                                                                                                                      |
| LOW_LIMIT    | double      | Lower trading limit / circuit breaker level                                                                                                                                                                                            |
| LOW_LIMIT_2  | double      | Second lower trading limit / circuit breaker level                                                                                                                                                                                     |
| LOW_LIMIT_3  | double      | Third lower trading limit / circuit breaker level                                                                                                                                                                                      |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### TAIFEX - MKT

Market phase / instrument status information

#### TAIFEX - MKT Table Schema

| Field      | Data Type   | Description                                                                                                                                                                                                                            |
|------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EVENT_CODE | string[4]   | Event that triggered an instrument status update                                                                                                                                                                                       |
| EXCH_TIME  | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| MKT_PHASE  | string[8]   | Indicates the instrument’s current market phase, as specified by the trading venue                                                                                                                                                     |
| OMDSEQ     | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OMD_STATUS | string[1]   | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| SESSION    | string[8]   | Trading session to which the update relates, e.g. Day, Night, T, T+1                                                                                                                                                                   |

### TAIFEX - QTE

Best bid / offer quotes

#### TAIFEX - QTE Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_PRICE        | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE         | int         | Best ask size                                                                                                                                                                                                                          |
| ASK_SIZE_IMPLIED | int         | Volume of implied orders included in the best ask size (best ask size = implied ask size + outright ask size)                                                                                                                          |
| BID_PRICE        | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE         | int         | Best bid size                                                                                                                                                                                                                          |
| BID_SIZE_IMPLIED | int         | Volume of implied orders included in the best bid size (best bid size = implied bid size + outright bid size)                                                                                                                          |
| EXCH_TIME        | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| QUOTE_SESSION    | string[8]   | Trading session from which the quote originates, e.g. Day, Night                                                                                                                                                                       |

### TAIFEX - STAT

Static data, e.g. ISIN, description, security type

#### TAIFEX - STAT Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                                                                                   |
|---------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALL_PUT_IND        | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                                               |
| CFI_CODE            | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                                                     |
| CONTRACT_SIZE       | double      | Indicates a derivative’s underlying quantity                                                                                                                                                                                                                  |
| CURRENCY            | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                                               |
| EXCH_SEC_TYPE       | string[20]  | Instrument type as specified by the exchange                                                                                                                                                                                                                  |
| EXCH_STRATEGY_TYPE  | string[20]  | Type of strategy / spread, as specified by the exchange                                                                                                                                                                                                       |
| EXCH_SYMBOL         | string[40]  | Ticker symbol specified by the exchange                                                                                                                                                                                                                       |
| EXERCISE_TYPE       | string[1]   | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)                                                                                                                                                                                    |
| EXPIRATION_DATE     | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                                                     |
| ISIN                | string[12]  | ISIN code                                                                                                                                                                                                                                                     |
| MIC                 | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                                              |
| NAME                | string[200] | Description of the instrument                                                                                                                                                                                                                                 |
| OMDSEQ              | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.                        |
| OPERATING_MIC       | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                                            |
| POINT_VALUE         | double      | Profit / loss per contract resulting from a 1 point price movement (e.g. if the price moves from 123.00 to 124.00).  Note that if an instrument trades in minor currency units such as USX (US cents), the point value will also be expressed in those units. |
| PRODUCT_CODE        | string[20]  | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD.                    |
| SEC_TYPE            | string[20]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                                       |
| SETTLEMENT_TYPE     | string[1]   | Settlement method for a derivatives contract (C - Cash, P - Physical, E - Either cash or physical)                                                                                                                                                            |
| STRATEGY_TYPE       | string[40]  | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly                                                                                                                                                                                            |
| STRIKE_PRICE        | double      | Exercise price for options / warrants                                                                                                                                                                                                                         |
| TICK_SIZE           | string[80]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                                                    |
| TICK_SIZE_TYPE      | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                                          |
| TICK_VALUE          | double      | Tick value, i.e. the profit / loss per contract resulting from a price movement equal to TICK_SIZE.                                                                                                                                                           |
| TRADING_CODE        | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                                                      |
| UNDERLYING_ISIN     | string[12]  | ISIN of the underlying instrument                                                                                                                                                                                                                             |
| UNDERLYING_SEC_TYPE | string[20]  | Underlying asset class                                                                                                                                                                                                                                        |
| UNDERLYING_SYMBOL   | string[32]  | Symbol of the underlying instrument                                                                                                                                                                                                                           |

### TAIFEX - TRD

Trades

#### TAIFEX - TRD Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AGGRESSOR_SIDE | string[1]   | Indicates whether a trade resulted from an incoming buy or sell order.                                                                                                                                                                 |
| BOOK_TYPE      | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                            |
| DELETED_TIME   | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| EXCH_TIME      | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE          | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE           | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| TICK_STATUS    | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| TRADE_ID       | string[20]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| TRADE_PERIOD   | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                       |
| TRADE_SESSION  | string[8]   | Trading session from which a trade originates, e.g. Day, Night                                                                                                                                                                         |
| TRADE_TYPE     | string[4]   | Type of trade                                                                                                                                                                                                                          |



## TAIFEX_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### TAIFEX_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### TAIFEX_DAILY - DAY Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOSE           | double      | Closing price                                                                                                                                                                                                                          |
| HIGH            | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW             | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OFF_BOOK_VOLUME | double      | Total volume traded off-book                                                                                                                                                                                                           |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| ON_BOOK_VOLUME  | double      | Total volume traded through the orderbook                                                                                                                                                                                              |
| OPEN            | double      | Open price for the current trading day                                                                                                                                                                                                 |
| OPEN_INT        | double      | Open interest for futures / options                                                                                                                                                                                                    |
| OPEN_INT_DATE   | string[8]   | Trading date to which the open interest relates (YYYYMMDD)                                                                                                                                                                             |
| SESSION         | string[8]   | Trading session to which the update relates, e.g. Day, Night, T, T+1                                                                                                                                                                   |
| SETTLE_DATE     | string[8]   | Trading date to which the settlement price relates (YYYYMMDD)                                                                                                                                                                          |
| SETTLE_PRICE    | double      | Settlement price                                                                                                                                                                                                                       |
| SPREAD_VOLUME   | double      | Total volume originating from spread executions  [i.e. strategy leg trades reported in each outright leg when two spread orders are matched]                                                                                           |
| TRADE_COUNT     | double      | Number of trades on the current trading day                                                                                                                                                                                            |
| UPDATE_TYPE     | string[16]  | Type of update                                                                                                                                                                                                                         |
| VOLUME          | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VWAP            | double      | Volume-weighted average price                                                                                                                                                                                                          |

### TAIFEX_DAILY - STAT

Static data, e.g. ISIN, description, security type

#### TAIFEX_DAILY - STAT Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                                                                                   |
|---------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALL_PUT_IND        | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                                               |
| CFI_CODE            | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                                                     |
| CONTRACT_SIZE       | double      | Indicates a derivative’s underlying quantity                                                                                                                                                                                                                  |
| CURRENCY            | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                                               |
| EXCH_SEC_TYPE       | string[20]  | Instrument type as specified by the exchange                                                                                                                                                                                                                  |
| EXCH_STRATEGY_TYPE  | string[20]  | Type of strategy / spread, as specified by the exchange                                                                                                                                                                                                       |
| EXCH_SYMBOL         | string[40]  | Ticker symbol specified by the exchange                                                                                                                                                                                                                       |
| EXERCISE_TYPE       | string[1]   | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)                                                                                                                                                                                    |
| EXPIRATION_DATE     | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                                                     |
| ISIN                | string[12]  | ISIN code                                                                                                                                                                                                                                                     |
| MIC                 | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                                              |
| NAME                | string[200] | Description of the instrument                                                                                                                                                                                                                                 |
| OMDSEQ              | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.                        |
| OPERATING_MIC       | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                                            |
| POINT_VALUE         | double      | Profit / loss per contract resulting from a 1 point price movement (e.g. if the price moves from 123.00 to 124.00).  Note that if an instrument trades in minor currency units such as USX (US cents), the point value will also be expressed in those units. |
| PRODUCT_CODE        | string[20]  | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD.                    |
| SEC_TYPE            | string[20]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                                       |
| SETTLEMENT_TYPE     | string[1]   | Settlement method for a derivatives contract (C - Cash, P - Physical, E - Either cash or physical)                                                                                                                                                            |
| STRATEGY_TYPE       | string[40]  | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly                                                                                                                                                                                            |
| STRIKE_PRICE        | double      | Exercise price for options / warrants                                                                                                                                                                                                                         |
| TICK_SIZE           | string[80]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                                                    |
| TICK_SIZE_TYPE      | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                                          |
| TICK_VALUE          | double      | Tick value, i.e. the profit / loss per contract resulting from a price movement equal to TICK_SIZE.                                                                                                                                                           |
| TRADING_CODE        | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                                                      |
| UNDERLYING_ISIN     | string[12]  | ISIN of the underlying instrument                                                                                                                                                                                                                             |
| UNDERLYING_SEC_TYPE | string[20]  | Underlying asset class                                                                                                                                                                                                                                        |
| UNDERLYING_SYMBOL   | string[32]  | Symbol of the underlying instrument                                                                                                                                                                                                                           |
