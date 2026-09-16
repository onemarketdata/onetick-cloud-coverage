# COMEX Futures Schemas

COMEX is a division of the CME Group, offering trading in metal futures and options.




## COMEX

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* FIXING - Fixing prices
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* RFQ - Data related to a Request for Quote
* TRD - Trades
* STAT - Static data, e.g. ISIN, description, security type



### COMEX - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### COMEX - DAY Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME   | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP     | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| UPDATE_TYPE   | string[16]  | Type of update                                                                                                                                                                                                                         |
| OPEN          | double      | Open price for the current trading day                                                                                                                                                                                                 |
| HIGH          | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW           | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| CLOSE         | double      | Closing price                                                                                                                                                                                                                          |
| VOLUME        | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| ELEC_VOLUME   | long        | Total volume traded electronically                                                                                                                                                                                                     |
| BLOCK_VOLUME  | long        | Total volume of block trades executed on the current day                                                                                                                                                                               |
| SETTLE_PRICE  | double      | Settlement price                                                                                                                                                                                                                       |
| SETTLE_DATE   | string[8]   | Trading date to which the settlement price relates (YYYYMMDD)                                                                                                                                                                          |
| OPEN_INT      | double      | Open interest for futures / options                                                                                                                                                                                                    |
| OPEN_INT_DATE | string[8]   | Trading date to which the open interest relates (YYYYMMDD)                                                                                                                                                                             |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### COMEX - IND

Indicative pricing, e.g. indicative auction prices and imbalance

#### COMEX - IND Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| PRICE       | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE        | int         | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### COMEX - FIXING

Fixing prices

#### COMEX - FIXING Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| PRICE       | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### COMEX - LULD

Limit Up / Limit Down price levels

#### COMEX - LULD Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                                                            |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME        | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP          | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| HIGH_LIMIT         | double      | Upper trading limit / circuit breaker level                                                                                                                                                                                            |
| LOW_LIMIT          | double      | Lower trading limit / circuit breaker level                                                                                                                                                                                            |
| DYNAMIC_PRICE_BAND | double      | Maximum price movement from one trade to the next                                                                                                                                                                                      |
| OMDSEQ             | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### COMEX - MKT

Market phase / instrument status information

#### COMEX - MKT Table Schema

| Field        | Data Type   | Description                                                                                                                                                                                                                            |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME  | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP    | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| TRADING_DATE | string[8]   | Identifies the current business date (YYYYMMDD). May be different to the calendar date, e.g. for T+1 trading sessions.                                                                                                                 |
| MKT_PHASE    | string[6]   | Indicates the instrument’s current market phase, as specified by the trading venue                                                                                                                                                     |
| REASON_CODE  | string[4]   | Reason for an instrument status update                                                                                                                                                                                                 |
| EVENT_CODE   | string[4]   | Event that triggered an instrument status update                                                                                                                                                                                       |
| OMD_STATUS   | string[1]   | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### COMEX - PRL_FULL

Full orderbook data, showing updates to each individual order (MBO)

#### COMEX - PRL_FULL Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME   | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP     | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| UPDATE_TYPE   | string[1]   | Type of update                                                                                                                                                                                                                         |
| ORDER_ID      | string[20]  | Order identifier, uniquely identifying an order at any given point in time.   Uniqueness depends on the exchange - e.g. may be globally unique, or unique per trading day, or per instrument per trading day.                          |
| BUY_SELL_FLAG | int         | Orderbook side (0 - Buy, 1 - Sell)                                                                                                                                                                                                     |
| ORDER_TYPE    | string[1]   | Type of order.                                                                                                                                                                                                                         |
| PRICE         | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE          | int         | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| TIME_PRIORITY | long        | Time priority of an order in the order queue.  If two standard orders on the same side have the same price, the one with the lower value of TIME_PRIORITY will be executed first.                                                      |
| TRADE_ID      | string[16]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| FILL_SIZE     | int         | Size filled in an order execution event                                                                                                                                                                                                |
| OLD_PRICE     | double      | Previous price of an order                                                                                                                                                                                                             |
| OLD_SIZE      | int         | Previous size of an order                                                                                                                                                                                                              |
| RECORD_TYPE   | string[1]   | Type of depth update.                                                                                                                                                                                                                  |
| DELETED_TIME  | nsectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS   | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### COMEX - QTE

Best bid / offer quotes

#### COMEX - QTE Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME      | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP        | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| BID_PRICE        | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE         | int         | Best bid size                                                                                                                                                                                                                          |
| BID_NUM_ORDERS   | short       | Number of orders at the best bid price                                                                                                                                                                                                 |
| BID_SIZE_IMPLIED | int         | Volume of implied orders included in the best bid size (best bid size = implied bid size + outright bid size)                                                                                                                          |
| ASK_PRICE        | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE         | int         | Best ask size                                                                                                                                                                                                                          |
| ASK_NUM_ORDERS   | short       | Number of orders at the best ask price                                                                                                                                                                                                 |
| ASK_SIZE_IMPLIED | int         | Volume of implied orders included in the best ask size (best ask size = implied ask size + outright ask size)                                                                                                                          |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### COMEX - RFQ

Data related to a Request for Quote

#### COMEX - RFQ Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| RFQ_ID      | string[25]  | Uniquely identifies a Request for Quote                                                                                                                                                                                                |
| SIZE        | int         | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| RFQ_SIDE    | string[6]   | Side to which a Request for Quote applies                                                                                                                                                                                              |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### COMEX - TRD

Trades

#### COMEX - TRD Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME    | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP      | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME      | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| PRICE          | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE           | int         | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| AGGRESSOR_SIDE | string[1]   | Indicates whether a trade resulted from an incoming buy or sell order.                                                                                                                                                                 |
| TRADE_TYPE     | string[4]   | Type of trade                                                                                                                                                                                                                          |
| TRADE_PERIOD   | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                       |
| BOOK_TYPE      | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                            |
| TRADE_ID       | string[16]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| BUY_ORDER_ID   | string[20]  | ID of the buy order involved in a trade                                                                                                                                                                                                |
| SELL_ORDER_ID  | string[20]  | ID of the sell order involved in a trade                                                                                                                                                                                               |
| DELETED_TIME   | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS    | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### COMEX - STAT

Static data, e.g. ISIN, description, security type

#### COMEX - STAT Table Schema

| Field                   | Data Type   | Description                                                                                                                                                                                                                                |
|-------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME             | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                             |
| TIMESTAMP               | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                    |
| NAME                    | string[250] | Description of the instrument                                                                                                                                                                                                              |
| EXCH_SYMBOL             | string[30]  | Ticker symbol specified by the exchange                                                                                                                                                                                                    |
| UNDERLYING_SYMBOL       | string[40]  | Symbol of the underlying instrument                                                                                                                                                                                                        |
| UNDERLYING_EXCH_SYMBOL  | string[30]  | Ticker symbol of the underlying instrument, as specified by the exchange                                                                                                                                                                   |
| TRADING_CODE            | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                                   |
| PRODUCT_CODE            | string[20]  | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD. |
| TRADING_GROUP           | string[8]   | Trading group to which the instrument belongs. Instruments in the same trading group will have the same trading schedule, order matching algorithm, etc.                                                                                   |
| MIC                     | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                           |
| OPERATING_MIC           | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                         |
| SEC_TYPE                | string[30]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                    |
| UNDERLYING_SEC_TYPE     | string[20]  | Underlying asset class                                                                                                                                                                                                                     |
| STRATEGY_TYPE           | string[40]  | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly                                                                                                                                                                         |
| EXCH_SEC_TYPE           | string[30]  | Instrument type as specified by the exchange                                                                                                                                                                                               |
| EXCH_STRATEGY_TYPE      | string[30]  | Type of strategy / spread, as specified by the exchange                                                                                                                                                                                    |
| CFI_CODE                | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                                  |
| CURRENCY                | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                            |
| EXPIRATION_DATE         | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                                  |
| LAST_TRADING_TIME       | nsectime    | Time when the instrument finishes trading on the final trading day                                                                                                                                                                         |
| CONTRACT_SIZE           | double      | Indicates a derivative’s underlying quantity                                                                                                                                                                                               |
| CONTRACT_UNITS          | string[25]  | Units in which CONTRACT_SIZE is expressed                                                                                                                                                                                                  |
| STRIKE_PRICE            | double      | Exercise price for options / warrants                                                                                                                                                                                                      |
| CALL_PUT_IND            | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                            |
| EXERCISE_TYPE           | string[1]   | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)                                                                                                                                                                 |
| TICK_SIZE_TYPE          | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                       |
| TICK_SIZE               | string[80]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                                 |
| TICK_VALUE              | double      | Tick value, i.e. the profit / loss per contract resulting from a price movement equal to TICK_SIZE.                                                                                                                                        |
| FRACTIONAL_PRICE_FORMAT | string[10]  | Indicates the denominator of the fractional portion of the price, for instruments whose price is conventionally displayed in fractional format. If the display price has a fraction and a subfraction, both are provided, separated by -.  |
| STRATEGY_LEG_COUNT      | int         | Number of legs in a strategy (spread)                                                                                                                                                                                                      |
| STRATEGY_LEGS           | string[600] | Comma-separated list of symbols for the legs of a futures / options spread                                                                                                                                                                 |
| STRATEGY_RATIO          | string[100] | Comma-separated list of ratios for the legs of a futures / options spread. Ratios are listed in the same order as the symbols in STRATEGY_LEGS.                                                                                            |
| HEDGE_LEG_COUNT         | int         | Number of legs in the hedge portion of a spread (e.g. for option spreads hedged against underlying futures)                                                                                                                                |
| HEDGE_LEGS              | string[70]  | Comma-separated list of symbols for the hedge portion of a spread                                                                                                                                                                          |
| HEDGE_RATIO             | string[40]  | Comma-separated list of ratios for the hedge portion of a futures / options spread. Ratios are listed in the same order as the symbols in HEDGE_LEGS.                                                                                      |
| HEDGE_PRICE             | string[70]  | Comma-separated list of prices for the hedge portion of a futures / options spread. Prices are listed in the same order as the symbols in HEDGE_LEGS.                                                                                      |
| MIN_TRADE_SIZE          | int         | Minimum tradable size                                                                                                                                                                                                                      |
| MAX_TRADE_SIZE          | int         | Maximum tradable size                                                                                                                                                                                                                      |
| ORDER_EXEC_ALGO         | string[30]  | Algorithm used by the matching engine to prioritise and match orders                                                                                                                                                                       |
| IMPLIED_PRICING         | string[1]   | Indicates whether a derivative instrument supports implied pricing (Y - Yes, N - No)                                                                                                                                                       |
| EXCH_PRICE_MULTIPLIER   | double      | Multiplier used to convert from the exchange’s internal price value used in the matching engine to the monetary price seen in market data                                                                                                  |
| EXCH_STRIKE_MULTIPLIER  | double      | Multiplier used to convert from the exchange’s internal strike price to the monetary strike price seen in market data                                                                                                                      |
| EXPIRY_CODE             | string[12]  | Code identifying a specific futures / options expiry within the exchange system                                                                                                                                                            |
| EXPIRY_WEEK             | string[2]   | Identifies the week of the month in which weekly futures / options expire                                                                                                                                                                  |
| OMDSEQ                  | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.     |



## COMEX_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* LAT_1M - 1-minute Latency bars for real time delivered data
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars



### COMEX_BARS - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### COMEX_BARS - DAY Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME   | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP     | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| UPDATE_TYPE   | string[16]  | Type of update                                                                                                                                                                                                                         |
| OPEN          | double      | Open price for the current trading day                                                                                                                                                                                                 |
| HIGH          | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW           | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| CLOSE         | double      | Closing price                                                                                                                                                                                                                          |
| VOLUME        | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| ELEC_VOLUME   | long        | Total volume traded electronically                                                                                                                                                                                                     |
| BLOCK_VOLUME  | long        | Total volume of block trades executed on the current day                                                                                                                                                                               |
| SETTLE_PRICE  | double      | Settlement price                                                                                                                                                                                                                       |
| SETTLE_DATE   | string[8]   | Trading date to which the settlement price relates (YYYYMMDD)                                                                                                                                                                          |
| OPEN_INT      | double      | Open interest for futures / options                                                                                                                                                                                                    |
| OPEN_INT_DATE | string[8]   | Trading date to which the open interest relates (YYYYMMDD)                                                                                                                                                                             |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### COMEX_BARS - MKT

Market phase / instrument status information

#### COMEX_BARS - MKT Table Schema

| Field        | Data Type   | Description                                                                                                                                                                                                                            |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME  | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP    | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| OMD_STATUS   | string[64]  | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| TRADING_DATE | string[8]   | Identifies the current business date (YYYYMMDD). May be different to the calendar date, e.g. for T+1 trading sessions.                                                                                                                 |
| MKT_PHASE    | string[6]   | Indicates the instrument’s current market phase, as specified by the trading venue                                                                                                                                                     |
| REASON_CODE  | string[4]   | Reason for an instrument status update                                                                                                                                                                                                 |
| EVENT_CODE   | string[4]   | Event that triggered an instrument status update                                                                                                                                                                                       |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### COMEX_BARS - LAT_1M

1-minute Latency bars for real time delivered data

#### COMEX_BARS - LAT_1M Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME            | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP              | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| AVG_LATENCY_COLLECTION | double      | Average Latency of Real Time Collection.  Difference between Exchange timestamp and collection timestamp.                                                                                                                              |
| MAX_LATENCY_COLLECTION | double      | Maximum Latency of Real Time Collection.  Difference between Exchange timestamp and collection timestamp.                                                                                                                              |
| AVG_LATENCY_LOAD       | double      | Average Latency of Real Time Loading.  Difference between the collection timestamp and availability within the Memory Database.                                                                                                        |
| MAX_LATENCY_LOAD       | double      | Maximum Latency of Real Time Loading.  Difference between the collection timestamp and availability within the Memory Database.                                                                                                        |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### COMEX_BARS - QTE_1M

1-minute quote bars

#### COMEX_BARS - QTE_1M Table Schema

| Field                 | Data Type   | Description                                                                                                                                                                                                                                       |
|-----------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME           | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                                    |
| TIMESTAMP             | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                           |
| FIRST_BID_TIME        | nsectime    | Time of the first best bid update in the current bar interval                                                                                                                                                                                     |
| FIRST_BID_PRICE       | double      | Price of the first best bid update in the current bar interval                                                                                                                                                                                    |
| FIRST_BID_SIZE        | long        | Size of the first best bid update in the current bar interval                                                                                                                                                                                     |
| FIRST_ASK_TIME        | nsectime    | Time of the first best ask update in the current bar interval                                                                                                                                                                                     |
| FIRST_ASK_PRICE       | double      | Price of the first best ask update in the current bar interval                                                                                                                                                                                    |
| FIRST_ASK_SIZE        | long        | Size of the first best ask update in the current bar interval                                                                                                                                                                                     |
| HIGH_BID_TIME         | nsectime    | Time of the bid quote that set HIGH_BID.  If there are multiple quotes at that price, the first one is used.                                                                                                                                      |
| HIGH_BID              | double      | Highest bid price in the current bar interval                                                                                                                                                                                                     |
| HIGH_BID_SIZE         | long        | Size of the bid quote that set HIGH_BID.  If there are multiple quotes at that price, the first one is used.                                                                                                                                      |
| ASK_PRICE_AT_HIGH_BID | double      | Ask price of the quote that set HIGH_BID.  If there are multiple bid quotes at HIGH_BID, the first one is used.                                                                                                                                   |
| ASK_SIZE_AT_HIGH_BID  | long        | Ask size of the quote that set HIGH_BID.  If there are multiple bid quotes at HIGH_BID, the first one is used.                                                                                                                                    |
| LOW_ASK_TIME          | nsectime    | Time of the bid quote that set LOW_ASK.  If there are multiple quotes at that price, the first one is used.                                                                                                                                       |
| LOW_ASK               | double      | Lowest ask price in the current bar interval                                                                                                                                                                                                      |
| LOW_ASK_SIZE          | long        | Size of the ask quote that set LOW_ASK.  If there are multiple quotes at that price, the first one is used.                                                                                                                                       |
| BID_PRICE_AT_LOW_ASK  | double      | Bid price of the quote that set LOW_ASK. If there are multiple ask quotes at LOW_ASK, the first one is used.                                                                                                                                      |
| BID_SIZE_LOW_ASK      | long        | Bid size of the quote that set LOW_ASK.  If there are multiple ask quotes at LOW_ASK, the first one is used.                                                                                                                                      |
| LAST_BID_TIME         | nsectime    | Time of the last best bid update in the current bar interval                                                                                                                                                                                      |
| LAST_BID_PRICE        | double      | Price of the last best bid update in the current bar interval                                                                                                                                                                                     |
| LAST_BID_SIZE         | long        | Size of the last best bid update in the current bar interval                                                                                                                                                                                      |
| LAST_ASK_TIME         | nsectime    | Time of the last best ask update in the current bar interval                                                                                                                                                                                      |
| LAST_ASK_PRICE        | double      | Price of the last best ask update in the current bar interval                                                                                                                                                                                     |
| LAST_ASK_SIZE         | long        | Size of the last best ask update in the current bar interval                                                                                                                                                                                      |
| MID_TWAP              | double      | Time-weighted average of the midpoint of the best bid/ask over the current bar interval.  [Note: One-sided or empty quotes are excluded from the calculation]                                                                                     |
| MID_MEDIAN            | double      | Median of the midpoint of the best bid/ask quotes over the current bar interval. [Note: One-sided or empty quotes are excluded from the calculation]                                                                                              |
| MID_LAST              | double      | Midpoint of the last best bid/ask in the current bar interval. [Note: One-sided or empty quotes are excluded from the calculation]                                                                                                                |
| SPREAD_MIN            | double      | Narrowest bid/ask spread, i.e. the lowest value of (best ask price - best bid price) over the current bar interval.   [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation] |
| SPREAD_MAX            | double      | Widest bid/ask spread, i.e. the highest value of (best ask price - best bid price) over the current bar interval.   [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation]   |
| SPREAD_TWAP           | double      | Time-weighted average of (best ask price - best bid price) over the current bar interval.  [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation]                            |
| SPREAD_MEDIAN         | double      | Median value of (best ask price - best bid price) over the current bar interval.   [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation]                                    |
| SPREAD_LAST           | double      | Last value of (best ask price - best bid price) over the current bar interval.  [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation]                                       |
| QUOTE_CURRENCY        | string[3]   | Currency in which a quote price is expressed.                                                                                                                                                                                                     |
| QUOTE_TICK_COUNT      | long        | Number of BBO quotes in the current bar interval                                                                                                                                                                                                  |
| CLOUD_DB              | string[32]  | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.                                                                                        |
| OMDSEQ                | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.            |

### COMEX_BARS - TRD_1D

Daily trade bars

#### COMEX_BARS - TRD_1D Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME      | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP        | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| FIRST_TIME       | nsectime    | Timestamp of the first eligible trade in the current bar interval                                                                                                                                                                      |
| FIRST            | double      | Price of the first eligible trade in the current bar interval                                                                                                                                                                          |
| FIRST_SIZE       | long        | Size of the first eligible trade in the current bar interval                                                                                                                                                                           |
| HIGH_TIME        | nsectime    | Timestamp of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                               |
| HIGH             | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| HIGH_SIZE        | long        | Size of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                    |
| LOW_TIME         | nsectime    | Timestamp of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                |
| LOW              | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| LOW_SIZE         | long        | Size of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                     |
| LAST_TIME        | nsectime    | Timestamp of the last eligible trade in the current bar interval                                                                                                                                                                       |
| LAST             | double      | Price of the last eligible trade in the current bar interval                                                                                                                                                                           |
| LAST_SIZE        | long        | Size of the last eligible trade in the current bar interval                                                                                                                                                                            |
| VWAP             | double      | Volume-weighted average price                                                                                                                                                                                                          |
| TWAP             | double      | TIme-weighted average price                                                                                                                                                                                                            |
| VOLUME           | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| BUY_VOLUME       | long        | Traded volume originating from incoming buy orders.  Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| SELL_VOLUME      | long        | Traded volume originating from incoming sell orders. Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| TRADE_CURRENCY   | string[3]   | Currency in which a trade was executed.                                                                                                                                                                                                |
| TRADE_TICK_COUNT | long        | Number of eligible trades in the current bar interval                                                                                                                                                                                  |
| CLOUD_DB         | string[32]  | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.                                                                             |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### COMEX_BARS - TRD_1M

1-minute trade bars

#### COMEX_BARS - TRD_1M Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME      | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP        | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| FIRST_TIME       | nsectime    | Timestamp of the first eligible trade in the current bar interval                                                                                                                                                                      |
| FIRST            | double      | Price of the first eligible trade in the current bar interval                                                                                                                                                                          |
| FIRST_SIZE       | long        | Size of the first eligible trade in the current bar interval                                                                                                                                                                           |
| HIGH_TIME        | nsectime    | Timestamp of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                               |
| HIGH             | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| HIGH_SIZE        | long        | Size of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                    |
| LOW_TIME         | nsectime    | Timestamp of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                |
| LOW              | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| LOW_SIZE         | long        | Size of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                     |
| LAST_TIME        | nsectime    | Timestamp of the last eligible trade in the current bar interval                                                                                                                                                                       |
| LAST             | double      | Price of the last eligible trade in the current bar interval                                                                                                                                                                           |
| LAST_SIZE        | long        | Size of the last eligible trade in the current bar interval                                                                                                                                                                            |
| VWAP             | double      | Volume-weighted average price                                                                                                                                                                                                          |
| TWAP             | double      | TIme-weighted average price                                                                                                                                                                                                            |
| VOLUME           | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| BUY_VOLUME       | long        | Traded volume originating from incoming buy orders.  Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| SELL_VOLUME      | long        | Traded volume originating from incoming sell orders. Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| TRADE_CURRENCY   | string[3]   | Currency in which a trade was executed.                                                                                                                                                                                                |
| TRADE_TICK_COUNT | long        | Number of eligible trades in the current bar interval                                                                                                                                                                                  |
| CLOUD_DB         | string[32]  | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.                                                                             |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### COMEX_BARS - VWAP_1H

1-hour VWAP bars

#### COMEX_BARS - VWAP_1H Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| VWAP        | double      | Volume-weighted average price                                                                                                                                                                                                          |
| TWAP        | double      | TIme-weighted average price                                                                                                                                                                                                            |
| VOLUME      | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| CURRENCY    | string[64]  | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| CLOUD_DB    | string[32]  | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.                                                                             |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |



## COMEX_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### COMEX_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### COMEX_DAILY - DAY Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME   | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP     | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| UPDATE_TYPE   | string[16]  | Type of update                                                                                                                                                                                                                         |
| OPEN          | double      | Open price for the current trading day                                                                                                                                                                                                 |
| HIGH          | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW           | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| CLOSE         | double      | Closing price                                                                                                                                                                                                                          |
| VOLUME        | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| ELEC_VOLUME   | long        | Total volume traded electronically                                                                                                                                                                                                     |
| BLOCK_VOLUME  | long        | Total volume of block trades executed on the current day                                                                                                                                                                               |
| SETTLE_PRICE  | double      | Settlement price                                                                                                                                                                                                                       |
| SETTLE_DATE   | string[8]   | Trading date to which the settlement price relates (YYYYMMDD)                                                                                                                                                                          |
| OPEN_INT      | double      | Open interest for futures / options                                                                                                                                                                                                    |
| OPEN_INT_DATE | string[8]   | Trading date to which the open interest relates (YYYYMMDD)                                                                                                                                                                             |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### COMEX_DAILY - STAT

Static data, e.g. ISIN, description, security type

#### COMEX_DAILY - STAT Table Schema

| Field                   | Data Type   | Description                                                                                                                                                                                                                                |
|-------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME             | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                             |
| TIMESTAMP               | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                    |
| NAME                    | string[250] | Description of the instrument                                                                                                                                                                                                              |
| EXCH_SYMBOL             | string[30]  | Ticker symbol specified by the exchange                                                                                                                                                                                                    |
| UNDERLYING_SYMBOL       | string[40]  | Symbol of the underlying instrument                                                                                                                                                                                                        |
| UNDERLYING_EXCH_SYMBOL  | string[30]  | Ticker symbol of the underlying instrument, as specified by the exchange                                                                                                                                                                   |
| TRADING_CODE            | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                                   |
| PRODUCT_CODE            | string[20]  | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD. |
| TRADING_GROUP           | string[8]   | Trading group to which the instrument belongs. Instruments in the same trading group will have the same trading schedule, order matching algorithm, etc.                                                                                   |
| MIC                     | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                           |
| OPERATING_MIC           | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                         |
| SEC_TYPE                | string[30]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                    |
| UNDERLYING_SEC_TYPE     | string[20]  | Underlying asset class                                                                                                                                                                                                                     |
| STRATEGY_TYPE           | string[40]  | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly                                                                                                                                                                         |
| EXCH_SEC_TYPE           | string[30]  | Instrument type as specified by the exchange                                                                                                                                                                                               |
| EXCH_STRATEGY_TYPE      | string[30]  | Type of strategy / spread, as specified by the exchange                                                                                                                                                                                    |
| CFI_CODE                | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                                  |
| CURRENCY                | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                            |
| EXPIRATION_DATE         | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                                  |
| LAST_TRADING_TIME       | nsectime    | Time when the instrument finishes trading on the final trading day                                                                                                                                                                         |
| CONTRACT_SIZE           | double      | Indicates a derivative’s underlying quantity                                                                                                                                                                                               |
| CONTRACT_UNITS          | string[25]  | Units in which CONTRACT_SIZE is expressed                                                                                                                                                                                                  |
| STRIKE_PRICE            | double      | Exercise price for options / warrants                                                                                                                                                                                                      |
| CALL_PUT_IND            | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                            |
| EXERCISE_TYPE           | string[1]   | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)                                                                                                                                                                 |
| TICK_SIZE_TYPE          | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                       |
| TICK_SIZE               | string[80]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                                 |
| TICK_VALUE              | double      | Tick value, i.e. the profit / loss per contract resulting from a price movement equal to TICK_SIZE.                                                                                                                                        |
| FRACTIONAL_PRICE_FORMAT | string[10]  | Indicates the denominator of the fractional portion of the price, for instruments whose price is conventionally displayed in fractional format. If the display price has a fraction and a subfraction, both are provided, separated by -.  |
| STRATEGY_LEG_COUNT      | int         | Number of legs in a strategy (spread)                                                                                                                                                                                                      |
| STRATEGY_LEGS           | string[600] | Comma-separated list of symbols for the legs of a futures / options spread                                                                                                                                                                 |
| STRATEGY_RATIO          | string[100] | Comma-separated list of ratios for the legs of a futures / options spread. Ratios are listed in the same order as the symbols in STRATEGY_LEGS.                                                                                            |
| HEDGE_LEG_COUNT         | int         | Number of legs in the hedge portion of a spread (e.g. for option spreads hedged against underlying futures)                                                                                                                                |
| HEDGE_LEGS              | string[70]  | Comma-separated list of symbols for the hedge portion of a spread                                                                                                                                                                          |
| HEDGE_RATIO             | string[40]  | Comma-separated list of ratios for the hedge portion of a futures / options spread. Ratios are listed in the same order as the symbols in HEDGE_LEGS.                                                                                      |
| HEDGE_PRICE             | string[70]  | Comma-separated list of prices for the hedge portion of a futures / options spread. Prices are listed in the same order as the symbols in HEDGE_LEGS.                                                                                      |
| MIN_TRADE_SIZE          | int         | Minimum tradable size                                                                                                                                                                                                                      |
| MAX_TRADE_SIZE          | int         | Maximum tradable size                                                                                                                                                                                                                      |
| ORDER_EXEC_ALGO         | string[30]  | Algorithm used by the matching engine to prioritise and match orders                                                                                                                                                                       |
| IMPLIED_PRICING         | string[1]   | Indicates whether a derivative instrument supports implied pricing (Y - Yes, N - No)                                                                                                                                                       |
| EXCH_PRICE_MULTIPLIER   | double      | Multiplier used to convert from the exchange’s internal price value used in the matching engine to the monetary price seen in market data                                                                                                  |
| EXCH_STRIKE_MULTIPLIER  | double      | Multiplier used to convert from the exchange’s internal strike price to the monetary strike price seen in market data                                                                                                                      |
| EXPIRY_CODE             | string[12]  | Code identifying a specific futures / options expiry within the exchange system                                                                                                                                                            |
| EXPIRY_WEEK             | string[2]   | Identifies the week of the month in which weekly futures / options expire                                                                                                                                                                  |
| OMDSEQ                  | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.     |



## COMEX_LATEST

Database includes the following tick types:

* SNAP - Latest Trade & Quote / NBBO Prices for all Instruments in the venue
* SNAP_QTE - Latest Quotes for all Instruments in the venue
* SNAP_TRD - Latest Trade Prices for all Traded Instruments in the venue



### COMEX_LATEST - SNAP

Latest Trade & Quote / NBBO Prices for all Instruments in the venue

#### COMEX_LATEST - SNAP Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                               |
|--------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME        | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                            |
| TIMESTAMP          | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                   |
| PRICE              | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross |
| SIZE               | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross          |
| TRADE_CURRENCY     | string[3]   | Currency in which a trade was executed.                                                                                                                                                                   |
| OPEN               | double      | Open price for the current trading day                                                                                                                                                                    |
| SETTLE_PRICE       | double      | Settlement price                                                                                                                                                                                          |
| SETTLE_DATE        | string[10]  | Trading date to which the settlement price relates (YYYYMMDD)                                                                                                                                             |
| OPEN_INT           | long        | Open interest for futures / options                                                                                                                                                                       |
| OPEN_INT_DATE      | string[10]  | Trading date to which the open interest relates (YYYYMMDD)                                                                                                                                                |
| LATENCY_LOAD       | long        | Latency in milliseconds for the time duration between data collection and in-memory database load                                                                                                         |
| LATENCY_COLLECTION | long        | Latency in milliseconds for the time duration between exchange publishing and data collection                                                                                                             |
| SEC_TYPE           | string[64]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                   |
| VOLUME             | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                         |
| HIGH               | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                               |
| LOW                | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                |
| SYMBOL             | string[64]  | Exchange Symbol                                                                                                                                                                                           |
| LAST_TRADE_TIME    | nsectime    | Last Trade Time                                                                                                                                                                                           |
| BID_PRICE          | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                          |
| ASK_PRICE          | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                          |
| LAST_QUOTE_TIME    | nsectime    | Last Quote Time                                                                                                                                                                                           |

### COMEX_LATEST - SNAP_QTE

Latest Quotes for all Instruments in the venue

#### COMEX_LATEST - SNAP_QTE Table Schema

| Field          | Data Type   | Description                                                                                                                                                    |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME    | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate) |
| TIMESTAMP      | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                        |
| BID_PRICE      | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                               |
| BID_SIZE       | long        | Best bid size                                                                                                                                                  |
| ASK_PRICE      | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                               |
| ASK_SIZE       | long        | Best ask size                                                                                                                                                  |
| QUOTE_CURRENCY | string[3]   | Currency in which a quote price is expressed.                                                                                                                  |
| SYMBOL         | string[64]  | Exchange Symbol                                                                                                                                                |
| TICK_TIME      | nsectime    | Timestamp for latest Trade / Quote or NBBO Update                                                                                                              |

### COMEX_LATEST - SNAP_TRD

Latest Trade Prices for all Traded Instruments in the venue

#### COMEX_LATEST - SNAP_TRD Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                               |
|--------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME        | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                            |
| TIMESTAMP          | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                   |
| PRICE              | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross |
| SIZE               | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross          |
| TRADE_CURRENCY     | string[3]   | Currency in which a trade was executed.                                                                                                                                                                   |
| OPEN               | double      | Open price for the current trading day                                                                                                                                                                    |
| SETTLE_PRICE       | double      | Settlement price                                                                                                                                                                                          |
| SETTLE_DATE        | string[10]  | Trading date to which the settlement price relates (YYYYMMDD)                                                                                                                                             |
| OPEN_INT           | long        | Open interest for futures / options                                                                                                                                                                       |
| OPEN_INT_DATE      | string[10]  | Trading date to which the open interest relates (YYYYMMDD)                                                                                                                                                |
| LATENCY_LOAD       | long        | Latency in milliseconds for the time duration between data collection and in-memory database load                                                                                                         |
| LATENCY_COLLECTION | long        | Latency in milliseconds for the time duration between exchange publishing and data collection                                                                                                             |
| SEC_TYPE           | string[64]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                   |
| VOLUME             | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                         |
| HIGH               | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                               |
| LOW                | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                |
| SYMBOL             | string[64]  | Exchange Symbol                                                                                                                                                                                           |
| TICK_TIME          | nsectime    | Timestamp for latest Trade / Quote or NBBO Update                                                                                                                                                         |
