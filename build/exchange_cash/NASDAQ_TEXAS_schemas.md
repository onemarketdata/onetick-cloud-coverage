# Nasdaq Texas Schemas

Nasdaq Texas is a U.S. national securities exchange and dual-listing venue headquartered in Dallas. Operated by Nasdaq, Inc., it allows publicly traded companies to maintain a concurrent listing on a Texas-domiciled exchange while trading under their existing ticker symbol, with no new compliance burdens




## NASDAQ_TEXAS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* MM_STATUS - Information on the market makers registered in each security
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* TRD - Trades



### NASDAQ_TEXAS - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### NASDAQ_TEXAS - DAY Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME            | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP              | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| UPDATE_TYPE            | string[16]  | Type of update                                                                                                                                                                                                                         |
| OPEN                   | double      | Open price for the current trading day                                                                                                                                                                                                 |
| HIGH                   | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW                    | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| CLOSE                  | double      | Closing price                                                                                                                                                                                                                          |
| VOLUME                 | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| TRADE_COUNT            | long        | Number of trades on the current trading day                                                                                                                                                                                            |
| TRADE_VALUE            | double      | Total monetary value traded on the current trading day.  Note: The value will typically be rounded to the nearest integer.                                                                                                             |
| VWAP                   | double      | Volume-weighted average price                                                                                                                                                                                                          |
| VOLUME_LIT             | long        | Volume traded in a lit orderbook                                                                                                                                                                                                       |
| VOLUME_DARK            | long        | Volume traded in a dark orderbook                                                                                                                                                                                                      |
| VOLUME_CONTINUOUS      | long        | Volume traded in the main orderbook during continuous trading                                                                                                                                                                          |
| VOLUME_MAIN_SESSION    | long        | Volume of the Main Trading Session                                                                                                                                                                                                     |
| VOLUME_PRE_MARKET      | long        | Volume of the Pre-Market Trading Session                                                                                                                                                                                               |
| VOLUME_POST_MARKET     | long        | Volume of the Post-Market Trading Session                                                                                                                                                                                              |
| VOLUME_AUCTION         | long        | Volume traded during auctions. Includes all auction types.                                                                                                                                                                             |
| PRICE_OPENING_AUCTION  | double      | Price of the Opening Auction                                                                                                                                                                                                           |
| VOLUME_OPENING_AUCTION | long        | Volume of the Opening Auction                                                                                                                                                                                                          |
| PRICE_CLOSING_AUCTION  | double      | Price of the Closing Auction                                                                                                                                                                                                           |
| VOLUME_CLOSING_AUCTION | long        | Volume of the Closing Auction                                                                                                                                                                                                          |
| VOLUME_HIDDEN          | long        | Volume traded against hidden orders in a lit orderbook                                                                                                                                                                                 |
| VOLUME_ODD_LOT         | long        | Volume of the Odd Lot Trades                                                                                                                                                                                                           |
| VOLUME_ROUND_LOT       | long        | Volume of Round Lot Trades                                                                                                                                                                                                             |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### NASDAQ_TEXAS - MKT

Market phase / instrument status information

#### NASDAQ_TEXAS - MKT Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME            | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP              | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME              | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| MKT_PHASE              | string[1]   | Indicates the instrument’s current market phase, as specified by the trading venue                                                                                                                                                     |
| REASON_CODE            | string[4]   | Reason for an instrument status update                                                                                                                                                                                                 |
| SCHEDULED_EVENT_TIME   | nsectime    | Time when an event is due to take place (e.g. if the status update refers to an auction call phase, this indicates when the auction cross will occur)                                                                                  |
| SHORT_SALE_RESTRICTION | string[1]   | Indicates whether short selling is permitted                                                                                                                                                                                           |
| OMD_STATUS             | string[1]   | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| SESSION                | string[12]  | Trading session to which the update relates, e.g. Day, Night, T, T+1                                                                                                                                                                   |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### NASDAQ_TEXAS - MM_STATUS

Information on the market makers registered in each security

#### NASDAQ_TEXAS - MM_STATUS Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME   | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP     | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME     | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| PART_ID       | string[4]   | Identifies the market participant that entered an order / quote                                                                                                                                                                        |
| IS_PRIMARY_MM | string[1]   | Indicates whether the participant identified by PART_ID is a primary market maker in the security (Y - Yes, N - No)                                                                                                                    |
| PART_TYPE     | string[1]   | Indicates the type of market participant identified by PART_ID                                                                                                                                                                         |
| PART_STATUS   | string[1]   | Status of the market participant identified by PART_ID.                                                                                                                                                                                |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### NASDAQ_TEXAS - PRL_FULL

Full orderbook data, showing updates to each individual order (MBO)

#### NASDAQ_TEXAS - PRL_FULL Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                                                                   |
|--------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME        | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                                |
| TIMESTAMP          | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                       |
| EXCH_TIME          | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                             |
| UPDATE_TYPE        | string[1]   | Type of update                                                                                                                                                                                                                                |
| ORDER_ID           | string[20]  | Order identifier, uniquely identifying an order at any given point in time.   Uniqueness depends on the exchange - e.g. may be globally unique, or unique per trading day, or per instrument per trading day.                                 |
| PART_ID            | string[4]   | Identifies the market participant that entered an order / quote                                                                                                                                                                               |
| ORDER_TYPE         | string[1]   | Type of order.                                                                                                                                                                                                                                |
| BUY_SELL_FLAG      | int         | Orderbook side (0 - Buy, 1 - Sell)                                                                                                                                                                                                            |
| PRICE              | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                                     |
| SIZE               | int         | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                              |
| TIME_PRIORITY      | long        | Time priority of an order in the order queue.  If two standard orders on the same side have the same price, the one with the lower value of TIME_PRIORITY will be executed first.                                                             |
| TRADE_ID           | string[20]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                            |
| FILL_PRICE         | double      | Price at which the order was executed                                                                                                                                                                                                         |
| FILL_SIZE          | int         | Size filled in an order execution event                                                                                                                                                                                                       |
| OLD_ORDER_ID       | string[20]  | Previous order ID, where a modification results in a new order ID being issued                                                                                                                                                                |
| OLD_PRICE          | double      | Previous price of an order                                                                                                                                                                                                                    |
| OLD_SIZE           | int         | Previous size of an order                                                                                                                                                                                                                     |
| ORIGINAL_ORDER_ID  | string[20]  | Order ID by which the order was identified when it was first entered.  Some markets issue a new order ID when orders are modified. Using this field, these orders can be tracked using their original order ID.                               |
| PRICE_LEVEL        | int         | Price level of the order after the orderbook update is applied.  e.g. if set to 3, this indicates that the order is at the third best price point after the orderbook update.  Always set to 0 for order deletions.                           |
| OLD_PRICE_LEVEL    | int         | Price level of the order before the orderbook update was applied. e.g. if set to 3, this indicates that the order was at the third best price point before the orderbook update. Always set to 0 for new orders.                              |
| ORDER_POSITION     | int         | Indicates the order’s position in the order queue after the orderbook update is applied. e.g. if set to 1, this indicates that the order is at the front of the order queue after the orderbook update.  Always set to 0 for order deletions. |
| OLD_ORDER_POSITION | int         | Indicates the order’s position in the order queue before the orderbook update was applied. e.g. if set to 1, this indicates that the order was at the front of the order queue before the orderbook update. Always 0 for new orders.          |
| SIZE_AHEAD         | long        | Total order volume ahead of the order in the order queue, after the order update is applied. Always 0 for order deletions.                                                                                                                    |
| RECORD_TYPE        | string[1]   | Type of depth update.                                                                                                                                                                                                                         |
| TICK_STATUS        | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                                  |
| DELETED_TIME       | nsectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                              |
| OMDSEQ             | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.        |

### NASDAQ_TEXAS - QTE

Best bid / offer quotes

#### NASDAQ_TEXAS - QTE Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME    | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP      | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME      | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| BID_PRICE      | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE       | int         | Best bid size                                                                                                                                                                                                                          |
| BID_NUM_ORDERS | int         | Number of orders at the best bid price                                                                                                                                                                                                 |
| ASK_PRICE      | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE       | int         | Best ask size                                                                                                                                                                                                                          |
| ASK_NUM_ORDERS | int         | Number of orders at the best ask price                                                                                                                                                                                                 |
| RPI            | string[1]   | Indicates the presence of Retail Price Improvement interest on bid and/or ask side                                                                                                                                                     |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### NASDAQ_TEXAS - TRD

Trades

#### NASDAQ_TEXAS - TRD Table Schema

| Field             | Data Type   | Description                                                                                                                                                                                                                            |
|-------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME       | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP         | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME         | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| PRICE             | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE              | int         | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| AGGRESSOR_SIDE    | string[1]   | Indicates whether a trade resulted from an incoming buy or sell order.                                                                                                                                                                 |
| TRADE_TYPE        | string[1]   | Type of trade                                                                                                                                                                                                                          |
| TRADE_TYPE_EXT    | string[4]   | Extended trade type code                                                                                                                                                                                                               |
| ODD_LOT           | string[1]   | Indicates whether a trade was an odd lot                                                                                                                                                                                               |
| TRADE_PERIOD      | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                       |
| BOOK_TYPE         | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                            |
| TRADE_ID          | string[20]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| TRADE_ALT_ID      | string[20]  | Secondary trade identifier                                                                                                                                                                                                             |
| EXECUTED_ORDER_ID | string[20]  | ID of the resting (passive) order that was executed                                                                                                                                                                                    |
| OMDSEQ            | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| DELETED_TIME      | nsectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS       | byte        | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |



## NASDAQ_TEXAS_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### NASDAQ_TEXAS_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### NASDAQ_TEXAS_DAILY - DAY Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME            | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP              | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| UPDATE_TYPE            | string[16]  | Type of update                                                                                                                                                                                                                         |
| OPEN                   | double      | Open price for the current trading day                                                                                                                                                                                                 |
| HIGH                   | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW                    | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| CLOSE                  | double      | Closing price                                                                                                                                                                                                                          |
| VOLUME                 | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| TRADE_COUNT            | long        | Number of trades on the current trading day                                                                                                                                                                                            |
| TRADE_VALUE            | double      | Total monetary value traded on the current trading day.  Note: The value will typically be rounded to the nearest integer.                                                                                                             |
| VWAP                   | double      | Volume-weighted average price                                                                                                                                                                                                          |
| VOLUME_LIT             | long        | Volume traded in a lit orderbook                                                                                                                                                                                                       |
| VOLUME_DARK            | long        | Volume traded in a dark orderbook                                                                                                                                                                                                      |
| VOLUME_CONTINUOUS      | long        | Volume traded in the main orderbook during continuous trading                                                                                                                                                                          |
| VOLUME_MAIN_SESSION    | long        | Volume of the Main Trading Session                                                                                                                                                                                                     |
| VOLUME_PRE_MARKET      | long        | Volume of the Pre-Market Trading Session                                                                                                                                                                                               |
| VOLUME_POST_MARKET     | long        | Volume of the Post-Market Trading Session                                                                                                                                                                                              |
| VOLUME_AUCTION         | long        | Volume traded during auctions. Includes all auction types.                                                                                                                                                                             |
| PRICE_OPENING_AUCTION  | double      | Price of the Opening Auction                                                                                                                                                                                                           |
| VOLUME_OPENING_AUCTION | long        | Volume of the Opening Auction                                                                                                                                                                                                          |
| PRICE_CLOSING_AUCTION  | double      | Price of the Closing Auction                                                                                                                                                                                                           |
| VOLUME_CLOSING_AUCTION | long        | Volume of the Closing Auction                                                                                                                                                                                                          |
| VOLUME_HIDDEN          | long        | Volume traded against hidden orders in a lit orderbook                                                                                                                                                                                 |
| VOLUME_ODD_LOT         | long        | Volume of the Odd Lot Trades                                                                                                                                                                                                           |
| VOLUME_ROUND_LOT       | long        | Volume of Round Lot Trades                                                                                                                                                                                                             |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### NASDAQ_TEXAS_DAILY - STAT

Static data, e.g. ISIN, description, security type

#### NASDAQ_TEXAS_DAILY - STAT Table Schema

| Field                 | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME           | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP             | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| NAME                  | string[200] | Description of the instrument                                                                                                                                                                                                          |
| EXCH_SYMBOL           | string[20]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| TRADING_CODE          | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                               |
| MIC                   | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| PRIMARY_MIC           | string[4]   | MIC of the instrument’s primary listing market, or the reference market for instruments traded on an MTF                                                                                                                               |
| OPERATING_MIC         | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| SEC_TYPE              | string[40]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| CURRENCY              | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| LOT_SIZE              | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| TICK_SIZE_TYPE        | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                   |
| TICK_SIZE             | string[80]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                             |
| IPO_FLAG              | string[1]   | Indicates whether the instrument is an IPO (Y - Yes, N - No,  - Unspecified)                                                                                                                                                           |
| FINANCIAL_STATUS      | string[1]   | Indicates the regulatory status of a security or its issuer                                                                                                                                                                            |
| REG_SHO_THRESHOLD_SEC | string[1]   | Indicates whether a security is included in the Threshold List of securities with large, persistent unsettled short positions                                                                                                          |
| OMDSEQ                | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
