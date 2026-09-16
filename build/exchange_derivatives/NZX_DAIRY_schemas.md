# SGX-NZX Dairy Derivatives Schemas

SGX-NZX’s Dairy Derivatives Market provides the dairy industry with a forward view of dairy prices and a cash settled instrument for managing price risk simply and efficiently.




## NZX_DAIRY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### NZX_DAIRY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### NZX_DAIRY - DAY Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME     | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP       | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| UPDATE_TYPE     | string[16]  | Type of update                                                                                                                                                                                                                         |
| SESSION         | string[8]   | Trading session to which the update relates, e.g. Day, Night, T, T+1                                                                                                                                                                   |
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

### NZX_DAIRY - MKT

Market phase / instrument status information

#### NZX_DAIRY - MKT Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME   | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| MKT_PHASE   | string[8]   | Indicates the instrument’s current market phase, as specified by the trading venue                                                                                                                                                     |
| OMD_STATUS  | string[1]   | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| SESSION     | string[8]   | Trading session to which the update relates, e.g. Day, Night, T, T+1                                                                                                                                                                   |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### NZX_DAIRY - QTE

Best bid / offer quotes

#### NZX_DAIRY - QTE Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME   | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP     | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME     | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| BID_PRICE     | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE      | int         | Best bid size                                                                                                                                                                                                                          |
| ASK_PRICE     | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE      | int         | Best ask size                                                                                                                                                                                                                          |
| QUOTE_SESSION | string[8]   | Trading session from which the quote originates, e.g. Day, Night                                                                                                                                                                       |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### NZX_DAIRY - STAT

Static data, e.g. ISIN, description, security type

#### NZX_DAIRY - STAT Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                                                                                   |
|---------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME         | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                                                |
| TIMESTAMP           | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                                       |
| NAME                | string[200] | Description of the instrument                                                                                                                                                                                                                                 |
| ISIN                | string[12]  | ISIN code                                                                                                                                                                                                                                                     |
| EXCH_SYMBOL         | string[40]  | Ticker symbol specified by the exchange                                                                                                                                                                                                                       |
| TRADING_CODE        | string[40]  | ID used to identify the instrument in the trading system                                                                                                                                                                                                      |
| TRADING_CODE_2      | string[20]  | Secondary ID used to identify the instrument in the trading system                                                                                                                                                                                            |
| PRODUCT_CODE        | string[10]  | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD.                    |
| UNDERLYING_SYMBOL   | string[40]  | Symbol of the underlying instrument                                                                                                                                                                                                                           |
| UNDERLYING_ISIN     | string[12]  | ISIN of the underlying instrument                                                                                                                                                                                                                             |
| MIC                 | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                                              |
| OPERATING_MIC       | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                                            |
| SEC_TYPE            | string[20]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                                       |
| UNDERLYING_SEC_TYPE | string[24]  | Underlying asset class                                                                                                                                                                                                                                        |
| STRATEGY_TYPE       | string[40]  | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly                                                                                                                                                                                            |
| CFI_CODE            | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                                                     |
| CURRENCY            | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                                               |
| EXPIRATION_DATE     | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                                                     |
| FIRST_TRADING_DATE  | string[8]   | First date on which the instrument can be traded (YYYYMMDD)                                                                                                                                                                                                   |
| FIRST_NOTICE_DATE   | string[8]   | Earliest date when holders of short futures positions can provide notice of their intention to deliver the underlying commodity (YYYYMMDD)                                                                                                                    |
| LAST_NOTICE_DATE    | string[8]   | Latest date when holders of short futures positions can provide notice of their intention to deliver the underlying commodity (YYYYMMDD)                                                                                                                      |
| DELIVERY_START_DATE | string[8]   | Date when a derivative’s delivery period begins (YYYYMMDD)                                                                                                                                                                                                    |
| DELIVERY_END_DATE   | string[8]   | Date when a derivative’s delivery period ends (YYYYMMDD)                                                                                                                                                                                                      |
| STRIKE_PRICE        | double      | Exercise price for options / warrants                                                                                                                                                                                                                         |
| CALL_PUT_IND        | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                                               |
| EXERCISE_TYPE       | string[1]   | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)                                                                                                                                                                                    |
| SETTLEMENT_TYPE     | string[1]   | Settlement method for a derivatives contract (C - Cash, P - Physical, E - Either cash or physical)                                                                                                                                                            |
| CONTRACT_SIZE       | double      | Indicates a derivative’s underlying quantity                                                                                                                                                                                                                  |
| TICK_SIZE_TYPE      | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                                          |
| TICK_SIZE           | string[64]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                                                    |
| TICK_VALUE          | double      | Tick value, i.e. the profit / loss per contract resulting from a price movement equal to TICK_SIZE.                                                                                                                                                           |
| POINT_VALUE         | double      | Profit / loss per contract resulting from a 1 point price movement (e.g. if the price moves from 123.00 to 124.00).  Note that if an instrument trades in minor currency units such as USX (US cents), the point value will also be expressed in those units. |
| OMDSEQ              | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.                        |

### NZX_DAIRY - TRD

Trades

#### NZX_DAIRY - TRD Table Schema

| Field             | Data Type   | Description                                                                                                                                                                                                                            |
|-------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME       | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP         | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME         | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| PRICE             | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE              | int         | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| AGGRESSOR_SIDE    | string[1]   | Indicates whether a trade resulted from an incoming buy or sell order.                                                                                                                                                                 |
| TRADE_TYPE        | string[8]   | Type of trade                                                                                                                                                                                                                          |
| TRADE_PERIOD      | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                       |
| BOOK_TYPE         | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                            |
| TRADE_SESSION     | string[8]   | Trading session from which a trade originates, e.g. Day, Night                                                                                                                                                                         |
| TRADE_ID          | string[20]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| COMBO_TRADE_ID    | string[20]  | Links leg trades in outright instruments with the spread trade that generated them                                                                                                                                                     |
| EXECUTED_ORDER_ID | string[20]  | ID of the resting (passive) order that was executed                                                                                                                                                                                    |
| DELETED_TIME      | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS       | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| OMDSEQ            | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
