# A3 Markets - Matba Rofex Schemas

A3 Mercados is Argentina’s largest financial exchange platform, created from the merger of Matba Rofex and Mercado Abierto Electrónico (MAE).




## A3

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IDX - Index values
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### A3 - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### A3 - DAY Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME     | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP       | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| UPDATE_TYPE     | string[16]  | Type of update                                                                                                                                                                                                                         |
| OPEN            | double      | Open price for the current trading day                                                                                                                                                                                                 |
| HIGH            | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW             | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| CLOSE           | double      | Closing price                                                                                                                                                                                                                          |
| VOLUME          | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| SETTLE_PRICE    | double      | Settlement price                                                                                                                                                                                                                       |
| SETTLE_DATE     | string[8]   | Trading date to which the settlement price relates (YYYYMMDD)                                                                                                                                                                          |
| OPEN_INT        | double      | Open interest for futures / options                                                                                                                                                                                                    |
| OPEN_INT_DATE   | string[8]   | Trading date to which the open interest relates (YYYYMMDD)                                                                                                                                                                             |
| TRADE_COUNT     | double      | Number of trades on the current trading day                                                                                                                                                                                            |
| VWAP            | double      | Volume-weighted average price                                                                                                                                                                                                          |
| ON_BOOK_VOLUME  | double      | Total volume traded through the orderbook                                                                                                                                                                                              |
| OFF_BOOK_VOLUME | double      | Total volume traded off-book                                                                                                                                                                                                           |
| SPREAD_VOLUME   | double      | Total volume originating from spread executions  [i.e. strategy leg trades reported in each outright leg when two spread orders are matched]                                                                                           |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### A3 - IDX

Index values

#### A3 - IDX Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME   | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| PRICE       | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### A3 - LULD

Limit Up / Limit Down price levels

#### A3 - LULD Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME   | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| HIGH_LIMIT  | double      | Upper trading limit / circuit breaker level                                                                                                                                                                                            |
| LOW_LIMIT   | double      | Lower trading limit / circuit breaker level                                                                                                                                                                                            |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### A3 - MKT

Market phase / instrument status information

#### A3 - MKT Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME   | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| MKT_PHASE   | string[8]   | Indicates the instrument’s current market phase, as specified by the trading venue                                                                                                                                                     |
| OMD_STATUS  | string[1]   | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### A3 - QTE

Best bid / offer quotes

#### A3 - QTE Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME   | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| BID_PRICE   | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE    | long        | Best bid size                                                                                                                                                                                                                          |
| ASK_PRICE   | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE    | long        | Best ask size                                                                                                                                                                                                                          |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### A3 - STAT

Static data, e.g. ISIN, description, security type

#### A3 - STAT Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                                                                                   |
|---------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME         | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                                                |
| TIMESTAMP           | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                                       |
| NAME                | string[200] | Description of the instrument                                                                                                                                                                                                                                 |
| ISIN                | string[12]  | ISIN code                                                                                                                                                                                                                                                     |
| EXCH_SYMBOL         | string[40]  | Ticker symbol specified by the exchange                                                                                                                                                                                                                       |
| TRADING_CODE        | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                                                      |
| PRODUCT_CODE        | string[20]  | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD.                    |
| UNDERLYING_SYMBOL   | string[32]  | Symbol of the underlying instrument                                                                                                                                                                                                                           |
| UNDERLYING_ISIN     | string[12]  | ISIN of the underlying instrument                                                                                                                                                                                                                             |
| MIC                 | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                                              |
| OPERATING_MIC       | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                                            |
| SEC_TYPE            | string[20]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                                       |
| UNDERLYING_SEC_TYPE | string[20]  | Underlying asset class                                                                                                                                                                                                                                        |
| STRATEGY_TYPE       | string[40]  | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly                                                                                                                                                                                            |
| EXCH_SEC_TYPE       | string[20]  | Instrument type as specified by the exchange                                                                                                                                                                                                                  |
| EXCH_STRATEGY_TYPE  | string[20]  | Type of strategy / spread, as specified by the exchange                                                                                                                                                                                                       |
| CFI_CODE            | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                                                     |
| CURRENCY            | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                                               |
| EXPIRATION_DATE     | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                                                     |
| STRIKE_PRICE        | double      | Exercise price for options / warrants                                                                                                                                                                                                                         |
| CALL_PUT_IND        | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                                               |
| EXERCISE_TYPE       | string[1]   | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)                                                                                                                                                                                    |
| SETTLEMENT_TYPE     | string[1]   | Settlement method for a derivatives contract (C - Cash, P - Physical, E - Either cash or physical)                                                                                                                                                            |
| CONTRACT_SIZE       | double      | Indicates a derivative’s underlying quantity                                                                                                                                                                                                                  |
| LOT_SIZE            | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                                          |
| TICK_SIZE_TYPE      | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                                          |
| TICK_SIZE           | string[80]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                                                    |
| TICK_VALUE          | double      | Tick value, i.e. the profit / loss per contract resulting from a price movement equal to TICK_SIZE.                                                                                                                                                           |
| POINT_VALUE         | double      | Profit / loss per contract resulting from a 1 point price movement (e.g. if the price moves from 123.00 to 124.00).  Note that if an instrument trades in minor currency units such as USX (US cents), the point value will also be expressed in those units. |
| OMDSEQ              | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.                        |

### A3 - TRD

Trades

#### A3 - TRD Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME    | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP      | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME      | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| PRICE          | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE           | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| AGGRESSOR_SIDE | string[1]   | Indicates whether a trade resulted from an incoming buy or sell order.                                                                                                                                                                 |
| TRADE_TYPE     | string[4]   | Type of trade                                                                                                                                                                                                                          |
| TRADE_PERIOD   | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                       |
| BOOK_TYPE      | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                            |
| TRADE_ID       | string[20]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| DELETED_TIME   | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS    | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |



## A3_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### A3_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### A3_DAILY - DAY Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME     | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP       | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| UPDATE_TYPE     | string[16]  | Type of update                                                                                                                                                                                                                         |
| OPEN            | double      | Open price for the current trading day                                                                                                                                                                                                 |
| HIGH            | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW             | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| CLOSE           | double      | Closing price                                                                                                                                                                                                                          |
| VOLUME          | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| SETTLE_PRICE    | double      | Settlement price                                                                                                                                                                                                                       |
| SETTLE_DATE     | string[8]   | Trading date to which the settlement price relates (YYYYMMDD)                                                                                                                                                                          |
| OPEN_INT        | double      | Open interest for futures / options                                                                                                                                                                                                    |
| OPEN_INT_DATE   | string[8]   | Trading date to which the open interest relates (YYYYMMDD)                                                                                                                                                                             |
| TRADE_COUNT     | double      | Number of trades on the current trading day                                                                                                                                                                                            |
| VWAP            | double      | Volume-weighted average price                                                                                                                                                                                                          |
| ON_BOOK_VOLUME  | double      | Total volume traded through the orderbook                                                                                                                                                                                              |
| OFF_BOOK_VOLUME | double      | Total volume traded off-book                                                                                                                                                                                                           |
| SPREAD_VOLUME   | double      | Total volume originating from spread executions  [i.e. strategy leg trades reported in each outright leg when two spread orders are matched]                                                                                           |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### A3_DAILY - STAT

Static data, e.g. ISIN, description, security type

#### A3_DAILY - STAT Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                                                                                   |
|---------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME         | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                                                |
| TIMESTAMP           | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                                       |
| NAME                | string[200] | Description of the instrument                                                                                                                                                                                                                                 |
| ISIN                | string[12]  | ISIN code                                                                                                                                                                                                                                                     |
| EXCH_SYMBOL         | string[40]  | Ticker symbol specified by the exchange                                                                                                                                                                                                                       |
| TRADING_CODE        | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                                                      |
| PRODUCT_CODE        | string[20]  | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD.                    |
| UNDERLYING_SYMBOL   | string[32]  | Symbol of the underlying instrument                                                                                                                                                                                                                           |
| UNDERLYING_ISIN     | string[12]  | ISIN of the underlying instrument                                                                                                                                                                                                                             |
| MIC                 | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                                              |
| OPERATING_MIC       | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                                            |
| SEC_TYPE            | string[20]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                                       |
| UNDERLYING_SEC_TYPE | string[20]  | Underlying asset class                                                                                                                                                                                                                                        |
| STRATEGY_TYPE       | string[40]  | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly                                                                                                                                                                                            |
| EXCH_SEC_TYPE       | string[20]  | Instrument type as specified by the exchange                                                                                                                                                                                                                  |
| EXCH_STRATEGY_TYPE  | string[20]  | Type of strategy / spread, as specified by the exchange                                                                                                                                                                                                       |
| CFI_CODE            | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                                                     |
| CURRENCY            | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                                               |
| EXPIRATION_DATE     | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                                                     |
| STRIKE_PRICE        | double      | Exercise price for options / warrants                                                                                                                                                                                                                         |
| CALL_PUT_IND        | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                                               |
| EXERCISE_TYPE       | string[1]   | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)                                                                                                                                                                                    |
| SETTLEMENT_TYPE     | string[1]   | Settlement method for a derivatives contract (C - Cash, P - Physical, E - Either cash or physical)                                                                                                                                                            |
| CONTRACT_SIZE       | double      | Indicates a derivative’s underlying quantity                                                                                                                                                                                                                  |
| LOT_SIZE            | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                                          |
| TICK_SIZE_TYPE      | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                                          |
| TICK_SIZE           | string[80]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                                                    |
| TICK_VALUE          | double      | Tick value, i.e. the profit / loss per contract resulting from a price movement equal to TICK_SIZE.                                                                                                                                                           |
| POINT_VALUE         | double      | Profit / loss per contract resulting from a 1 point price movement (e.g. if the price moves from 123.00 to 124.00).  Note that if an instrument trades in minor currency units such as USX (US cents), the point value will also be expressed in those units. |
| OMDSEQ              | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.                        |
