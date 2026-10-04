# Nextrade ATS Schemas

Nextrade (NXT) is South Korea’s first licensed Alternative Trading System (ATS), operating alongside the traditional Korea Exchange.




## NEXTRADE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### NEXTRADE - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### NEXTRADE - DAY Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME            | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP              | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
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
| OFF_BOOK_VOLUME        | long        | Total volume traded off-book                                                                                                                                                                                                           |
| VOLUME_CONTINUOUS      | long        | Volume traded in the main orderbook during continuous trading                                                                                                                                                                          |
| VOLUME_AUCTION         | long        | Volume traded during auctions. Includes all auction types.                                                                                                                                                                             |
| VOLUME_OPENING_AUCTION | long        | Volume of the Opening Auction                                                                                                                                                                                                          |
| VOLUME_CLOSING_AUCTION | long        | Volume of the Closing Auction                                                                                                                                                                                                          |
| VOLUME_PRE_MARKET      | long        | Volume of the Pre-Market Trading Session                                                                                                                                                                                               |
| VOLUME_POST_MARKET     | long        | Volume of the Post-Market Trading Session                                                                                                                                                                                              |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### NEXTRADE - IND

Indicative pricing, e.g. indicative auction prices and imbalance

#### NEXTRADE - IND Table Schema

| Field        | Data Type   | Description                                                                                                                                                                                                                            |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME  | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP    | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME    | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| PRICE        | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE         | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| AUCTION_TYPE | string[1]   | Type of auction from which an indicative auction price / auction imbalance originates.                                                                                                                                                 |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### NEXTRADE - MKT

Market phase / instrument status information

#### NEXTRADE - MKT Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME   | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| MKT_PHASE   | string[8]   | Indicates the instrument’s current market phase, as specified by the trading venue                                                                                                                                                     |
| OMD_STATUS  | string[1]   | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### NEXTRADE - QTE

Best bid / offer quotes

#### NEXTRADE - QTE Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME   | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| BID_PRICE   | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE    | long        | Best bid size                                                                                                                                                                                                                          |
| ASK_PRICE   | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE    | long        | Best ask size                                                                                                                                                                                                                          |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### NEXTRADE - STAT

Static data, e.g. ISIN, description, security type

#### NEXTRADE - STAT Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME    | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP      | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| NAME           | string[160] | Description of the instrument                                                                                                                                                                                                          |
| ISIN           | string[12]  | ISIN code                                                                                                                                                                                                                              |
| EXCH_SYMBOL    | string[40]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| TRADING_CODE   | string[40]  | ID used to identify the instrument in the trading system                                                                                                                                                                               |
| MIC            | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| OPERATING_MIC  | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| PRIMARY_MIC    | string[4]   | MIC of the instrument’s primary listing market, or the reference market for instruments traded on an MTF                                                                                                                               |
| SEC_TYPE       | string[40]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| CFI_CODE       | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                              |
| CURRENCY       | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| LOT_SIZE       | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| TICK_SIZE_TYPE | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                   |
| TICK_SIZE      | string[200] | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                             |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### NEXTRADE - TRD

Trades

#### NEXTRADE - TRD Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME    | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP      | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME      | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| PRICE          | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE           | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| AGGRESSOR_SIDE | string[1]   | Indicates whether a trade resulted from an incoming buy or sell order.                                                                                                                                                                 |
| TRADE_TYPE     | string[8]   | Type of trade                                                                                                                                                                                                                          |
| TRADE_PERIOD   | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                       |
| BOOK_TYPE      | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                            |
| TRADE_ID       | string[20]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| DELETED_TIME   | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS    | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |



## NEXTRADE_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### NEXTRADE_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### NEXTRADE_DAILY - DAY Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME            | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP              | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
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
| OFF_BOOK_VOLUME        | long        | Total volume traded off-book                                                                                                                                                                                                           |
| VOLUME_CONTINUOUS      | long        | Volume traded in the main orderbook during continuous trading                                                                                                                                                                          |
| VOLUME_AUCTION         | long        | Volume traded during auctions. Includes all auction types.                                                                                                                                                                             |
| VOLUME_OPENING_AUCTION | long        | Volume of the Opening Auction                                                                                                                                                                                                          |
| VOLUME_CLOSING_AUCTION | long        | Volume of the Closing Auction                                                                                                                                                                                                          |
| VOLUME_PRE_MARKET      | long        | Volume of the Pre-Market Trading Session                                                                                                                                                                                               |
| VOLUME_POST_MARKET     | long        | Volume of the Post-Market Trading Session                                                                                                                                                                                              |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### NEXTRADE_DAILY - STAT

Static data, e.g. ISIN, description, security type

#### NEXTRADE_DAILY - STAT Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME    | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP      | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| NAME           | string[160] | Description of the instrument                                                                                                                                                                                                          |
| ISIN           | string[12]  | ISIN code                                                                                                                                                                                                                              |
| EXCH_SYMBOL    | string[40]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| TRADING_CODE   | string[40]  | ID used to identify the instrument in the trading system                                                                                                                                                                               |
| MIC            | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| OPERATING_MIC  | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| PRIMARY_MIC    | string[4]   | MIC of the instrument’s primary listing market, or the reference market for instruments traded on an MTF                                                                                                                               |
| SEC_TYPE       | string[40]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| CFI_CODE       | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                              |
| CURRENCY       | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| LOT_SIZE       | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| TICK_SIZE_TYPE | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                   |
| TICK_SIZE      | string[200] | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                             |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
