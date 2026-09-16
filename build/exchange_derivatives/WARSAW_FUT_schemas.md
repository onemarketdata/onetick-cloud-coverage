# Warsaw Stock Exchange - Derivatives Schemas

Warsaw Stock Exchange operates a financial instruments exchange. The Exchange trades equities, fixed income, derivatives, listings, bonds, subscription rights.




## WARSAW_FUT

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### WARSAW_FUT - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### WARSAW_FUT - DAY Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME   | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP     | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| UPDATE_TYPE   | string[16]  | Type of update                                                                                                                                                                                                                         |
| OPEN          | double      | Open price for the current trading day                                                                                                                                                                                                 |
| HIGH          | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW           | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| CLOSE         | double      | Closing price                                                                                                                                                                                                                          |
| SETTLE_PRICE  | double      | Settlement price                                                                                                                                                                                                                       |
| SETTLE_DATE   | string[8]   | Trading date to which the settlement price relates (YYYYMMDD)                                                                                                                                                                          |
| VOLUME        | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| OPEN_INT      | double      | Open interest for futures / options                                                                                                                                                                                                    |
| OPEN_INT_DATE | string[8]   | Trading date to which the open interest relates (YYYYMMDD)                                                                                                                                                                             |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### WARSAW_FUT - IND

Indicative pricing, e.g. indicative auction prices and imbalance

#### WARSAW_FUT - IND Table Schema

| Field        | Data Type   | Description                                                                                                                                                                                                                            |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME  | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP    | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME    | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| PRICE        | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE         | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| AUCTION_TYPE | string[1]   | Type of auction from which an indicative auction price / auction imbalance originates.                                                                                                                                                 |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### WARSAW_FUT - LULD

Limit Up / Limit Down price levels

#### WARSAW_FUT - LULD Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME   | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| HIGH_LIMIT  | double      | Upper trading limit / circuit breaker level                                                                                                                                                                                            |
| LOW_LIMIT   | double      | Lower trading limit / circuit breaker level                                                                                                                                                                                            |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### WARSAW_FUT - MKT

Market phase / instrument status information

#### WARSAW_FUT - MKT Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                                                            |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME        | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP          | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME          | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| MKT_PHASE          | string[6]   | Indicates the instrument’s current market phase, as specified by the trading venue                                                                                                                                                     |
| EVENT_CODE         | string[4]   | Event that triggered an instrument status update                                                                                                                                                                                       |
| REASON_CODE        | string[1]   | Reason for an instrument status update                                                                                                                                                                                                 |
| ORDER_ENTRY_STATUS | string[1]   | Indicates the availability of order entry / modification / cancellation                                                                                                                                                                |
| OMD_STATUS         | string[1]   | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| OMDSEQ             | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### WARSAW_FUT - PRL_FULL

Full orderbook data, showing updates to each individual order (MBO)

#### WARSAW_FUT - PRL_FULL Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME   | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP     | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME     | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| UPDATE_TYPE   | string[1]   | Type of update                                                                                                                                                                                                                         |
| ORDER_ID      | string[20]  | Order identifier, uniquely identifying an order at any given point in time.   Uniqueness depends on the exchange - e.g. may be globally unique, or unique per trading day, or per instrument per trading day.                          |
| ORDER_TYPE    | string[1]   | Type of order.                                                                                                                                                                                                                         |
| BUY_SELL_FLAG | int         | Orderbook side (0 - Buy, 1 - Sell)                                                                                                                                                                                                     |
| PRICE         | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE          | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| RECORD_TYPE   | string[1]   | Type of depth update.                                                                                                                                                                                                                  |
| TICK_STATUS   | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| DELETED_TIME  | nsectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### WARSAW_FUT - QTE

Best bid / offer quotes

#### WARSAW_FUT - QTE Table Schema

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

### WARSAW_FUT - STAT

Static data, e.g. ISIN, description, security type

#### WARSAW_FUT - STAT Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                                                                |
|---------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME         | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                             |
| TIMESTAMP           | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                    |
| NAME                | string[200] | Description of the instrument                                                                                                                                                                                                              |
| ISIN                | string[12]  | ISIN code                                                                                                                                                                                                                                  |
| EXCH_SYMBOL         | string[40]  | Ticker symbol specified by the exchange                                                                                                                                                                                                    |
| TRADING_CODE        | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                                   |
| PRODUCT_CODE        | string[20]  | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD. |
| UNDERLYING_SYMBOL   | string[32]  | Symbol of the underlying instrument                                                                                                                                                                                                        |
| UNDERLYING_ISIN     | string[12]  | ISIN of the underlying instrument                                                                                                                                                                                                          |
| MIC                 | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                           |
| OPERATING_MIC       | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                         |
| SEC_TYPE            | string[32]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                    |
| UNDERLYING_SEC_TYPE | string[20]  | Underlying asset class                                                                                                                                                                                                                     |
| STRATEGY_TYPE       | string[48]  | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly                                                                                                                                                                         |
| EXCH_STRATEGY_TYPE  | string[12]  | Type of strategy / spread, as specified by the exchange                                                                                                                                                                                    |
| CFI_CODE            | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                                  |
| CURRENCY            | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                            |
| EXPIRATION_DATE     | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                                  |
| STRIKE_PRICE        | double      | Exercise price for options / warrants                                                                                                                                                                                                      |
| CALL_PUT_IND        | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                            |
| EXERCISE_TYPE       | string[1]   | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)                                                                                                                                                                 |
| SETTLEMENT_TYPE     | string[1]   | Settlement method for a derivatives contract (C - Cash, P - Physical, E - Either cash or physical)                                                                                                                                         |
| CONTRACT_SIZE       | double      | Indicates a derivative’s underlying quantity                                                                                                                                                                                               |
| TICK_SIZE_TYPE      | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                       |
| TICK_SIZE           | string[40]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                                 |
| TICK_VALUE          | double      | Tick value, i.e. the profit / loss per contract resulting from a price movement equal to TICK_SIZE.                                                                                                                                        |
| OMDSEQ              | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.     |

### WARSAW_FUT - TRD

Trades

#### WARSAW_FUT - TRD Table Schema

| Field                 | Data Type   | Description                                                                                                                                                                                                                                       |
|-----------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME           | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                                    |
| TIMESTAMP             | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                           |
| EXCH_TIME             | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                                 |
| PRICE                 | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                                         |
| SIZE                  | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                                  |
| TRADE_TYPE            | string[4]   | Type of trade                                                                                                                                                                                                                                     |
| TRADE_VENUE           | string[4]   | Identifies the venue where a trade was executed.   Typically a MIC, with the special values XOFF for off-exchange and SINT for Systematic Internaliser trades.                                                                                    |
| TRADE_CURRENCY        | string[3]   | Currency in which a trade was executed.                                                                                                                                                                                                           |
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



## WARSAW_FUT_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### WARSAW_FUT_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### WARSAW_FUT_DAILY - DAY Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME   | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP     | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| UPDATE_TYPE   | string[16]  | Type of update                                                                                                                                                                                                                         |
| OPEN          | double      | Open price for the current trading day                                                                                                                                                                                                 |
| HIGH          | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW           | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| CLOSE         | double      | Closing price                                                                                                                                                                                                                          |
| SETTLE_PRICE  | double      | Settlement price                                                                                                                                                                                                                       |
| SETTLE_DATE   | string[8]   | Trading date to which the settlement price relates (YYYYMMDD)                                                                                                                                                                          |
| VOLUME        | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| OPEN_INT      | double      | Open interest for futures / options                                                                                                                                                                                                    |
| OPEN_INT_DATE | string[8]   | Trading date to which the open interest relates (YYYYMMDD)                                                                                                                                                                             |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### WARSAW_FUT_DAILY - STAT

Static data, e.g. ISIN, description, security type

#### WARSAW_FUT_DAILY - STAT Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                                                                |
|---------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME         | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                             |
| TIMESTAMP           | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                    |
| NAME                | string[200] | Description of the instrument                                                                                                                                                                                                              |
| ISIN                | string[12]  | ISIN code                                                                                                                                                                                                                                  |
| EXCH_SYMBOL         | string[40]  | Ticker symbol specified by the exchange                                                                                                                                                                                                    |
| TRADING_CODE        | string[20]  | ID used to identify the instrument in the trading system                                                                                                                                                                                   |
| PRODUCT_CODE        | string[20]  | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD. |
| UNDERLYING_SYMBOL   | string[32]  | Symbol of the underlying instrument                                                                                                                                                                                                        |
| UNDERLYING_ISIN     | string[12]  | ISIN of the underlying instrument                                                                                                                                                                                                          |
| MIC                 | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                           |
| OPERATING_MIC       | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                         |
| SEC_TYPE            | string[32]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                    |
| UNDERLYING_SEC_TYPE | string[20]  | Underlying asset class                                                                                                                                                                                                                     |
| STRATEGY_TYPE       | string[48]  | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly                                                                                                                                                                         |
| EXCH_STRATEGY_TYPE  | string[12]  | Type of strategy / spread, as specified by the exchange                                                                                                                                                                                    |
| CFI_CODE            | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                                  |
| CURRENCY            | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                            |
| EXPIRATION_DATE     | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                                  |
| STRIKE_PRICE        | double      | Exercise price for options / warrants                                                                                                                                                                                                      |
| CALL_PUT_IND        | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                            |
| EXERCISE_TYPE       | string[1]   | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)                                                                                                                                                                 |
| SETTLEMENT_TYPE     | string[1]   | Settlement method for a derivatives contract (C - Cash, P - Physical, E - Either cash or physical)                                                                                                                                         |
| CONTRACT_SIZE       | double      | Indicates a derivative’s underlying quantity                                                                                                                                                                                               |
| TICK_SIZE_TYPE      | string[8]   | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.                                                                                                                                                       |
| TICK_SIZE           | string[40]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                                 |
| TICK_VALUE          | double      | Tick value, i.e. the profit / loss per contract resulting from a price movement equal to TICK_SIZE.                                                                                                                                        |
| OMDSEQ              | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.     |
