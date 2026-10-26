# Nodal Exchange Schemas

Nodal Exchange is a leading commodities derivatives exchange providing price, credit, and liquidity risk management to participants in the North American energy markets. It operates as the #1 power futures exchange in the United States, capturing roughly 55% market share of the U.S. power futures open interest.




## NODAL

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* PRL - Market depth data, aggregated by price point (MBP)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### NODAL - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### NODAL - DAY Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME     | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP       | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| CLOSE           | double      | Closing price                                                                                                                                                                                                                          |
| DELTA           | double      | Option delta, i.e. the rate of change of an option’s price relative to its underlying                                                                                                                                                  |
| HIGH            | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW             | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OFF_BOOK_VOLUME | double      | Total volume traded off-book                                                                                                                                                                                                           |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| ON_BOOK_VOLUME  | double      | Total volume traded through the orderbook                                                                                                                                                                                              |
| OPEN            | double      | Open price for the current trading day                                                                                                                                                                                                 |
| OPEN_INT        | double      | Open interest for futures / options                                                                                                                                                                                                    |
| OPEN_INT_DATE   | string[8]   | Trading date to which the open interest relates (YYYYMMDD)                                                                                                                                                                             |
| SETTLE_DATE     | string[8]   | Trading date to which the settlement price relates (YYYYMMDD)                                                                                                                                                                          |
| SETTLE_PRICE    | double      | Settlement price                                                                                                                                                                                                                       |
| SPREAD_VOLUME   | double      | Total volume originating from spread executions  [i.e. strategy leg trades reported in each outright leg when two spread orders are matched]                                                                                           |
| TRADE_COUNT     | double      | Number of trades on the current trading day                                                                                                                                                                                            |
| UPDATE_TYPE     | string[16]  | Type of update                                                                                                                                                                                                                         |
| VOLUME          | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VWAP            | double      | Volume-weighted average price                                                                                                                                                                                                          |

### NODAL - PRL

Market depth data, aggregated by price point (MBP)

#### NODAL - PRL Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME   | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP     | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| BUY_SELL_FLAG | int         | Orderbook side (0 - Buy, 1 - Sell)                                                                                                                                                                                                     |
| DELETED_TIME  | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| EXCH_TIME     | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE         | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| RECORD_TYPE   | string[1]   | Type of depth update.                                                                                                                                                                                                                  |
| SIZE          | int         | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| TICK_STATUS   | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |

### NODAL - QTE

Best bid / offer quotes

#### NODAL - QTE Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| ASK_PRICE   | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE    | int         | Best ask size                                                                                                                                                                                                                          |
| BID_PRICE   | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE    | int         | Best bid size                                                                                                                                                                                                                          |
| EXCH_TIME   | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### NODAL - STAT

Static data, e.g. ISIN, description, security type

#### NODAL - STAT Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                                                                |
|---------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME         | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                             |
| TIMESTAMP           | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                    |
| CALL_PUT_IND        | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                            |
| CONTRACT_FREQUENCY  | string[1]   | Expiration frequency of a derivative contract (D - Daily, W - Weekly, M - Monthly, Q - Quarterly, A - Annual, I - Irregular)                                                                                                               |
| CONTRACT_LOCATION   | string[40]  | Location to which a derivative contract relates (e.g. ISO load zone for US power contracts)                                                                                                                                                |
| CONTRACT_REGION     | string[16]  | Region to which a derivative contract relates                                                                                                                                                                                              |
| CONTRACT_SIZE       | double      | Indicates a derivative’s underlying quantity                                                                                                                                                                                               |
| CONTRACT_UNITS      | string[16]  | Units in which CONTRACT_SIZE is expressed                                                                                                                                                                                                  |
| CURRENCY            | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                            |
| EXCH_SEC_TYPE       | string[20]  | Instrument type as specified by the exchange                                                                                                                                                                                               |
| EXCH_STRATEGY_TYPE  | string[20]  | Type of strategy / spread, as specified by the exchange                                                                                                                                                                                    |
| EXCH_SYMBOL         | string[40]  | Ticker symbol specified by the exchange                                                                                                                                                                                                    |
| EXCH_SYMBOL_2       | string[40]  | Secondary ticker symbol specified by the exchange                                                                                                                                                                                          |
| EXERCISE_TYPE       | string[1]   | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)                                                                                                                                                                 |
| EXPIRATION_DATE     | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                                  |
| MIC                 | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                           |
| NAME                | string[200] | Description of the instrument                                                                                                                                                                                                              |
| OMDSEQ              | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.     |
| OPERATING_MIC       | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                         |
| PRODUCT_CODE        | string[20]  | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD. |
| SEC_TYPE            | string[20]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                    |
| SETTLEMENT_TYPE     | string[1]   | Settlement method for a derivatives contract (C - Cash, P - Physical, E - Either cash or physical)                                                                                                                                         |
| STRATEGY_TYPE       | string[40]  | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly                                                                                                                                                                         |
| STRIKE_PRICE        | double      | Exercise price for options / warrants                                                                                                                                                                                                      |
| TICK_SIZE           | string[80]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                                 |
| UNDERLYING_SEC_TYPE | string[20]  | Underlying asset class                                                                                                                                                                                                                     |
| UNDERLYING_SYMBOL   | string[32]  | Symbol of the underlying instrument                                                                                                                                                                                                        |

### NODAL - TRD

Trades

#### NODAL - TRD Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME    | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP      | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| AGGRESSOR_SIDE | string[1]   | Indicates whether a trade resulted from an incoming buy or sell order.                                                                                                                                                                 |
| BOOK_TYPE      | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                            |
| DELETED_TIME   | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| EXCH_TIME      | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE          | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE           | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| TICK_STATUS    | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| TRADE_ID       | string[32]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| TRADE_PERIOD   | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                       |
| TRADE_TYPE     | string[4]   | Type of trade                                                                                                                                                                                                                          |



## NODAL_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### NODAL_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### NODAL_DAILY - DAY Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME     | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP       | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| CLOSE           | double      | Closing price                                                                                                                                                                                                                          |
| DELTA           | double      | Option delta, i.e. the rate of change of an option’s price relative to its underlying                                                                                                                                                  |
| HIGH            | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW             | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OFF_BOOK_VOLUME | double      | Total volume traded off-book                                                                                                                                                                                                           |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| ON_BOOK_VOLUME  | double      | Total volume traded through the orderbook                                                                                                                                                                                              |
| OPEN            | double      | Open price for the current trading day                                                                                                                                                                                                 |
| OPEN_INT        | double      | Open interest for futures / options                                                                                                                                                                                                    |
| OPEN_INT_DATE   | string[8]   | Trading date to which the open interest relates (YYYYMMDD)                                                                                                                                                                             |
| SETTLE_DATE     | string[8]   | Trading date to which the settlement price relates (YYYYMMDD)                                                                                                                                                                          |
| SETTLE_PRICE    | double      | Settlement price                                                                                                                                                                                                                       |
| SPREAD_VOLUME   | double      | Total volume originating from spread executions  [i.e. strategy leg trades reported in each outright leg when two spread orders are matched]                                                                                           |
| TRADE_COUNT     | double      | Number of trades on the current trading day                                                                                                                                                                                            |
| UPDATE_TYPE     | string[16]  | Type of update                                                                                                                                                                                                                         |
| VOLUME          | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VWAP            | double      | Volume-weighted average price                                                                                                                                                                                                          |

### NODAL_DAILY - STAT

Static data, e.g. ISIN, description, security type

#### NODAL_DAILY - STAT Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                                                                |
|---------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME         | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                             |
| TIMESTAMP           | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                    |
| CALL_PUT_IND        | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                            |
| CONTRACT_FREQUENCY  | string[1]   | Expiration frequency of a derivative contract (D - Daily, W - Weekly, M - Monthly, Q - Quarterly, A - Annual, I - Irregular)                                                                                                               |
| CONTRACT_LOCATION   | string[40]  | Location to which a derivative contract relates (e.g. ISO load zone for US power contracts)                                                                                                                                                |
| CONTRACT_REGION     | string[16]  | Region to which a derivative contract relates                                                                                                                                                                                              |
| CONTRACT_SIZE       | double      | Indicates a derivative’s underlying quantity                                                                                                                                                                                               |
| CONTRACT_UNITS      | string[16]  | Units in which CONTRACT_SIZE is expressed                                                                                                                                                                                                  |
| CURRENCY            | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                            |
| EXCH_SEC_TYPE       | string[20]  | Instrument type as specified by the exchange                                                                                                                                                                                               |
| EXCH_STRATEGY_TYPE  | string[20]  | Type of strategy / spread, as specified by the exchange                                                                                                                                                                                    |
| EXCH_SYMBOL         | string[40]  | Ticker symbol specified by the exchange                                                                                                                                                                                                    |
| EXCH_SYMBOL_2       | string[40]  | Secondary ticker symbol specified by the exchange                                                                                                                                                                                          |
| EXERCISE_TYPE       | string[1]   | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)                                                                                                                                                                 |
| EXPIRATION_DATE     | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                                  |
| MIC                 | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                           |
| NAME                | string[200] | Description of the instrument                                                                                                                                                                                                              |
| OMDSEQ              | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.     |
| OPERATING_MIC       | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                         |
| PRODUCT_CODE        | string[20]  | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD. |
| SEC_TYPE            | string[20]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                    |
| SETTLEMENT_TYPE     | string[1]   | Settlement method for a derivatives contract (C - Cash, P - Physical, E - Either cash or physical)                                                                                                                                         |
| STRATEGY_TYPE       | string[40]  | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly                                                                                                                                                                         |
| STRIKE_PRICE        | double      | Exercise price for options / warrants                                                                                                                                                                                                      |
| TICK_SIZE           | string[80]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                                 |
| UNDERLYING_SEC_TYPE | string[20]  | Underlying asset class                                                                                                                                                                                                                     |
| UNDERLYING_SYMBOL   | string[32]  | Symbol of the underlying instrument                                                                                                                                                                                                        |
