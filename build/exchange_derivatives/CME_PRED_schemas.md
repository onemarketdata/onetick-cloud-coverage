# CME Event Contracts / Prediction Markets Schemas

ME Group offers federally regulated prediction markets via event contracts priced from $0.01 to $0.99, paying out $1 if correct.




## CME_PRED

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### CME_PRED - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### CME_PRED - DAY Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BLOCK_VOLUME  | long        | Total volume of block trades executed on the current day                                                                                                                                                                               |
| CLOSE         | double      | Closing price                                                                                                                                                                                                                          |
| ELEC_VOLUME   | long        | Total volume traded electronically                                                                                                                                                                                                     |
| HIGH          | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW           | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN          | double      | Open price for the current trading day                                                                                                                                                                                                 |
| OPEN_INT      | double      | Open interest for futures / options                                                                                                                                                                                                    |
| OPEN_INT_DATE | string[8]   | Trading date to which the open interest relates (YYYYMMDD)                                                                                                                                                                             |
| SETTLE_DATE   | string[8]   | Trading date to which the settlement price relates (YYYYMMDD)                                                                                                                                                                          |
| SETTLE_PRICE  | double      | Settlement price                                                                                                                                                                                                                       |
| UPDATE_TYPE   | string[16]  | Type of update                                                                                                                                                                                                                         |
| VOLUME        | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |

### CME_PRED - IND

Indicative pricing, e.g. indicative auction prices and imbalance

#### CME_PRED - IND Table Schema

| Field   | Data Type   | Description                                                                                                                                                                                                                            |
|---------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| OMDSEQ  | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE   | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE    | int         | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |

### CME_PRED - LULD

Limit Up / Limit Down price levels

#### CME_PRED - LULD Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                                                            |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DYNAMIC_PRICE_BAND | double      | Maximum price movement from one trade to the next                                                                                                                                                                                      |
| HIGH_LIMIT         | double      | Upper trading limit / circuit breaker level                                                                                                                                                                                            |
| LOW_LIMIT          | double      | Lower trading limit / circuit breaker level                                                                                                                                                                                            |
| OMDSEQ             | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### CME_PRED - MKT

Market phase / instrument status information

#### CME_PRED - MKT Table Schema

| Field        | Data Type   | Description                                                                                                                                                                                                                            |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EVENT_CODE   | string[4]   | Event that triggered an instrument status update                                                                                                                                                                                       |
| MKT_PHASE    | string[6]   | Indicates the instrument’s current market phase, as specified by the trading venue                                                                                                                                                     |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OMD_STATUS   | string[1]   | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| REASON_CODE  | string[4]   | Reason for an instrument status update                                                                                                                                                                                                 |
| TRADING_DATE | string[8]   | Identifies the current business date (YYYYMMDD). May be different to the calendar date, e.g. for T+1 trading sessions.                                                                                                                 |

### CME_PRED - PRL_FULL

Full orderbook data, showing updates to each individual order (MBO)

#### CME_PRED - PRL_FULL Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BUY_SELL_FLAG | int         | Orderbook side (0 - Buy, 1 - Sell)                                                                                                                                                                                                     |
| DELETED_TIME  | nsectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| FILL_SIZE     | int         | Size filled in an order execution event                                                                                                                                                                                                |
| OLD_PRICE     | double      | Previous price of an order                                                                                                                                                                                                             |
| OLD_SIZE      | int         | Previous size of an order                                                                                                                                                                                                              |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| ORDER_ID      | string[20]  | Order identifier, uniquely identifying an order at any given point in time.   Uniqueness depends on the exchange - e.g. may be globally unique, or unique per trading day, or per instrument per trading day.                          |
| ORDER_TYPE    | string[1]   | Type of order.                                                                                                                                                                                                                         |
| PRICE         | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| RECORD_TYPE   | string[1]   | Type of depth update.                                                                                                                                                                                                                  |
| SIZE          | int         | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| TICK_STATUS   | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| TIME_PRIORITY | long        | Time priority of an order in the order queue.  If two standard orders on the same side have the same price, the one with the lower value of TIME_PRIORITY will be executed first.                                                      |
| TRADE_ID      | string[16]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| UPDATE_TYPE   | string[1]   | Type of update                                                                                                                                                                                                                         |

### CME_PRED - QTE

Best bid / offer quotes

#### CME_PRED - QTE Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_NUM_ORDERS   | int         | Number of orders at the best ask price                                                                                                                                                                                                 |
| ASK_PRICE        | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE         | int         | Best ask size                                                                                                                                                                                                                          |
| ASK_SIZE_IMPLIED | int         | Volume of implied orders included in the best ask size (best ask size = implied ask size + outright ask size)                                                                                                                          |
| BID_NUM_ORDERS   | int         | Number of orders at the best bid price                                                                                                                                                                                                 |
| BID_PRICE        | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE         | int         | Best bid size                                                                                                                                                                                                                          |
| BID_SIZE_IMPLIED | int         | Volume of implied orders included in the best bid size (best bid size = implied bid size + outright bid size)                                                                                                                          |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### CME_PRED - STAT

Static data, e.g. ISIN, description, security type

#### CME_PRED - STAT Table Schema

| Field                   | Data Type   | Description                                                                                                                                                                                                                                |
|-------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALL_PUT_IND            | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                            |
| CFI_CODE                | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                                  |
| CONTRACT_SIZE           | double      | Indicates a derivative’s underlying quantity                                                                                                                                                                                               |
| CONTRACT_UNITS          | string[25]  | Units in which CONTRACT_SIZE is expressed                                                                                                                                                                                                  |
| CURRENCY                | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                            |
| EXCH_PRICE_MULTIPLIER   | double      | Multiplier used to convert from the exchange’s internal price value used in the matching engine to the monetary price seen in market data                                                                                                  |
| EXCH_SEC_TYPE           | string[30]  | Instrument type as specified by the exchange                                                                                                                                                                                               |
| EXCH_STRATEGY_TYPE      | string[30]  | Type of strategy / spread, as specified by the exchange                                                                                                                                                                                    |
| EXCH_STRIKE_MULTIPLIER  | double      | Multiplier used to convert from the exchange’s internal strike price to the monetary strike price seen in market data                                                                                                                      |
| EXCH_SYMBOL             | string[30]  | Ticker symbol specified by the exchange                                                                                                                                                                                                    |
| EXERCISE_TYPE           | string[1]   | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)                                                                                                                                                                 |
| EXPIRATION_DATE         | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                                  |
| EXPIRY_CODE             | string[12]  | Code identifying a specific futures / options expiry within the exchange system                                                                                                                                                            |
| EXPIRY_WEEK             | string[2]   | Identifies the week of the month in which weekly futures / options expire                                                                                                                                                                  |
| FRACTIONAL_PRICE_FORMAT | string[10]  | Indicates the denominator of the fractional portion of the price, for instruments whose price is conventionally displayed in fractional format. If the display price has a fraction and a subfraction, both are provided, separated by -.  |
| HEDGE_LEGS              | string[70]  | Comma-separated list of symbols for the hedge portion of a spread                                                                                                                                                                          |
| HEDGE_LEG_COUNT         | int         | Number of legs in the hedge portion of a spread (e.g. for option spreads hedged against underlying futures)                                                                                                                                |
| HEDGE_PRICE             | string[70]  | Comma-separated list of prices for the hedge portion of a futures / options spread. Prices are listed in the same order as the symbols in HEDGE_LEGS.                                                                                      |
| HEDGE_RATIO             | string[40]  | Comma-separated list of ratios for the hedge portion of a futures / options spread. Ratios are listed in the same order as the symbols in HEDGE_LEGS.                                                                                      |
| IMPLIED_PRICING         | string[1]   | Indicates whether a derivative instrument supports implied pricing (Y - Yes, N - No)                                                                                                                                                       |
| LAST_TRADING_TIME       | nsectime    | Time when the instrument finishes trading on the final trading day                                                                                                                                                                         |
| MAX_TRADE_SIZE          | int         | Maximum tradable size                                                                                                                                                                                                                      |
| MIC                     | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                           |
| MIN_TRADE_SIZE          | int         | Minimum tradable size                                                                                                                                                                                                                      |
| NAME                    | string[250] | Description of the instrument                                                                                                                                                                                                              |
| OMDSEQ                  | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.     |
| OPERATING_MIC           | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                         |
| ORDER_EXEC_ALGO         | string[30]  | Algorithm used by the matching engine to prioritise and match orders                                                                                                                                                                       |
| PRODUCT_CODE            | string[20]  | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD. |
| SEC_TYPE                | string[30]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                    |
| STRATEGY_LEGS           | string[600] | Comma-separated list of symbols for the legs of a futures / options spread                                                                                                                                                                 |
| STRATEGY_LEG_COUNT      | int         | Number of legs in a strategy (spread)                                                                                                                                                                                                      |
| STRATEGY_RATIO          | string[100] | Comma-separated list of ratios for the legs of a futures / options spread. Ratios are listed in the same order as the symbols in STRATEGY_LEGS.                                                                                            |
| STRATEGY_TYPE           | string[40]  | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly                                                                                                                                                                         |
| STRIKE_PRICE            | double      | Exercise price for options / warrants                                                                                                                                                                                                      |
| TICK_SIZE               | string[80]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                                 |
| TICK_SIZE_TYPE          | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                       |
| TICK_VALUE              | double      | Tick value, i.e. the profit / loss per contract resulting from a price movement equal to TICK_SIZE.                                                                                                                                        |
| TRADING_CODE            | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                                   |
| TRADING_GROUP           | string[8]   | Trading group to which the instrument belongs. Instruments in the same trading group will have the same trading schedule, order matching algorithm, etc.                                                                                   |
| UNDERLYING_EXCH_SYMBOL  | string[30]  | Ticker symbol of the underlying instrument, as specified by the exchange                                                                                                                                                                   |
| UNDERLYING_SEC_TYPE     | string[20]  | Underlying asset class                                                                                                                                                                                                                     |
| UNDERLYING_SYMBOL       | string[40]  | Symbol of the underlying instrument                                                                                                                                                                                                        |

### CME_PRED - TRD

Trades

#### CME_PRED - TRD Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AGGRESSOR_SIDE | string[1]   | Indicates whether a trade resulted from an incoming buy or sell order.                                                                                                                                                                 |
| BOOK_TYPE      | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                            |
| BUY_ORDER_ID   | string[20]  | ID of the buy order involved in a trade                                                                                                                                                                                                |
| DELETED_TIME   | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| EXCH_TIME      | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE          | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SELL_ORDER_ID  | string[20]  | ID of the sell order involved in a trade                                                                                                                                                                                               |
| SIZE           | int         | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| TICK_STATUS    | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| TRADE_ID       | string[16]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| TRADE_PERIOD   | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                       |
| TRADE_TYPE     | string[4]   | Type of trade                                                                                                                                                                                                                          |



## CME_PRED_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### CME_PRED_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### CME_PRED_DAILY - DAY Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BLOCK_VOLUME  | long        | Total volume of block trades executed on the current day                                                                                                                                                                               |
| CLOSE         | double      | Closing price                                                                                                                                                                                                                          |
| ELEC_VOLUME   | long        | Total volume traded electronically                                                                                                                                                                                                     |
| HIGH          | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW           | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN          | double      | Open price for the current trading day                                                                                                                                                                                                 |
| OPEN_INT      | double      | Open interest for futures / options                                                                                                                                                                                                    |
| OPEN_INT_DATE | string[8]   | Trading date to which the open interest relates (YYYYMMDD)                                                                                                                                                                             |
| SETTLE_DATE   | string[8]   | Trading date to which the settlement price relates (YYYYMMDD)                                                                                                                                                                          |
| SETTLE_PRICE  | double      | Settlement price                                                                                                                                                                                                                       |
| UPDATE_TYPE   | string[16]  | Type of update                                                                                                                                                                                                                         |
| VOLUME        | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |

### CME_PRED_DAILY - STAT

Static data, e.g. ISIN, description, security type

#### CME_PRED_DAILY - STAT Table Schema

| Field                   | Data Type   | Description                                                                                                                                                                                                                                |
|-------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALL_PUT_IND            | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                            |
| CFI_CODE                | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                                  |
| CONTRACT_SIZE           | double      | Indicates a derivative’s underlying quantity                                                                                                                                                                                               |
| CONTRACT_UNITS          | string[25]  | Units in which CONTRACT_SIZE is expressed                                                                                                                                                                                                  |
| CURRENCY                | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                            |
| EXCH_PRICE_MULTIPLIER   | double      | Multiplier used to convert from the exchange’s internal price value used in the matching engine to the monetary price seen in market data                                                                                                  |
| EXCH_SEC_TYPE           | string[30]  | Instrument type as specified by the exchange                                                                                                                                                                                               |
| EXCH_STRATEGY_TYPE      | string[30]  | Type of strategy / spread, as specified by the exchange                                                                                                                                                                                    |
| EXCH_STRIKE_MULTIPLIER  | double      | Multiplier used to convert from the exchange’s internal strike price to the monetary strike price seen in market data                                                                                                                      |
| EXCH_SYMBOL             | string[30]  | Ticker symbol specified by the exchange                                                                                                                                                                                                    |
| EXERCISE_TYPE           | string[1]   | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)                                                                                                                                                                 |
| EXPIRATION_DATE         | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                                  |
| EXPIRY_CODE             | string[12]  | Code identifying a specific futures / options expiry within the exchange system                                                                                                                                                            |
| EXPIRY_WEEK             | string[2]   | Identifies the week of the month in which weekly futures / options expire                                                                                                                                                                  |
| FRACTIONAL_PRICE_FORMAT | string[10]  | Indicates the denominator of the fractional portion of the price, for instruments whose price is conventionally displayed in fractional format. If the display price has a fraction and a subfraction, both are provided, separated by -.  |
| HEDGE_LEGS              | string[70]  | Comma-separated list of symbols for the hedge portion of a spread                                                                                                                                                                          |
| HEDGE_LEG_COUNT         | int         | Number of legs in the hedge portion of a spread (e.g. for option spreads hedged against underlying futures)                                                                                                                                |
| HEDGE_PRICE             | string[70]  | Comma-separated list of prices for the hedge portion of a futures / options spread. Prices are listed in the same order as the symbols in HEDGE_LEGS.                                                                                      |
| HEDGE_RATIO             | string[40]  | Comma-separated list of ratios for the hedge portion of a futures / options spread. Ratios are listed in the same order as the symbols in HEDGE_LEGS.                                                                                      |
| IMPLIED_PRICING         | string[1]   | Indicates whether a derivative instrument supports implied pricing (Y - Yes, N - No)                                                                                                                                                       |
| LAST_TRADING_TIME       | nsectime    | Time when the instrument finishes trading on the final trading day                                                                                                                                                                         |
| MAX_TRADE_SIZE          | int         | Maximum tradable size                                                                                                                                                                                                                      |
| MIC                     | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                           |
| MIN_TRADE_SIZE          | int         | Minimum tradable size                                                                                                                                                                                                                      |
| NAME                    | string[250] | Description of the instrument                                                                                                                                                                                                              |
| OMDSEQ                  | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.     |
| OPERATING_MIC           | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                         |
| ORDER_EXEC_ALGO         | string[30]  | Algorithm used by the matching engine to prioritise and match orders                                                                                                                                                                       |
| PRODUCT_CODE            | string[20]  | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD. |
| SEC_TYPE                | string[30]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                    |
| STRATEGY_LEGS           | string[600] | Comma-separated list of symbols for the legs of a futures / options spread                                                                                                                                                                 |
| STRATEGY_LEG_COUNT      | int         | Number of legs in a strategy (spread)                                                                                                                                                                                                      |
| STRATEGY_RATIO          | string[100] | Comma-separated list of ratios for the legs of a futures / options spread. Ratios are listed in the same order as the symbols in STRATEGY_LEGS.                                                                                            |
| STRATEGY_TYPE           | string[40]  | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly                                                                                                                                                                         |
| STRIKE_PRICE            | double      | Exercise price for options / warrants                                                                                                                                                                                                      |
| TICK_SIZE               | string[80]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                                 |
| TICK_SIZE_TYPE          | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                       |
| TICK_VALUE              | double      | Tick value, i.e. the profit / loss per contract resulting from a price movement equal to TICK_SIZE.                                                                                                                                        |
| TRADING_CODE            | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                                   |
| TRADING_GROUP           | string[8]   | Trading group to which the instrument belongs. Instruments in the same trading group will have the same trading schedule, order matching algorithm, etc.                                                                                   |
| UNDERLYING_EXCH_SYMBOL  | string[30]  | Ticker symbol of the underlying instrument, as specified by the exchange                                                                                                                                                                   |
| UNDERLYING_SEC_TYPE     | string[20]  | Underlying asset class                                                                                                                                                                                                                     |
| UNDERLYING_SYMBOL       | string[40]  | Symbol of the underlying instrument                                                                                                                                                                                                        |
