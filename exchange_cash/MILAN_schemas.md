# Euronext Milan (Borsa Italiana) - Equities Schemas

Borsa Italiana is Italy’s main stock exchange located in Milan, facilitating trading in Italian equities.




## MILAN

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### MILAN - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### MILAN - DAY Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOSE                  | double      | Closing price                                                                                                                                                                                                                          |
| CURRENCY               | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| HIGH                   | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW                    | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OFF_BOOK_VOLUME        | long        | Total volume traded off-book                                                                                                                                                                                                           |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN                   | double      | Open price for the current trading day                                                                                                                                                                                                 |
| TRADE_COUNT            | long        | Number of trades on the current trading day                                                                                                                                                                                            |
| TURNOVER               | double      | Total monetary value traded on the current trading day                                                                                                                                                                                 |
| VOLUME                 | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VOLUME_AUCTION         | long        | Volume traded during auctions. Includes all auction types.                                                                                                                                                                             |
| VOLUME_CLOSING_AUCTION | long        | Volume of the Closing Auction                                                                                                                                                                                                          |
| VOLUME_CONTINUOUS      | long        | Volume traded in the main orderbook during continuous trading                                                                                                                                                                          |
| VOLUME_DARK            | long        | Volume traded in a dark orderbook                                                                                                                                                                                                      |
| VOLUME_LIT             | long        | Volume traded in a lit orderbook                                                                                                                                                                                                       |
| VOLUME_OPENING_AUCTION | long        | Volume of the Opening Auction                                                                                                                                                                                                          |
| VOLUME_RFQ             | long        | Volume traded through an RFQ / RFC (Request for Quote / Request for Cross) process                                                                                                                                                     |
| VWAP                   | double      | Volume-weighted average price                                                                                                                                                                                                          |

### MILAN - IND

Indicative pricing, e.g. indicative auction prices and imbalance

#### MILAN - IND Table Schema

| Field        | Data Type   | Description                                                                                                                                                                                                                            |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AUCTION_TYPE | string[1]   | Type of auction from which an indicative auction price / auction imbalance originates.                                                                                                                                                 |
| EXCH_TIME    | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| IMB_SIDE     | string[1]   | Indicates if one side of the orderbook has excess executable orders during an auction phase.                                                                                                                                           |
| IMB_VOLUME   | long        | Size of an auction imbalance, i.e. the excess volume of orders on the side indicated by IMB_SIDE                                                                                                                                       |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE        | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE         | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |

### MILAN - MKT

Market phase / instrument status information

#### MILAN - MKT Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                                                            |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME          | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| MKT_PHASE          | string[4]   | Indicates the instrument’s current market phase, as specified by the trading venue                                                                                                                                                     |
| OMDSEQ             | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OMD_STATUS         | string[1]   | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| ORDER_ENTRY_STATUS | string[1]   | Indicates the availability of order entry / modification / cancellation                                                                                                                                                                |
| REASON_CODE        | string[1]   | Reason for an instrument status update                                                                                                                                                                                                 |
| SESSION            | string[12]  | Trading session to which the update relates, e.g. Day, Night, T, T+1                                                                                                                                                                   |

### MILAN - PRL_FULL

Full orderbook data, showing updates to each individual order (MBO)

#### MILAN - PRL_FULL Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BUY_SELL_FLAG | int         | Orderbook side (0 - Buy, 1 - Sell)                                                                                                                                                                                                     |
| DELETED_TIME  | nsectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| EXCH_TIME     | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| ORDER_ID      | string[20]  | Order identifier, uniquely identifying an order at any given point in time.   Uniqueness depends on the exchange - e.g. may be globally unique, or unique per trading day, or per instrument per trading day.                          |
| ORDER_TYPE    | string[1]   | Type of order.                                                                                                                                                                                                                         |
| PRICE         | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| RECORD_TYPE   | string[1]   | Type of depth update.                                                                                                                                                                                                                  |
| SIZE          | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| TICK_STATUS   | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| TIME_PRIORITY | long        | Time priority of an order in the order queue.  If two standard orders on the same side have the same price, the one with the lower value of TIME_PRIORITY will be executed first.                                                      |
| UPDATE_TYPE   | string[1]   | Type of update                                                                                                                                                                                                                         |

### MILAN - QTE

Best bid / offer quotes

#### MILAN - QTE Table Schema

| Field     | Data Type   | Description                                                                                                                                                                                                                            |
|-----------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_PRICE | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE  | long        | Best ask size                                                                                                                                                                                                                          |
| BID_PRICE | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE  | long        | Best bid size                                                                                                                                                                                                                          |
| EXCH_TIME | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ    | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### MILAN - STAT

Static data, e.g. ISIN, description, security type

#### MILAN - STAT Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CFI_CODE      | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                              |
| CURRENCY      | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| EXCH_SYMBOL   | string[20]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| ISIN          | string[12]  | ISIN code                                                                                                                                                                                                                              |
| LOT_SIZE      | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| MIC           | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| MKT_SEGMENT   | string[4]   | Market segment on which the instrument is traded                                                                                                                                                                                       |
| NAME          | string[100] | Description of the instrument                                                                                                                                                                                                          |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPERATING_MIC | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| SEC_TYPE      | string[40]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| TRADING_CODE  | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                               |

### MILAN - TRD

Trades

#### MILAN - TRD Table Schema

| Field                 | Data Type   | Description                                                                                                                                                                                                                                       |
|-----------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AGGRESSOR_SIDE        | string[1]   | Indicates whether a trade resulted from an incoming buy or sell order.                                                                                                                                                                            |
| BOOK_TYPE             | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                                       |
| DELETED_TIME          | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                                  |
| EXCH_TIME             | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                                 |
| MMT_ALGO_IND          | string[1]   | Identifies whether a trade involved an algorithmic order.                                                                                                                                                                                         |
| MMT_BENCHMARK_IND     | string[1]   | Identifies whether a trade was priced according to a defined benchmark (e.g. VWAP) or reference price (e.g. midpoint of the primary market BBO), or whether it was part of a trade in multiple instruments (contingent trade or portfolio trade). |
| MMT_CROSS_IND         | string[1]   | Identifies agency cross trades, where a broker crossed two client orders outside the order book.                                                                                                                                                  |
| MMT_DEFERRAL_TYPE     | string[1]   | Type of publication deferral or subsequent enrichment applied to a trade report.                                                                                                                                                                  |
| MMT_DIVIDEND_IND      | string[1]   | Identifies whether a trade includes special dividend arrangements, e.g. a trade sold cum-dividend during an ex-dividend period.                                                                                                                   |
| MMT_DUP_IND           | string[1]   | Identifies trades reported to more than one Approved Publication Arrangement.                                                                                                                                                                     |
| MMT_MKT_MECH          | string[1]   | Market mechanism through which a trade was executed.                                                                                                                                                                                              |
| MMT_MOD_IND           | string[1]   | Identifies trade cancellations, or amendments of a previous trade.                                                                                                                                                                                |
| MMT_NEGOTIATED_IND    | string[1]   | Indicates privately negotiated trades, or Systematic Internaliser trades exempt from pre-trade transparency.                                                                                                                                      |
| MMT_OFF_BOOK_AUTO_IND | string[1]   | Identifies whether an off-book trade report was executed via a manual or automated process.                                                                                                                                                       |
| MMT_PRICE_FORMING_IND | string[1]   | Identifies whether a trade is price-forming, or contributes to the price discovery process.                                                                                                                                                       |
| MMT_PUB_MODE          | string[1]   | Identifies whether a trade was subject to delayed publication, and the reason for the deferral.                                                                                                                                                   |
| MMT_TRANS_CAT         | string[1]   | Identifies various special categories of trade.                                                                                                                                                                                                   |
| MMT_TRD_MODE          | string[1]   | Trading period during which an on-book trade was executed, or origin of an off-book trade report (on-exchange / off-exchange / SI).                                                                                                               |
| OMDSEQ                | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.            |
| PRICE                 | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                                         |
| PUB_VENUE             | string[4]   | Venue (MIC) used to publish an off-exchange trade                                                                                                                                                                                                 |
| SIZE                  | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                                  |
| TICK_STATUS           | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                                      |
| TRADE_CURRENCY        | string[3]   | Currency in which a trade was executed.                                                                                                                                                                                                           |
| TRADE_ID              | string[52]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                                |
| TRADE_PERIOD          | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                                  |
| TRADE_TYPE            | string[6]   | Type of trade                                                                                                                                                                                                                                     |
| TRADE_VENUE           | string[4]   | Identifies the venue where a trade was executed.   Typically a MIC, with the special values XOFF for off-exchange and SINT for Systematic Internaliser trades.                                                                                    |



## MILAN_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* LAT_1M - 1-minute Latency bars for real time delivered data
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars



### MILAN_BARS - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### MILAN_BARS - DAY Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOSE                  | double      | Closing price                                                                                                                                                                                                                          |
| CURRENCY               | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| HIGH                   | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW                    | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OFF_BOOK_VOLUME        | long        | Total volume traded off-book                                                                                                                                                                                                           |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN                   | double      | Open price for the current trading day                                                                                                                                                                                                 |
| TRADE_COUNT            | long        | Number of trades on the current trading day                                                                                                                                                                                            |
| TURNOVER               | double      | Total monetary value traded on the current trading day                                                                                                                                                                                 |
| VOLUME                 | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VOLUME_AUCTION         | long        | Volume traded during auctions. Includes all auction types.                                                                                                                                                                             |
| VOLUME_CLOSING_AUCTION | long        | Volume of the Closing Auction                                                                                                                                                                                                          |
| VOLUME_CONTINUOUS      | long        | Volume traded in the main orderbook during continuous trading                                                                                                                                                                          |
| VOLUME_DARK            | long        | Volume traded in a dark orderbook                                                                                                                                                                                                      |
| VOLUME_LIT             | long        | Volume traded in a lit orderbook                                                                                                                                                                                                       |
| VOLUME_OPENING_AUCTION | long        | Volume of the Opening Auction                                                                                                                                                                                                          |
| VOLUME_RFQ             | long        | Volume traded through an RFQ / RFC (Request for Quote / Request for Cross) process                                                                                                                                                     |
| VWAP                   | double      | Volume-weighted average price                                                                                                                                                                                                          |

### MILAN_BARS - LAT_1M

1-minute Latency bars for real time delivered data

#### MILAN_BARS - LAT_1M Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AVG_LATENCY_COLLECTION | double      | Average Latency of Real Time Collection.  Difference between Exchange timestamp and collection timestamp.                                                                                                                              |
| AVG_LATENCY_LOAD       | double      | Average Latency of Real Time Loading.  Difference between the collection timestamp and availability within the Memory Database.                                                                                                        |
| MAX_LATENCY_COLLECTION | double      | Maximum Latency of Real Time Collection.  Difference between Exchange timestamp and collection timestamp.                                                                                                                              |
| MAX_LATENCY_LOAD       | double      | Maximum Latency of Real Time Loading.  Difference between the collection timestamp and availability within the Memory Database.                                                                                                        |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### MILAN_BARS - MKT

Market phase / instrument status information

#### MILAN_BARS - MKT Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                                                            |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME          | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| MKT_PHASE          | string[4]   | Indicates the instrument’s current market phase, as specified by the trading venue                                                                                                                                                     |
| OMDSEQ             | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OMD_STATUS         | string[64]  | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| ORDER_ENTRY_STATUS | string[1]   | Indicates the availability of order entry / modification / cancellation                                                                                                                                                                |
| REASON_CODE        | string[1]   | Reason for an instrument status update                                                                                                                                                                                                 |
| SESSION            | string[12]  | Trading session to which the update relates, e.g. Day, Night, T, T+1                                                                                                                                                                   |

### MILAN_BARS - QTE_1M

1-minute quote bars

#### MILAN_BARS - QTE_1M Table Schema

| Field                 | Data Type   | Description                                                                                                                                                                                                                                       |
|-----------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_PRICE_AT_HIGH_BID | double      | Ask price of the quote that set HIGH_BID.  If there are multiple bid quotes at HIGH_BID, the first one is used.                                                                                                                                   |
| ASK_SIZE_AT_HIGH_BID  | long        | Ask size of the quote that set HIGH_BID.  If there are multiple bid quotes at HIGH_BID, the first one is used.                                                                                                                                    |
| BID_PRICE_AT_LOW_ASK  | double      | Bid price of the quote that set LOW_ASK. If there are multiple ask quotes at LOW_ASK, the first one is used.                                                                                                                                      |
| BID_SIZE_LOW_ASK      | long        | Bid size of the quote that set LOW_ASK.  If there are multiple ask quotes at LOW_ASK, the first one is used.                                                                                                                                      |
| CLOUD_DB              | string[32]  | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.                                                                                        |
| FIRST_ASK_PRICE       | double      | Price of the first best ask update in the current bar interval                                                                                                                                                                                    |
| FIRST_ASK_SIZE        | long        | Size of the first best ask update in the current bar interval                                                                                                                                                                                     |
| FIRST_ASK_TIME        | nsectime    | Time of the first best ask update in the current bar interval                                                                                                                                                                                     |
| FIRST_BID_PRICE       | double      | Price of the first best bid update in the current bar interval                                                                                                                                                                                    |
| FIRST_BID_SIZE        | long        | Size of the first best bid update in the current bar interval                                                                                                                                                                                     |
| FIRST_BID_TIME        | nsectime    | Time of the first best bid update in the current bar interval                                                                                                                                                                                     |
| HIGH_BID              | double      | Highest bid price in the current bar interval                                                                                                                                                                                                     |
| HIGH_BID_SIZE         | long        | Size of the bid quote that set HIGH_BID.  If there are multiple quotes at that price, the first one is used.                                                                                                                                      |
| HIGH_BID_TIME         | nsectime    | Time of the bid quote that set HIGH_BID.  If there are multiple quotes at that price, the first one is used.                                                                                                                                      |
| LAST_ASK_PRICE        | double      | Price of the last best ask update in the current bar interval                                                                                                                                                                                     |
| LAST_ASK_SIZE         | long        | Size of the last best ask update in the current bar interval                                                                                                                                                                                      |
| LAST_ASK_TIME         | nsectime    | Time of the last best ask update in the current bar interval                                                                                                                                                                                      |
| LAST_BID_PRICE        | double      | Price of the last best bid update in the current bar interval                                                                                                                                                                                     |
| LAST_BID_SIZE         | long        | Size of the last best bid update in the current bar interval                                                                                                                                                                                      |
| LAST_BID_TIME         | nsectime    | Time of the last best bid update in the current bar interval                                                                                                                                                                                      |
| LOW_ASK               | double      | Lowest ask price in the current bar interval                                                                                                                                                                                                      |
| LOW_ASK_SIZE          | long        | Size of the ask quote that set LOW_ASK.  If there are multiple quotes at that price, the first one is used.                                                                                                                                       |
| LOW_ASK_TIME          | nsectime    | Time of the bid quote that set LOW_ASK.  If there are multiple quotes at that price, the first one is used.                                                                                                                                       |
| MID_LAST              | double      | Midpoint of the last best bid/ask in the current bar interval. [Note: One-sided or empty quotes are excluded from the calculation]                                                                                                                |
| MID_MEDIAN            | double      | Median of the midpoint of the best bid/ask quotes over the current bar interval. [Note: One-sided or empty quotes are excluded from the calculation]                                                                                              |
| MID_TWAP              | double      | Time-weighted average of the midpoint of the best bid/ask over the current bar interval.  [Note: One-sided or empty quotes are excluded from the calculation]                                                                                     |
| OMDSEQ                | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.            |
| QUOTE_CURRENCY        | string[3]   | Currency in which a quote price is expressed.                                                                                                                                                                                                     |
| QUOTE_TICK_COUNT      | long        | Number of BBO quotes in the current bar interval                                                                                                                                                                                                  |
| SPREAD_LAST           | double      | Last value of (best ask price - best bid price) over the current bar interval.  [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation]                                       |
| SPREAD_MAX            | double      | Widest bid/ask spread, i.e. the highest value of (best ask price - best bid price) over the current bar interval.   [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation]   |
| SPREAD_MEDIAN         | double      | Median value of (best ask price - best bid price) over the current bar interval.   [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation]                                    |
| SPREAD_MIN            | double      | Narrowest bid/ask spread, i.e. the lowest value of (best ask price - best bid price) over the current bar interval.   [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation] |
| SPREAD_TWAP           | double      | Time-weighted average of (best ask price - best bid price) over the current bar interval.  [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation]                            |

### MILAN_BARS - TRD_1D

Daily trade bars

#### MILAN_BARS - TRD_1D Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BUY_VOLUME       | long        | Traded volume originating from incoming buy orders.  Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| CLOUD_DB         | string[32]  | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.                                                                             |
| FIRST            | double      | Price of the first eligible trade in the current bar interval                                                                                                                                                                          |
| FIRST_SIZE       | long        | Size of the first eligible trade in the current bar interval                                                                                                                                                                           |
| FIRST_TIME       | nsectime    | Timestamp of the first eligible trade in the current bar interval                                                                                                                                                                      |
| HIGH             | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| HIGH_SIZE        | long        | Size of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                    |
| HIGH_TIME        | nsectime    | Timestamp of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                               |
| LAST             | double      | Price of the last eligible trade in the current bar interval                                                                                                                                                                           |
| LAST_SIZE        | long        | Size of the last eligible trade in the current bar interval                                                                                                                                                                            |
| LAST_TIME        | nsectime    | Timestamp of the last eligible trade in the current bar interval                                                                                                                                                                       |
| LOW              | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| LOW_SIZE         | long        | Size of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                     |
| LOW_TIME         | nsectime    | Timestamp of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| SELL_VOLUME      | long        | Traded volume originating from incoming sell orders. Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| TRADE_CURRENCY   | string[3]   | Currency in which a trade was executed.                                                                                                                                                                                                |
| TRADE_TICK_COUNT | long        | Number of eligible trades in the current bar interval                                                                                                                                                                                  |
| TWAP             | double      | TIme-weighted average price                                                                                                                                                                                                            |
| VOLUME           | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VWAP             | double      | Volume-weighted average price                                                                                                                                                                                                          |

### MILAN_BARS - TRD_1M

1-minute trade bars

#### MILAN_BARS - TRD_1M Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BUY_VOLUME       | long        | Traded volume originating from incoming buy orders.  Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| CLOUD_DB         | string[32]  | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.                                                                             |
| FIRST            | double      | Price of the first eligible trade in the current bar interval                                                                                                                                                                          |
| FIRST_SIZE       | long        | Size of the first eligible trade in the current bar interval                                                                                                                                                                           |
| FIRST_TIME       | nsectime    | Timestamp of the first eligible trade in the current bar interval                                                                                                                                                                      |
| HIGH             | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| HIGH_SIZE        | long        | Size of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                    |
| HIGH_TIME        | nsectime    | Timestamp of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                               |
| LAST             | double      | Price of the last eligible trade in the current bar interval                                                                                                                                                                           |
| LAST_SIZE        | long        | Size of the last eligible trade in the current bar interval                                                                                                                                                                            |
| LAST_TIME        | nsectime    | Timestamp of the last eligible trade in the current bar interval                                                                                                                                                                       |
| LOW              | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| LOW_SIZE         | long        | Size of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                     |
| LOW_TIME         | nsectime    | Timestamp of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| SELL_VOLUME      | long        | Traded volume originating from incoming sell orders. Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| TRADE_CURRENCY   | string[3]   | Currency in which a trade was executed.                                                                                                                                                                                                |
| TRADE_TICK_COUNT | long        | Number of eligible trades in the current bar interval                                                                                                                                                                                  |
| TWAP             | double      | TIme-weighted average price                                                                                                                                                                                                            |
| VOLUME           | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VWAP             | double      | Volume-weighted average price                                                                                                                                                                                                          |

### MILAN_BARS - VWAP_1H

1-hour VWAP bars

#### MILAN_BARS - VWAP_1H Table Schema

| Field    | Data Type   | Description                                                                                                                                                                                                                            |
|----------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOUD_DB | string[32]  | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.                                                                             |
| CURRENCY | string[64]  | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| OMDSEQ   | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| TWAP     | double      | TIme-weighted average price                                                                                                                                                                                                            |
| VOLUME   | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VWAP     | double      | Volume-weighted average price                                                                                                                                                                                                          |



## MILAN_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### MILAN_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### MILAN_DAILY - DAY Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOSE                  | double      | Closing price                                                                                                                                                                                                                          |
| CURRENCY               | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| HIGH                   | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW                    | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OFF_BOOK_VOLUME        | long        | Total volume traded off-book                                                                                                                                                                                                           |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN                   | double      | Open price for the current trading day                                                                                                                                                                                                 |
| TRADE_COUNT            | long        | Number of trades on the current trading day                                                                                                                                                                                            |
| TURNOVER               | double      | Total monetary value traded on the current trading day                                                                                                                                                                                 |
| VOLUME                 | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VOLUME_AUCTION         | long        | Volume traded during auctions. Includes all auction types.                                                                                                                                                                             |
| VOLUME_CLOSING_AUCTION | long        | Volume of the Closing Auction                                                                                                                                                                                                          |
| VOLUME_CONTINUOUS      | long        | Volume traded in the main orderbook during continuous trading                                                                                                                                                                          |
| VOLUME_DARK            | long        | Volume traded in a dark orderbook                                                                                                                                                                                                      |
| VOLUME_LIT             | long        | Volume traded in a lit orderbook                                                                                                                                                                                                       |
| VOLUME_OPENING_AUCTION | long        | Volume of the Opening Auction                                                                                                                                                                                                          |
| VOLUME_RFQ             | long        | Volume traded through an RFQ / RFC (Request for Quote / Request for Cross) process                                                                                                                                                     |
| VWAP                   | double      | Volume-weighted average price                                                                                                                                                                                                          |

### MILAN_DAILY - STAT

Static data, e.g. ISIN, description, security type

#### MILAN_DAILY - STAT Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CFI_CODE      | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                              |
| CURRENCY      | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| EXCH_SYMBOL   | string[20]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| ISIN          | string[12]  | ISIN code                                                                                                                                                                                                                              |
| LOT_SIZE      | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| MIC           | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| MKT_SEGMENT   | string[4]   | Market segment on which the instrument is traded                                                                                                                                                                                       |
| NAME          | string[100] | Description of the instrument                                                                                                                                                                                                          |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPERATING_MIC | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| SEC_TYPE      | string[40]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| TRADING_CODE  | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                               |



## MILAN_LATEST

Database includes the following tick types:

* TRD - Trades
* QTE - Best bid / offer quotes



### MILAN_LATEST - TRD

Trades

#### MILAN_LATEST - TRD Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                               |
|--------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME          | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                         |
| PRICE              | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross |
| SIZE               | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross          |
| TRADE_CURRENCY     | string[3]   | Currency in which a trade was executed.                                                                                                                                                                   |
| OPEN               | double      | Open price for the current trading day                                                                                                                                                                    |
| CLOSE              | double      | Closing price                                                                                                                                                                                             |
| CLOSE_DATE         | string[10]  | Date for Closing Price                                                                                                                                                                                    |
| LATENCY_LOAD       | long        | Latency in milliseconds for the time duration between data collection and in-memory database load                                                                                                         |
| LATENCY_COLLECTION | long        | Latency in milliseconds for the time duration between exchange publishing and data collection                                                                                                             |
| VOLUME             | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                         |
