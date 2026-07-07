# ICE Abu Dhabi Schemas

IFAD broadens regional trading opportunities with micro Index futures on the MSCI GCC, MSCI Qatar, MSCI UAE, and MSCI India indices, providing seamless access to these key markets on a single venue.




## ICE_ABU_DHABI

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IDX - Index values
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### ICE_ABU_DHABI - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### ICE_ABU_DHABI - DAY Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOSE         | double      | Closing price                                                                                                                                                                                                                          |
| HIGH          | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW           | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN          | double      | Open price for the current trading day                                                                                                                                                                                                 |
| OPEN_INT      | double      | Open interest for futures / options                                                                                                                                                                                                    |
| OPEN_INT_DATE | string[8]   | Trading date to which the open interest relates (YYYYMMDD)                                                                                                                                                                             |
| SETTLE_DATE   | string[8]   | Trading date to which the settlement price relates (YYYYMMDD)                                                                                                                                                                          |
| SETTLE_PRICE  | double      | Settlement price                                                                                                                                                                                                                       |
| UPDATE_TYPE   | string[16]  | Type of update                                                                                                                                                                                                                         |
| VOLUME        | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |

### ICE_ABU_DHABI - IDX

Index values

#### ICE_ABU_DHABI - IDX Table Schema

| Field     | Data Type   | Description                                                                                                                                                                                                                            |
|-----------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ    | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE     | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |

### ICE_ABU_DHABI - IND

Indicative pricing, e.g. indicative auction prices and imbalance

#### ICE_ABU_DHABI - IND Table Schema

| Field     | Data Type   | Description                                                                                                                                                                                                                            |
|-----------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ    | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE     | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE      | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |

### ICE_ABU_DHABI - MKT

Market phase / instrument status information

#### ICE_ABU_DHABI - MKT Table Schema

| Field      | Data Type   | Description                                                                                                                                                                                                                            |
|------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME  | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| MKT_PHASE  | string[6]   | Indicates the instrument’s current market phase, as specified by the trading venue                                                                                                                                                     |
| OMD_STATUS | string[1]   | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| OMDSEQ     | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### ICE_ABU_DHABI - QTE

Best bid / offer quotes

#### ICE_ABU_DHABI - QTE Table Schema

| Field     | Data Type   | Description                                                                                                                                                                                                                            |
|-----------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_PRICE | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE  | int         | Best ask size                                                                                                                                                                                                                          |
| BID_PRICE | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE  | int         | Best bid size                                                                                                                                                                                                                          |
| EXCH_TIME | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ    | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### ICE_ABU_DHABI - STAT

Static data, e.g. ISIN, description, security type

#### ICE_ABU_DHABI - STAT Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                                                                |
|--------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALL_PUT_IND       | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                            |
| CFI_CODE           | string[6]   | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                                  |
| CONTRACT_SIZE      | double      | Indicates a derivative’s underlying quantity                                                                                                                                                                                               |
| CURRENCY           | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                            |
| EXCH_STRATEGY_TYPE | string[10]  | Type of strategy / spread, as specified by the exchange                                                                                                                                                                                    |
| EXCH_SYMBOL        | string[40]  | Ticker symbol specified by the exchange                                                                                                                                                                                                    |
| EXERCISE_TYPE      | string[1]   | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)                                                                                                                                                                 |
| EXPIRATION_DATE    | string[8]   | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                                  |
| ISIN               | string[12]  | ISIN code                                                                                                                                                                                                                                  |
| MIC                | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                           |
| NAME               | string[200] | Description of the instrument                                                                                                                                                                                                              |
| OMDSEQ             | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.     |
| OPERATING_MIC      | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                         |
| PRODUCT_CODE       | string[20]  | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD. |
| SEC_TYPE           | string[30]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                    |
| STRATEGY_TYPE      | string[40]  | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly                                                                                                                                                                         |
| STRIKE_PRICE       | double      | Exercise price for options / warrants                                                                                                                                                                                                      |
| TICK_SIZE          | string[50]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                                 |
| TICK_VALUE         | double      | Tick value, i.e. the profit / loss per contract resulting from a price movement equal to TICK_SIZE.                                                                                                                                        |
| TRADING_CODE       | string[12]  | ID used to identify the instrument in the trading system                                                                                                                                                                                   |
| UNDERLYING_ISIN    | string[12]  | ISIN of the underlying instrument                                                                                                                                                                                                          |
| UNDERLYING_SYMBOL  | string[32]  | Symbol of the underlying instrument                                                                                                                                                                                                        |

### ICE_ABU_DHABI - TRD

Trades

#### ICE_ABU_DHABI - TRD Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AGGRESSOR_SIDE | string[1]   | Indicates whether a trade resulted from an incoming buy or sell order.                                                                                                                                                                 |
| BOOK_TYPE      | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                            |
| DELETED_TIME   | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| EXCH_TIME      | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE          | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE           | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| TICK_STATUS    | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| TRADE_ID       | string[16]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| TRADE_TYPE     | string[4]   | Type of trade                                                                                                                                                                                                                          |



## ICE_ABU_DHABI_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### ICE_ABU_DHABI_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### ICE_ABU_DHABI_DAILY - DAY Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOSE         | double      | Closing price                                                                                                                                                                                                                          |
| HIGH          | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW           | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN          | double      | Open price for the current trading day                                                                                                                                                                                                 |
| OPEN_INT      | double      | Open interest for futures / options                                                                                                                                                                                                    |
| OPEN_INT_DATE | string[8]   | Trading date to which the open interest relates (YYYYMMDD)                                                                                                                                                                             |
| SETTLE_DATE   | string[8]   | Trading date to which the settlement price relates (YYYYMMDD)                                                                                                                                                                          |
| SETTLE_PRICE  | double      | Settlement price                                                                                                                                                                                                                       |
| UPDATE_TYPE   | string[16]  | Type of update                                                                                                                                                                                                                         |
| VOLUME        | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |

### ICE_ABU_DHABI_DAILY - STAT

Static data, e.g. ISIN, description, security type

#### ICE_ABU_DHABI_DAILY - STAT Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                                                                |
|--------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALL_PUT_IND       | string[1]   | C - Call option, P - Put option                                                                                                                                                                                                            |
