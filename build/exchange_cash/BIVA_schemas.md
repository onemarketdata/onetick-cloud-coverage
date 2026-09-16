# BIVA (Bolsa Institucional de Valores) Schemas

The Institutional Stock Exchange, commonly known as BIVA, is Mexico’s second stock exchange, based in Mexico City. BIVA began operations on 25 July 2018 and trades the same instruments as the other exchange in Mexico, the Bolsa Mexicana de Valores: equities, debts, warrants and some Mexican-specific instruments such as CKDs and FIBRAs.




## BIVA

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### BIVA - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### BIVA - DAY Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| OPEN        | double      | Open price for the current trading day                                                                                                                                                                                                 |
| HIGH        | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW         | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| CLOSE       | double      | Closing price                                                                                                                                                                                                                          |
| VOLUME      | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### BIVA - MKT

Market phase / instrument status information

#### BIVA - MKT Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME    | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP      | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME      | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| TRADING_STATUS | string[4]   | Indicates whether the instrument is subject to a halt or suspension                                                                                                                                                                    |
| MKT_PHASE      | string[4]   | Indicates the instrument’s current market phase, as specified by the trading venue                                                                                                                                                     |
| REASON_CODE    | string[1]   | Reason for an instrument status update                                                                                                                                                                                                 |
| OMD_STATUS     | string[1]   | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### BIVA - QTE

Best bid / offer quotes

#### BIVA - QTE Table Schema

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

### BIVA - STAT

Static data, e.g. ISIN, description, security type

#### BIVA - STAT Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME     | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP       | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| NAME            | string[100] | Description of the instrument                                                                                                                                                                                                          |
| ISIN            | string[12]  | ISIN code                                                                                                                                                                                                                              |
| EXCH_SYMBOL     | string[20]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| TRADING_CODE    | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                               |
| MIC             | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| OPERATING_MIC   | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| SEC_TYPE        | string[40]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| CFI_CODE        | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                              |
| MKT_SEGMENT     | string[8]   | Market segment on which the instrument is traded                                                                                                                                                                                       |
| LISTING_STATUS  | string[20]  | Free text field identifying the instrument’s listing status, e.g. Listed, Admitted to Trading, Delisted                                                                                                                                |
| CURRENCY        | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| EXPIRATION_DATE | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                              |
| LOT_SIZE        | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| MIN_ORDER_SIZE  | long        | Minimum order size                                                                                                                                                                                                                     |
| TICK_SIZE_TYPE  | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                   |
| TICK_SIZE       | string[80]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                             |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### BIVA - TRD

Trades

#### BIVA - TRD Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME    | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP      | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME      | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| PRICE          | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE           | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| BUYER          | string[8]   | ID of the market participant on the buy side of a trade                                                                                                                                                                                |
| SELLER         | string[8]   | ID of the market participant on the sell side of a trade                                                                                                                                                                               |
| AGGRESSOR_SIDE | string[1]   | Indicates whether a trade resulted from an incoming buy or sell order.                                                                                                                                                                 |
| TRADE_TYPE     | string[4]   | Type of trade                                                                                                                                                                                                                          |
| TRADE_PERIOD   | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                       |
| BOOK_TYPE      | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                            |
| TRADE_ID       | string[24]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| DELETED_TIME   | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS    | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |



## BIVA_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### BIVA_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### BIVA_DAILY - DAY Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| OPEN        | double      | Open price for the current trading day                                                                                                                                                                                                 |
| HIGH        | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW         | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| CLOSE       | double      | Closing price                                                                                                                                                                                                                          |
| VOLUME      | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### BIVA_DAILY - STAT

Static data, e.g. ISIN, description, security type

#### BIVA_DAILY - STAT Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME     | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP       | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| NAME            | string[100] | Description of the instrument                                                                                                                                                                                                          |
| ISIN            | string[12]  | ISIN code                                                                                                                                                                                                                              |
| EXCH_SYMBOL     | string[20]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| TRADING_CODE    | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                               |
| MIC             | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| OPERATING_MIC   | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| SEC_TYPE        | string[40]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| CFI_CODE        | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                              |
| MKT_SEGMENT     | string[8]   | Market segment on which the instrument is traded                                                                                                                                                                                       |
| LISTING_STATUS  | string[20]  | Free text field identifying the instrument’s listing status, e.g. Listed, Admitted to Trading, Delisted                                                                                                                                |
| CURRENCY        | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| EXPIRATION_DATE | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                              |
| LOT_SIZE        | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| MIN_ORDER_SIZE  | long        | Minimum order size                                                                                                                                                                                                                     |
| TICK_SIZE_TYPE  | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                   |
| TICK_SIZE       | string[80]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                             |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
