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

| Field   | Data Type   | Description                                                                                                                                                                                                                            |
|---------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOSE   | double      | Closing price                                                                                                                                                                                                                          |
| HIGH    | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW     | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OMDSEQ  | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN    | double      | Open price for the current trading day                                                                                                                                                                                                 |
| VOLUME  | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |

### BIVA - MKT

Market phase / instrument status information

#### BIVA - MKT Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME      | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| MKT_PHASE      | string[4]   | Indicates the instrument’s current market phase, as specified by the trading venue                                                                                                                                                     |
| OMD_STATUS     | string[1]   | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| REASON_CODE    | string[1]   | Reason for an instrument status update                                                                                                                                                                                                 |
| TRADING_STATUS | string[4]   | Indicates whether the instrument is subject to a halt or suspension                                                                                                                                                                    |

### BIVA - QTE

Best bid / offer quotes

#### BIVA - QTE Table Schema

| Field     | Data Type   | Description                                                                                                                                                                                                                            |
|-----------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_PRICE | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE  | long        | Best ask size                                                                                                                                                                                                                          |
| BID_PRICE | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE  | long        | Best bid size                                                                                                                                                                                                                          |
| EXCH_TIME | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ    | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### BIVA - STAT

Static data, e.g. ISIN, description, security type

#### BIVA - STAT Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CFI_CODE        | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                              |
| CURRENCY        | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| EXCH_SYMBOL     | string[20]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| EXPIRATION_DATE | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                              |
| ISIN            | string[12]  | ISIN code                                                                                                                                                                                                                              |
| LISTING_STATUS  | string[20]  | Free text field identifying the instrument’s listing status, e.g. Listed, Admitted to Trading, Delisted                                                                                                                                |
| LOT_SIZE        | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| MIC             | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| MIN_ORDER_SIZE  | long        | Minimum order size                                                                                                                                                                                                                     |
| MKT_SEGMENT     | string[8]   | Market segment on which the instrument is traded                                                                                                                                                                                       |
| NAME            | string[100] | Description of the instrument                                                                                                                                                                                                          |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPERATING_MIC   | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| SEC_TYPE        | string[40]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| TICK_SIZE       | string[80]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                             |
| TICK_SIZE_TYPE  | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                   |
| TRADING_CODE    | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                               |

### BIVA - TRD

Trades

#### BIVA - TRD Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AGGRESSOR_SIDE | string[1]   | Indicates whether a trade resulted from an incoming buy or sell order.                                                                                                                                                                 |
| BOOK_TYPE      | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                            |
| BUYER          | string[8]   | ID of the market participant on the buy side of a trade                                                                                                                                                                                |
| DELETED_TIME   | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| EXCH_TIME      | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE          | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SELLER         | string[8]   | ID of the market participant on the sell side of a trade                                                                                                                                                                               |
| SIZE           | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| TICK_STATUS    | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| TRADE_ID       | string[24]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| TRADE_PERIOD   | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                       |
| TRADE_TYPE     | string[4]   | Type of trade                                                                                                                                                                                                                          |



## BIVA_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### BIVA_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### BIVA_DAILY - DAY Table Schema

| Field   | Data Type   | Description                                                                                                                                                                                                                            |
|---------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOSE   | double      | Closing price                                                                                                                                                                                                                          |
| HIGH    | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW     | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OMDSEQ  | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN    | double      | Open price for the current trading day                                                                                                                                                                                                 |
| VOLUME  | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |

### BIVA_DAILY - STAT

Static data, e.g. ISIN, description, security type

