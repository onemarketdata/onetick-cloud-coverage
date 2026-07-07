# The Nasdaq Schemas

The Nasdaq is an American multinational financial services corporation that operates the world’s second-largest stock exchange by market capitalization




## NASDAQ

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* MM_STATUS - Information on the market makers registered in each security
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* TRD - Trades



### NASDAQ - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### NASDAQ - DAY Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOSE                  | double      | Closing price                                                                                                                                                                                                                          |
| HIGH                   | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW                    | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN                   | double      | Open price for the current trading day                                                                                                                                                                                                 |
| PRICE_CLOSING_AUCTION  | double      | Price of the Closing Auction                                                                                                                                                                                                           |
| PRICE_OPENING_AUCTION  | double      | Price of the Opening Auction                                                                                                                                                                                                           |
| TRADE_COUNT            | long        | Number of trades on the current trading day                                                                                                                                                                                            |
| TRADE_VALUE            | double      | Total monetary value traded on the current trading day                                                                                                                                                                                 |
| UPDATE_TYPE            | string[16]  | Type of update                                                                                                                                                                                                                         |
| VOLUME                 | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VOLUME_AUCTION         | long        | Volume traded during auctions. Includes all auction types.                                                                                                                                                                             |
| VOLUME_CLOSING_AUCTION | long        | Volume of the Closing Auction                                                                                                                                                                                                          |
| VOLUME_CONTINUOUS      | long        | Volume traded in the main orderbook during continuous trading                                                                                                                                                                          |
| VOLUME_DARK            | long        | Volume traded in a dark orderbook                                                                                                                                                                                                      |
| VOLUME_HIDDEN          | long        | Volume traded against hidden orders in a lit orderbook                                                                                                                                                                                 |
| VOLUME_LIT             | long        | Volume traded in a lit orderbook                                                                                                                                                                                                       |
| VOLUME_MAIN_SESSION    | long        | Volume of the Main Trading Session                                                                                                                                                                                                     |
| VOLUME_ODD_LOT         | long        | Volume of the Odd Lot Trades                                                                                                                                                                                                           |
| VOLUME_OPENING_AUCTION | long        | Volume of the Opening Auction                                                                                                                                                                                                          |
| VOLUME_POST_MARKET     | long        | Volume of the Post-Market Trading Session                                                                                                                                                                                              |
| VOLUME_PRE_MARKET      | long        | Volume of the Pre-Market Trading Session                                                                                                                                                                                               |
| VOLUME_ROUND_LOT       | long        | Volume of Round Lot Trades                                                                                                                                                                                                             |
| VWAP                   | double      | Volume-weighted average price                                                                                                                                                                                                          |

### NASDAQ - IND

Indicative pricing, e.g. indicative auction prices and imbalance

#### NASDAQ - IND Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                                                            |
|---------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AUCTION_BOOK_PRICE  | double      | Theoretical auction price calculated using auction-only orders (i.e. excluding orders in the continuous book)                                                                                                                          |
| AUCTION_TYPE        | string[1]   | Type of auction from which an indicative auction price / auction imbalance originates.                                                                                                                                                 |
| EXCH_TIME           | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| IMB_SIDE            | string[1]   | Indicates if one side of the orderbook has excess executable orders during an auction phase.                                                                                                                                           |
| IMB_VOLUME          | long        | Size of an auction imbalance, i.e. the excess volume of orders on the side indicated by IMB_SIDE                                                                                                                                       |
| OMDSEQ              | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE               | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| PRICE_VARIATION_IND | string[1]   | > Indicates the difference between the indicative auction price (Near price) and the instrument’s reference price in the continuous book.                                                                                              |
| REF_PRICE           | double      | Reference price according to which the auction price limits are set - usually the mid of the BBO, or the last sale price                                                                                                               |
| SIZE                | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |

### NASDAQ - LULD

Limit Up / Limit Down price levels

#### NASDAQ - LULD Table Schema

| Field      | Data Type   | Description                                                                                                                                                                                                                            |
|------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME  | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| HIGH_LIMIT | double      | Upper trading limit / circuit breaker level                                                                                                                                                                                            |
| LOW_LIMIT  | double      | Lower trading limit / circuit breaker level                                                                                                                                                                                            |
| OMDSEQ     | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### NASDAQ - MKT

Market phase / instrument status information

#### NASDAQ - MKT Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME              | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| MKT_PHASE              | string[1]   | Indicates the instrument’s current market phase, as specified by the trading venue                                                                                                                                                     |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OMD_STATUS             | string[1]   | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| REASON_CODE            | string[4]   | Reason for an instrument status update                                                                                                                                                                                                 |
| SCHEDULED_EVENT_TIME   | nsectime    | Time when an event is due to take place (e.g. if the status update refers to an auction call phase, this indicates when the auction cross will occur)                                                                                  |
| SESSION                | string[12]  | Trading session to which the update relates, e.g. Day, Night, T, T+1                                                                                                                                                                   |
| SHORT_SALE_RESTRICTION | string[1]   | Indicates whether short selling is permitted                                                                                                                                                                                           |

### NASDAQ - MM_STATUS

Information on the market makers registered in each security

#### NASDAQ - MM_STATUS Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME     | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| IS_PRIMARY_MM | string[1]   | Indicates whether the participant identified by PART_ID is a primary market maker in the security (Y - Yes, N - No)                                                                                                                    |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PART_ID       | string[4]   | Identifies the market participant that entered an order / quote                                                                                                                                                                        |
| PART_STATUS   | string[1]   | Status of the market participant identified by PART_ID.                                                                                                                                                                                |
| PART_TYPE     | string[1]   | Indicates the type of market participant identified by PART_ID                                                                                                                                                                         |

### NASDAQ - PRL_FULL

Full orderbook data, showing updates to each individual order (MBO)

#### NASDAQ - PRL_FULL Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                                                                   |
|--------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BUY_SELL_FLAG      | int         | Orderbook side (0 - Buy, 1 - Sell)                                                                                                                                                                                                            |
| DELETED_TIME       | nsectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                              |
| EXCH_TIME          | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                             |
| FILL_PRICE         | double      | Price at which the order was executed                                                                                                                                                                                                         |
| FILL_SIZE          | int         | Size filled in an order execution event                                                                                                                                                                                                       |
| OLD_ORDER_ID       | string[20]  | Previous order ID, where a modification results in a new order ID being issued                                                                                                                                                                |
| OLD_ORDER_POSITION | int         | Indicates the order’s position in the order queue before the orderbook update was applied. e.g. if set to 1, this indicates that the order was at the front of the order queue before the orderbook update. Always 0 for new orders.          |
| OLD_PRICE          | double      | Previous price of an order                                                                                                                                                                                                                    |
| OLD_PRICE_LEVEL    | int         | Price level of the order before the orderbook update was applied. e.g. if set to 3, this indicates that the order was at the third best price point before the orderbook update. Always set to 0 for new orders.                              |
| OLD_SIZE           | int         | Previous size of an order                                                                                                                                                                                                                     |
| OMDSEQ             | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.        |
| ORDER_ID           | string[20]  | Order identifier, uniquely identifying an order at any given point in time.   Uniqueness depends on the exchange - e.g. may be globally unique, or unique per trading day, or per instrument per trading day.                                 |
| ORDER_POSITION     | int         | Indicates the order’s position in the order queue after the orderbook update is applied. e.g. if set to 1, this indicates that the order is at the front of the order queue after the orderbook update.  Always set to 0 for order deletions. |
| ORDER_TYPE         | string[1]   | Type of order.                                                                                                                                                                                                                                |
| ORIGINAL_ORDER_ID  | string[20]  | Order ID by which the order was identified when it was first entered.  Some markets issue a new order ID when orders are modified. Using this field, these orders can be tracked using their original order ID.                               |
| PART_ID            | string[4]   | Identifies the market participant that entered an order / quote                                                                                                                                                                               |
| PRICE              | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                                     |
| PRICE_LEVEL        | int         | Price level of the order after the orderbook update is applied.  e.g. if set to 3, this indicates that the order is at the third best price point after the orderbook update.  Always set to 0 for order deletions.                           |
| RECORD_TYPE        | string[1]   | Type of depth update.                                                                                                                                                                                                                         |
| SIZE               | int         | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                              |
| SIZE_AHEAD         | long        | Total order volume ahead of the order in the order queue, after the order update is applied. Always 0 for order deletions.                                                                                                                    |
| TICK_STATUS        | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                                  |
| TIME_PRIORITY      | long        | Time priority of an order in the order queue.  If two standard orders on the same side have the same price, the one with the lower value of TIME_PRIORITY will be executed first.                                                             |
| TRADE_ID           | string[16]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                            |
| UPDATE_TYPE        | string[1]   | Type of update                                                                                                                                                                                                                                |

### NASDAQ - QTE

Best bid / offer quotes

#### NASDAQ - QTE Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_NUM_ORDERS | int         | Number of orders at the best ask price                                                                                                                                                                                                 |
| ASK_PRICE      | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE       | int         | Best ask size                                                                                                                                                                                                                          |
| BID_NUM_ORDERS | int         | Number of orders at the best bid price                                                                                                                                                                                                 |
| BID_PRICE      | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE       | int         | Best bid size                                                                                                                                                                                                                          |
| EXCH_TIME      | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| RPI            | string[1]   | Indicates the presence of Retail Price Improvement interest on bid and/or ask side                                                                                                                                                     |

### NASDAQ - TRD
