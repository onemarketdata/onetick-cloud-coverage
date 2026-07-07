# B3 (Bovespa) - OTC Market Schemas

The São Paulo Stock, Commodities and Futures Exchange (known as B3 S.A. - Brasil, Bolsa,balcão) currently has several different trading market segments: the traditional stock exchange and over-the-counter markets, and the special trading segments Level 1, Level 2 and New Market (Novo Mercado), Bovespa Mais and Bovespa Mais Level 2, which allow the trading of securities of listed companies adopting a special level of corporate governance.




## BRAZIL_OTC

Database includes the following tick types:

* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades
* TRD_ODD_LOT - Trades from the odd lot book



### BRAZIL_OTC - IND

Indicative pricing, e.g. indicative auction prices and imbalance

#### BRAZIL_OTC - IND Table Schema

| Field        | Data Type   | Description                                                                                                                                                                                                                            |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AUCTION_TYPE | string[1]   | Type of auction from which an indicative auction price / auction imbalance originates.                                                                                                                                                 |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE        | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE         | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |

### BRAZIL_OTC - MKT

Market phase / instrument status information

#### BRAZIL_OTC - MKT Table Schema

| Field      | Data Type   | Description                                                                                                                                                                                                                            |
|------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MKT_PHASE  | string[4]   | Indicates the instrument’s current market phase, as specified by the trading venue                                                                                                                                                     |
| OMD_STATUS | string[1]   | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| OMDSEQ     | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### BRAZIL_OTC - QTE

Best bid / offer quotes

#### BRAZIL_OTC - QTE Table Schema

| Field     | Data Type   | Description                                                                                                                                                                                                                            |
|-----------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_PRICE | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE  | long        | Best ask size                                                                                                                                                                                                                          |
| BID_PRICE | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE  | long        | Best bid size                                                                                                                                                                                                                          |
| OMDSEQ    | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### BRAZIL_OTC - STAT

Static data, e.g. ISIN, description, security type

#### BRAZIL_OTC - STAT Table Schema

| Field             | Data Type   | Description                                                                                                                                                                                                                            |
|-------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BBG_TICKER        | string[40]  | Bloomberg ticker symbol                                                                                                                                                                                                                |
| COMPOSITE_FIGI    | string[12]  | Country-composite FIGI, identifying a security across all venues in a particular country                                                                                                                                               |
| CONTRACT_SIZE     | double      | Indicates a derivative’s underlying quantity                                                                                                                                                                                           |
| CURRENCY          | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| EXCH_SYMBOL       | string[20]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| EXERCISE_TYPE     | string[1]   | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)                                                                                                                                                             |
| EXPIRATION_DATE   | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                              |
| FIGI              | string[12]  | Financial Instrument Global Identifier, identifying an individual instrument traded on a specific venue                                                                                                                                |
| ISIN              | string[12]  | ISIN code                                                                                                                                                                                                                              |
| LOT_SIZE          | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| MIC               | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| NAME              | string[120] | Description of the instrument                                                                                                                                                                                                          |
| OMDSEQ            | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPERATING_MIC     | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| RTS_SYMBOL        | string[32]  | Ticker symbol used by ICE Data Services                                                                                                                                                                                                |
| SEC_TYPE          | string[25]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| SEDOL             | string[7]   | SEDOL code                                                                                                                                                                                                                             |
| STRIKE_PRICE      | double      | Exercise price for options / warrants                                                                                                                                                                                                  |
| TICK_SIZE         | string[100] | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                             |
| TICK_SIZE_TYPE    | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                   |
| UNDERLYING_SYMBOL | string[40]  | Symbol of the underlying instrument                                                                                                                                                                                                    |

### BRAZIL_OTC - TRD

Trades

#### BRAZIL_OTC - TRD Table Schema

| Field        | Data Type   | Description                                                                                                                                                                                                                            |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BOOK_TYPE    | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                            |
| BUYER        | string[6]   | ID of the market participant on the buy side of a trade                                                                                                                                                                                |
| DELETED_TIME | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| EXCH_TIME    | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE        | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SELLER       | string[6]   | ID of the market participant on the sell side of a trade                                                                                                                                                                               |
| SIZE         | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| TICK_STATUS  | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| TRADE_PERIOD | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                       |
| TRADE_TYPE   | string[6]   | Type of trade                                                                                                                                                                                                                          |

### BRAZIL_OTC - TRD_ODD_LOT

Trades from the odd lot book

#### BRAZIL_OTC - TRD_ODD_LOT Table Schema

| Field        | Data Type   | Description                                                                                                                                                                                                                            |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BOOK_TYPE    | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                            |
| BUYER        | string[6]   | ID of the market participant on the buy side of a trade                                                                                                                                                                                |
| DELETED_TIME | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| EXCH_TIME    | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE        | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SELLER       | string[6]   | ID of the market participant on the sell side of a trade                                                                                                                                                                               |
| SIZE         | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| TICK_STATUS  | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| TRADE_PERIOD | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                       |
| TRADE_TYPE   | string[6]   | Type of trade                                                                                                                                                                                                                          |
