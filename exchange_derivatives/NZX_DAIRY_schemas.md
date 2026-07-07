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

### NZX_DAIRY - MKT

Market phase / instrument status information

#### NZX_DAIRY - MKT Table Schema

| Field      | Data Type   | Description                                                                                                                                                                                                                            |
|------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME  | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| MKT_PHASE  | string[8]   | Indicates the instrument’s current market phase, as specified by the trading venue                                                                                                                                                     |
| OMDSEQ     | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OMD_STATUS | string[1]   | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| SESSION    | string[8]   | Trading session to which the update relates, e.g. Day, Night, T, T+1                                                                                                                                                                   |

### NZX_DAIRY - QTE

Best bid / offer quotes

#### NZX_DAIRY - QTE Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_PRICE     | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE      | int         | Best ask size                                                                                                                                                                                                                          |
| BID_PRICE     | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE      | int         | Best bid size                                                                                                                                                                                                                          |
| EXCH_TIME     | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| QUOTE_SESSION | string[8]   | Trading session from which the quote originates, e.g. Day, Night                                                                                                                                                                       |

### NZX_DAIRY - STAT

Static data, e.g. ISIN, description, security type

#### NZX_DAIRY - STAT Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                                                                                   |
|---------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALL_PUT_IND        | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                                               |
| CFI_CODE            | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                                                     |
| CONTRACT_SIZE       | double      | Indicates a derivative’s underlying quantity                                                                                                                                                                                                                  |
| CURRENCY            | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                                               |
| DELIVERY_END_DATE   | string[8]   | Date when a derivative’s delivery period ends (YYYYMMDD)                                                                                                                                                                                                      |
| DELIVERY_START_DATE | string[8]   | Date when a derivative’s delivery period begins (YYYYMMDD)                                                                                                                                                                                                    |
| EXCH_SYMBOL         | string[40]  | Ticker symbol specified by the exchange                                                                                                                                                                                                                       |
| EXERCISE_TYPE       | string[1]   | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)                                                                                                                                                                                    |
| EXPIRATION_DATE     | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                                                     |
| FIRST_NOTICE_DATE   | string[8]   | Earliest date when holders of short futures positions can provide notice of their intention to deliver the underlying commodity (YYYYMMDD)                                                                                                                    |
| FIRST_TRADING_DATE  | string[8]   | First date on which the instrument can be traded (YYYYMMDD)                                                                                                                                                                                                   |
| ISIN                | string[12]  | ISIN code                                                                                                                                                                                                                                                     |
| LAST_NOTICE_DATE    | string[8]   | Latest date when holders of short futures positions can provide notice of their intention to deliver the underlying commodity (YYYYMMDD)                                                                                                                      |
| MIC                 | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                                              |
| NAME                | string[200] | Description of the instrument                                                                                                                                                                                                                                 |
| OMDSEQ              | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.                        |
| OPERATING_MIC       | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                                            |
| POINT_VALUE         | double      | Profit / loss per contract resulting from a 1 point price movement (e.g. if the price moves from 123.00 to 124.00).  Note that if an instrument trades in minor currency units such as USX (US cents), the point value will also be expressed in those units. |
| PRODUCT_CODE        | string[10]  | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD.                    |
| SEC_TYPE            | string[20]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                                       |
| SETTLEMENT_TYPE     | string[1]   | Settlement method for a derivatives contract (C - Cash, P - Physical, E - Either cash or physical)                                                                                                                                                            |
| STRATEGY_TYPE       | string[40]  | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly                                                                                                                                                                                            |
| STRIKE_PRICE        | double      | Exercise price for options / warrants                                                                                                                                                                                                                         |
| TICK_SIZE           | string[64]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                                                    |
| TICK_SIZE_TYPE      | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                                          |
| TICK_VALUE          | double      | Tick value, i.e. the profit / loss per contract resulting from a price movement equal to TICK_SIZE.                                                                                                                                                           |
| TRADING_CODE        | string[40]  | ID used to identify the instrument in the trading system                                                                                                                                                                                                      |
| TRADING_CODE_2      | string[20]  | Secondary ID used to identify the instrument in the trading system                                                                                                                                                                                            |
| UNDERLYING_ISIN     | string[12]  | ISIN of the underlying instrument                                                                                                                                                                                                                             |
| UNDERLYING_SEC_TYPE | string[24]  | Underlying asset class                                                                                                                                                                                                                                        |
| UNDERLYING_SYMBOL   | string[40]  | Symbol of the underlying instrument                                                                                                                                                                                                                           |

### NZX_DAIRY - TRD
