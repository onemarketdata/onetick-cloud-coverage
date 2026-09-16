# CME Event Contracts / Prediction Markets Schemas

ME Group offers federally regulated prediction markets via event contracts priced from $0.01 to $0.99, paying out $1 if correct.




## CME_PRED

Database includes the following tick types:

* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* QTE - Best bid / offer quotes
* TRD - Trades



### CME_PRED - IND

Indicative pricing, e.g. indicative auction prices and imbalance

#### CME_PRED - IND Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| PRICE       | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE        | int         | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### CME_PRED - QTE

Best bid / offer quotes

#### CME_PRED - QTE Table Schema

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

### CME_PRED - TRD

Trades

#### CME_PRED - TRD Table Schema

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



## CME_PRED_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### CME_PRED_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### CME_PRED_DAILY - DAY Table Schema

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

### CME_PRED_DAILY - STAT

Static data, e.g. ISIN, description, security type

#### CME_PRED_DAILY - STAT Table Schema

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
