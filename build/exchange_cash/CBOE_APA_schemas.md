# Cboe Europe Trade Reporting Schemas

Cboe Europe Trade Reporting allows firms to report off-order book trades in European equities to comply with MiFID II trade reporting obligations.




## CBOE_APA

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### CBOE_APA - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### CBOE_APA - DAY Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME            | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP              | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| CURRENCY               | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| OPEN                   | double      | Open price for the current trading day                                                                                                                                                                                                 |
| HIGH                   | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW                    | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| CLOSE                  | double      | Closing price                                                                                                                                                                                                                          |
| VOLUME                 | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| TRADE_COUNT            | long        | Number of trades on the current trading day                                                                                                                                                                                            |
| TURNOVER               | double      | Total monetary value traded on the current trading day. Note: The value will typically be rounded to the nearest integer.                                                                                                              |
| VWAP                   | double      | Volume-weighted average price                                                                                                                                                                                                          |
| VOLUME_LIT             | long        | Volume traded in a lit orderbook                                                                                                                                                                                                       |
| VOLUME_DARK            | long        | Volume traded in a dark orderbook                                                                                                                                                                                                      |
| OFF_BOOK_VOLUME        | long        | Total volume traded off-book                                                                                                                                                                                                           |
| VOLUME_RFQ             | long        | Volume traded through an RFQ / RFC (Request for Quote / Request for Cross) process                                                                                                                                                     |
| VOLUME_CONTINUOUS      | long        | Volume traded in the main orderbook during continuous trading                                                                                                                                                                          |
| VOLUME_AUCTION         | long        | Volume traded during auctions. Includes all auction types.                                                                                                                                                                             |
| VOLUME_OPENING_AUCTION | long        | Volume of the Opening Auction                                                                                                                                                                                                          |
| VOLUME_CLOSING_AUCTION | long        | Volume of the Closing Auction                                                                                                                                                                                                          |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### CBOE_APA - STAT

Static data, e.g. ISIN, description, security type

#### CBOE_APA - STAT Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME   | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP     | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| NAME          | string[100] | Description of the instrument                                                                                                                                                                                                          |
| ISIN          | string[12]  | ISIN code                                                                                                                                                                                                                              |
| EXCH_SYMBOL   | string[20]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| TRADING_CODE  | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                               |
| MIC           | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| OPERATING_MIC | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| PRIMARY_MIC   | string[4]   | MIC of the instrument’s primary listing market, or the reference market for instruments traded on an MTF                                                                                                                               |
| SEC_TYPE      | string[40]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| CFI_CODE      | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                              |
| MKT_SEGMENT   | string[8]   | Market segment on which the instrument is traded                                                                                                                                                                                       |
| CURRENCY      | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| LOT_SIZE      | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### CBOE_APA - TRD

Trades

#### CBOE_APA - TRD Table Schema

| Field                 | Data Type   | Description                                                                                                                                                                                                                                       |
|-----------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME           | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                                    |
| TIMESTAMP             | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                           |
| EXCH_TIME             | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                                 |
| PRICE                 | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                                         |
| SIZE                  | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                                  |
| AGGRESSOR_SIDE        | string[1]   | Indicates whether a trade resulted from an incoming buy or sell order.                                                                                                                                                                            |
| TRADE_TYPE            | string[6]   | Type of trade                                                                                                                                                                                                                                     |
| TRADE_VENUE           | string[4]   | Identifies the venue where a trade was executed.   Typically a MIC, with the special values XOFF for off-exchange and SINT for Systematic Internaliser trades.                                                                                    |
| PUB_VENUE             | string[4]   | Venue (MIC) used to publish an off-exchange trade                                                                                                                                                                                                 |
| TRADE_CURRENCY        | string[3]   | Currency in which a trade was executed.                                                                                                                                                                                                           |
| TRADE_PERIOD          | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                                  |
| BOOK_TYPE             | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                                       |
| LATE_REPORTED         | string[1]   | Indicates whether a trade was reported late and/or outside normal trading hours                                                                                                                                                                   |
| MMT_MKT_MECH          | string[1]   | Market mechanism through which a trade was executed.                                                                                                                                                                                              |
| MMT_TRD_MODE          | string[1]   | Trading period during which an on-book trade was executed, or origin of an off-book trade report (on-exchange / off-exchange / SI).                                                                                                               |
| MMT_TRANS_CAT         | string[1]   | Identifies various special categories of trade.                                                                                                                                                                                                   |
| MMT_NEGOTIATED_IND    | string[1]   | Indicates privately negotiated trades, or Systematic Internaliser trades exempt from pre-trade transparency.                                                                                                                                      |
| MMT_CROSS_IND         | string[1]   | Identifies agency cross trades, where a broker crossed two client orders outside the order book.                                                                                                                                                  |
| MMT_MOD_IND           | string[1]   | Identifies trade cancellations, or amendments of a previous trade.                                                                                                                                                                                |
| MMT_BENCHMARK_IND     | string[1]   | Identifies whether a trade was priced according to a defined benchmark (e.g. VWAP) or reference price (e.g. midpoint of the primary market BBO), or whether it was part of a trade in multiple instruments (contingent trade or portfolio trade). |
| MMT_DIVIDEND_IND      | string[1]   | Identifies whether a trade includes special dividend arrangements, e.g. a trade sold cum-dividend during an ex-dividend period.                                                                                                                   |
| MMT_OFF_BOOK_AUTO_IND | string[1]   | Identifies whether an off-book trade report was executed via a manual or automated process.                                                                                                                                                       |
| MMT_PRICE_FORMING_IND | string[1]   | Identifies whether a trade is price-forming, or contributes to the price discovery process.                                                                                                                                                       |
| MMT_ALGO_IND          | string[1]   | Identifies whether a trade involved an algorithmic order.                                                                                                                                                                                         |
| MMT_PUB_MODE          | string[1]   | Identifies whether a trade was subject to delayed publication, and the reason for the deferral.                                                                                                                                                   |
| MMT_DEFERRAL_TYPE     | string[1]   | Type of publication deferral or subsequent enrichment applied to a trade report.                                                                                                                                                                  |
| MMT_DUP_IND           | string[1]   | Identifies trades reported to more than one Approved Publication Arrangement.                                                                                                                                                                     |
| TRADE_ID              | string[20]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                                |
| DELETED_TIME          | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                                  |
| TICK_STATUS           | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                                      |
| OMDSEQ                | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.            |



## CBOE_APA_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### CBOE_APA_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### CBOE_APA_DAILY - DAY Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME            | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP              | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| CURRENCY               | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| OPEN                   | double      | Open price for the current trading day                                                                                                                                                                                                 |
| HIGH                   | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW                    | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| CLOSE                  | double      | Closing price                                                                                                                                                                                                                          |
| VOLUME                 | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| TRADE_COUNT            | long        | Number of trades on the current trading day                                                                                                                                                                                            |
| TURNOVER               | double      | Total monetary value traded on the current trading day. Note: The value will typically be rounded to the nearest integer.                                                                                                              |
| VWAP                   | double      | Volume-weighted average price                                                                                                                                                                                                          |
| VOLUME_LIT             | long        | Volume traded in a lit orderbook                                                                                                                                                                                                       |
| VOLUME_DARK            | long        | Volume traded in a dark orderbook                                                                                                                                                                                                      |
| OFF_BOOK_VOLUME        | long        | Total volume traded off-book                                                                                                                                                                                                           |
| VOLUME_RFQ             | long        | Volume traded through an RFQ / RFC (Request for Quote / Request for Cross) process                                                                                                                                                     |
| VOLUME_CONTINUOUS      | long        | Volume traded in the main orderbook during continuous trading                                                                                                                                                                          |
| VOLUME_AUCTION         | long        | Volume traded during auctions. Includes all auction types.                                                                                                                                                                             |
| VOLUME_OPENING_AUCTION | long        | Volume of the Opening Auction                                                                                                                                                                                                          |
| VOLUME_CLOSING_AUCTION | long        | Volume of the Closing Auction                                                                                                                                                                                                          |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### CBOE_APA_DAILY - STAT

Static data, e.g. ISIN, description, security type

#### CBOE_APA_DAILY - STAT Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME   | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP     | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| NAME          | string[100] | Description of the instrument                                                                                                                                                                                                          |
| ISIN          | string[12]  | ISIN code                                                                                                                                                                                                                              |
| EXCH_SYMBOL   | string[20]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| TRADING_CODE  | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                               |
| MIC           | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| OPERATING_MIC | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| PRIMARY_MIC   | string[4]   | MIC of the instrument’s primary listing market, or the reference market for instruments traded on an MTF                                                                                                                               |
| SEC_TYPE      | string[40]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| CFI_CODE      | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                              |
| MKT_SEGMENT   | string[8]   | Market segment on which the instrument is traded                                                                                                                                                                                       |
| CURRENCY      | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| LOT_SIZE      | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
