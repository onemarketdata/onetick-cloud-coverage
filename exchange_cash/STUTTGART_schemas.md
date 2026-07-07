# Stuttgart Stock Exchange Schemas

Börse Stuttgart is the leading stock exchange for structured securities and corporate bond trading in Germany




## STUTTGART

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### STUTTGART - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### STUTTGART - DAY Table Schema

| Field   | Data Type   | Description                                                                                                                                                                                                                            |
|---------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOSE   | double      | Closing price                                                                                                                                                                                                                          |
| HIGH    | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW     | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OMDSEQ  | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN    | double      | Open price for the current trading day                                                                                                                                                                                                 |
| VOLUME  | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |

### STUTTGART - MKT

Market phase / instrument status information

#### STUTTGART - MKT Table Schema

| Field      | Data Type   | Description                                                                                                                                                                                                                            |
|------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME  | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| MKT_PHASE  | string[1]   | Indicates the instrument’s current market phase, as specified by the trading venue                                                                                                                                                     |
| OMDSEQ     | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OMD_STATUS | string[1]   | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |

### STUTTGART - QTE

Best bid / offer quotes

#### STUTTGART - QTE Table Schema

| Field     | Data Type   | Description                                                                                                                                                                                                                            |
|-----------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_PRICE | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE  | long        | Best ask size                                                                                                                                                                                                                          |
| BID_PRICE | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE  | long        | Best bid size                                                                                                                                                                                                                          |
| EXCH_TIME | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ    | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### STUTTGART - STAT

Static data, e.g. ISIN, description, security type

#### STUTTGART - STAT Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CFI_CODE      | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                              |
| CURRENCY      | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| EXCH_SYMBOL   | string[20]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| ISIN          | string[12]  | ISIN code                                                                                                                                                                                                                              |
| LOT_SIZE      | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| MIC           | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| MKT_SEGMENT   | string[25]  | Market segment on which the instrument is traded                                                                                                                                                                                       |
| NAME          | string[100] | Description of the instrument                                                                                                                                                                                                          |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPERATING_MIC | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| SEC_TYPE      | string[40]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| TRADING_CODE  | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                               |

### STUTTGART - TRD

Trades

#### STUTTGART - TRD Table Schema

| Field                 | Data Type   | Description                                                                                                                                                                                                                                       |
|-----------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AGGRESSOR_SIDE        | string[1]   | Indicates whether a trade resulted from an incoming buy or sell order.                                                                                                                                                                            |
| BOOK_TYPE             | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                                       |
| CLEARED               | string[1]   | Cleared                                                                                                                                                                                                                                           |
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
| SIZE                  | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                                  |
| TICK_STATUS           | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                                      |
| TRADE_CURRENCY        | string[3]   | Currency in which a trade was executed.                                                                                                                                                                                                           |
| TRADE_ID              | string[52]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                                |
| TRADE_PERIOD          | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                                  |
| TRADE_TYPE            | string[6]   | Type of trade                                                                                                                                                                                                                                     |
| TRADE_VENUE           | string[4]   | Identifies the venue where a trade was executed.   Typically a MIC, with the special values XOFF for off-exchange and SINT for Systematic Internaliser trades.                                                                                    |



## STUTTGART_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### STUTTGART_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### STUTTGART_DAILY - DAY Table Schema

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

### STUTTGART_DAILY - STAT

Static data, e.g. ISIN, description, security type

#### STUTTGART_DAILY - STAT Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CFI_CODE      | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                              |
| CURRENCY      | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| EXCH_SYMBOL   | string[20]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| ISIN          | string[12]  | ISIN code                                                                                                                                                                                                                              |
| LOT_SIZE      | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| MIC           | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| MKT_SEGMENT   | string[25]  | Market segment on which the instrument is traded                                                                                                                                                                                       |
| NAME          | string[100] | Description of the instrument                                                                                                                                                                                                          |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPERATING_MIC | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| SEC_TYPE      | string[40]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| TRADING_CODE  | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                               |
