# US OTC Equities (Trades only) Schemas

FINRA reported trades for OTC instruments




## US_OTC

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### US_OTC - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### US_OTC - DAY Table Schema

| Field   | Data Type   | Description                                                                                                                                                                                                                            |
|---------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOSE   | double      | Closing price                                                                                                                                                                                                                          |
| HIGH    | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW     | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OMDSEQ  | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN    | double      | Open price for the current trading day                                                                                                                                                                                                 |
| VOLUME  | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |

### US_OTC - MKT

Market phase / instrument status information

#### US_OTC - MKT Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME      | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMD_STATUS     | string[1]   | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| REASON_CODE    | string[50]  | Reason for an instrument status update                                                                                                                                                                                                 |
| TRADING_STATUS | string[6]   | Indicates whether the instrument is subject to a halt or suspension                                                                                                                                                                    |

### US_OTC - STAT

Static data, e.g. ISIN, description, security type

#### US_OTC - STAT Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CURRENCY      | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| EXCH_SYMBOL   | string[20]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| ISIN          | string[12]  | ISIN code                                                                                                                                                                                                                              |
| LOT_SIZE      | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| MIC           | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| NAME          | string[100] | Description of the instrument                                                                                                                                                                                                          |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPERATING_MIC | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| PREV_SYMBOL   | string[20]  | Previous ticker symbol, in the event of a symbol change                                                                                                                                                                                |
| SEC_TYPE      | string[40]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |

### US_OTC - TRD

Trades

#### US_OTC - TRD Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DELETED_TIME     | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| EXCH_TIME        | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| LATE_REPORTED    | string[1]   | Indicates whether a trade was reported late and/or outside normal trading hours                                                                                                                                                        |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE            | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SETTLEMENT_TERMS | string[1]   | Settlement terms associated with a trade                                                                                                                                                                                               |
| SIZE             | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| TICK_STATUS      | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| TRADE_CURRENCY   | string[3]   | Currency in which a trade was executed.                                                                                                                                                                                                |
| TRADE_ID         | string[20]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| TRADE_TYPE       | string[1]   | Type of trade                                                                                                                                                                                                                          |



## US_OTC_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars



### US_OTC_BARS - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### US_OTC_BARS - DAY Table Schema

| Field   | Data Type   | Description                                                                                                                                                                                                                            |
|---------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOSE   | double      | Closing price                                                                                                                                                                                                                          |
| HIGH    | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW     | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OMDSEQ  | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN    | double      | Open price for the current trading day                                                                                                                                                                                                 |
| VOLUME  | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |

### US_OTC_BARS - MKT

Market phase / instrument status information

#### US_OTC_BARS - MKT Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME      | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OMD_STATUS     | string[64]  | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| REASON_CODE    | string[50]  | Reason for an instrument status update                                                                                                                                                                                                 |
| TRADING_STATUS | string[6]   | Indicates whether the instrument is subject to a halt or suspension                                                                                                                                                                    |

### US_OTC_BARS - TRD_1D

Daily trade bars

#### US_OTC_BARS - TRD_1D Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BUY_VOLUME       | long        | Traded volume originating from incoming buy orders.  Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| CLOUD_DB         | string[32]  | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.                                                                             |
| FIRST            | double      | Price of the first eligible trade in the current bar interval                                                                                                                                                                          |
| FIRST_SIZE       | long        | Size of the first eligible trade in the current bar interval                                                                                                                                                                           |
| FIRST_TIME       | nsectime    | Timestamp of the first eligible trade in the current bar interval                                                                                                                                                                      |
| HIGH             | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| HIGH_SIZE        | long        | Size of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                    |
| HIGH_TIME        | nsectime    | Timestamp of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                               |
| LAST             | double      | Price of the last eligible trade in the current bar interval                                                                                                                                                                           |
| LAST_SIZE        | long        | Size of the last eligible trade in the current bar interval                                                                                                                                                                            |
| LAST_TIME        | nsectime    | Timestamp of the last eligible trade in the current bar interval                                                                                                                                                                       |
| LOW              | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| LOW_SIZE         | long        | Size of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                     |
| LOW_TIME         | nsectime    | Timestamp of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| SELL_VOLUME      | long        | Traded volume originating from incoming sell orders. Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| TRADE_CURRENCY   | string[3]   | Currency in which a trade was executed.                                                                                                                                                                                                |
| TRADE_TICK_COUNT | long        | Number of eligible trades in the current bar interval                                                                                                                                                                                  |
| TWAP             | double      | TIme-weighted average price                                                                                                                                                                                                            |
| VOLUME           | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VWAP             | double      | Volume-weighted average price                                                                                                                                                                                                          |

### US_OTC_BARS - TRD_1M

1-minute trade bars

#### US_OTC_BARS - TRD_1M Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BUY_VOLUME       | long        | Traded volume originating from incoming buy orders.  Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| CLOUD_DB         | string[32]  | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.                                                                             |
| FIRST            | double      | Price of the first eligible trade in the current bar interval                                                                                                                                                                          |
| FIRST_SIZE       | long        | Size of the first eligible trade in the current bar interval                                                                                                                                                                           |
| FIRST_TIME       | nsectime    | Timestamp of the first eligible trade in the current bar interval                                                                                                                                                                      |
| HIGH             | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| HIGH_SIZE        | long        | Size of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                    |
| HIGH_TIME        | nsectime    | Timestamp of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                               |
| LAST             | double      | Price of the last eligible trade in the current bar interval                                                                                                                                                                           |
| LAST_SIZE        | long        | Size of the last eligible trade in the current bar interval                                                                                                                                                                            |
| LAST_TIME        | nsectime    | Timestamp of the last eligible trade in the current bar interval                                                                                                                                                                       |
| LOW              | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| LOW_SIZE         | long        | Size of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                     |
| LOW_TIME         | nsectime    | Timestamp of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| SELL_VOLUME      | long        | Traded volume originating from incoming sell orders. Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| TRADE_CURRENCY   | string[3]   | Currency in which a trade was executed.                                                                                                                                                                                                |
| TRADE_TICK_COUNT | long        | Number of eligible trades in the current bar interval                                                                                                                                                                                  |
| TWAP             | double      | TIme-weighted average price                                                                                                                                                                                                            |
| VOLUME           | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VWAP             | double      | Volume-weighted average price                                                                                                                                                                                                          |

### US_OTC_BARS - VWAP_1H

1-hour VWAP bars

#### US_OTC_BARS - VWAP_1H Table Schema

| Field    | Data Type   | Description                                                                                                                                                                                                                            |
|----------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOUD_DB | string[32]  | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.                                                                             |
| CURRENCY | string[64]  | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| OMDSEQ   | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| TWAP     | double      | TIme-weighted average price                                                                                                                                                                                                            |
| VOLUME   | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VWAP     | double      | Volume-weighted average price                                                                                                                                                                                                          |



## US_OTC_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type
* TRD_1D - Daily trade bars



### US_OTC_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### US_OTC_DAILY - DAY Table Schema

| Field   | Data Type   | Description                                                                                                                                                                                                                            |
|---------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOSE   | double      | Closing price                                                                                                                                                                                                                          |
| HIGH    | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW     | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OMDSEQ  | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN    | double      | Open price for the current trading day                                                                                                                                                                                                 |
| VOLUME  | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |

### US_OTC_DAILY - STAT

Static data, e.g. ISIN, description, security type

#### US_OTC_DAILY - STAT Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CURRENCY      | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| EXCH_SYMBOL   | string[20]  | Ticker symbol specified by the exchange                                                                                                                                                                                                |
| ISIN          | string[12]  | ISIN code                                                                                                                                                                                                                              |
| LOT_SIZE      | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| MIC           | string[4]   | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| NAME          | string[100] | Description of the instrument                                                                                                                                                                                                          |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPERATING_MIC | string[4]   | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| PREV_SYMBOL   | string[20]  | Previous ticker symbol, in the event of a symbol change                                                                                                                                                                                |
| SEC_TYPE      | string[40]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |

### US_OTC_DAILY - TRD_1D

Daily trade bars

#### US_OTC_DAILY - TRD_1D Table Schema

