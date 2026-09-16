# US Consolidated Equities (exc. OTC) Sample Schemas

A subset of symbols from the US SIP for trading between January 2,2024 and March 31, 2024




## US_COMP_SAMPLE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* NBBO - National Best Bid / Offer quotes
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### US_COMP_SAMPLE - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### US_COMP_SAMPLE - DAY Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME            | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP              | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCHANGE               | string[4]   | Exchange from which the update originates                                                                                                                                                                                              |
| OPEN                   | double      | Open price for the current trading day                                                                                                                                                                                                 |
| HIGH                   | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW                    | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| CLOSE                  | double      | Closing price                                                                                                                                                                                                                          |
| VOLUME                 | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VWAP                   | double      | Volume-weighted average price                                                                                                                                                                                                          |
| PRICE_OPENING_AUCTION  | double      | Price of the Opening Auction                                                                                                                                                                                                           |
| VOLUME_OPENING_AUCTION | long        | Volume of the Opening Auction                                                                                                                                                                                                          |
| PRICE_CLOSING_AUCTION  | double      | Price of the Closing Auction                                                                                                                                                                                                           |
| VOLUME_CLOSING_AUCTION | long        | Volume of the Closing Auction                                                                                                                                                                                                          |
| VOLUME_MAIN_SESSION    | long        | Volume of the Main Trading Session                                                                                                                                                                                                     |
| VOLUME_PRE_MARKET      | long        | Volume of the Pre-Market Trading Session                                                                                                                                                                                               |
| VOLUME_POST_MARKET     | long        | Volume of the Post-Market Trading Session                                                                                                                                                                                              |
| VOLUME_ODD_LOT         | long        | Volume of the Odd Lot Trades                                                                                                                                                                                                           |
| VOLUME_ROUND_LOT       | long        | Volume of Round Lot Trades                                                                                                                                                                                                             |
| VOLUME_OFF_EXCHANGE    | long        | Volume of Off Exchange Trades                                                                                                                                                                                                          |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP_SAMPLE - LULD

Limit Up / Limit Down price levels

#### US_COMP_SAMPLE - LULD Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| SEQ_NUM     | long        | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds                                                                                        |
| LOW_LIMIT   | double      | Lower trading limit / circuit breaker level                                                                                                                                                                                            |
| HIGH_LIMIT  | double      | Upper trading limit / circuit breaker level                                                                                                                                                                                            |
| LULD_IND    | string[2]   | Type of Limit Up / Limit Down (LULD) price update                                                                                                                                                                                      |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP_SAMPLE - MKT

Market phase / instrument status information

#### US_COMP_SAMPLE - MKT Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME            | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP              | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCHANGE               | string[1]   | Exchange from which the update originates                                                                                                                                                                                              |
| TRADING_STATUS         | string[1]   | Indicates whether the instrument is subject to a halt or suspension                                                                                                                                                                    |
| SHORT_SALE_RESTRICTION | string[1]   | Indicates whether short selling is permitted                                                                                                                                                                                           |
| PARTICIPANT_TIME       | nsectime    | Event timestamp (e.g. trade execution time), as provided by one of the participant exchanges in a consolidated feed                                                                                                                    |
| SEQ_NUM                | long        | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds                                                                                        |
| REASON_CODE            | string[6]   | Reason for an instrument status update                                                                                                                                                                                                 |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP_SAMPLE - NBBO

National Best Bid / Offer quotes

#### US_COMP_SAMPLE - NBBO Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME    | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP      | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| BID_PRICE      | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE       | int         | Best bid size                                                                                                                                                                                                                          |
| BID_SIZE_TOTAL | int         | Total size at the (national) best bid price across all participant markets                                                                                                                                                             |
| BID_EXCHANGE   | string[2]   | Exchange that set the best bid                                                                                                                                                                                                         |
| ASK_PRICE      | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE       | int         | Best ask size                                                                                                                                                                                                                          |
| ASK_SIZE_TOTAL | int         | Total size at the (national) best ask price across all participant markets                                                                                                                                                             |
| ASK_EXCHANGE   | string[2]   | Exchange that set the best ask                                                                                                                                                                                                         |
| IS_PRE_OPEN    | int         | Indicates whether a quote originates from the period before (1) or after (0) the instrument has opened on the primary market                                                                                                           |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP_SAMPLE - QTE

Best bid / offer quotes

#### US_COMP_SAMPLE - QTE Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                                                            |
|---------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME         | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP           | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCHANGE            | string[1]   | Exchange from which the update originates                                                                                                                                                                                              |
| CORR                | string[1]   | Type of trade correction / cancellation                                                                                                                                                                                                |
| DELETED_TIME        | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS         | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| COND                | string[1]   | Condition code                                                                                                                                                                                                                         |
| NBBO_IND            | string[1]   | Indicates whether the quote affects the NBBO                                                                                                                                                                                           |
| FINRA_BBO_IND       | string[1]   | Indicates whether the quote affects the FINRA BBO [currently unused]                                                                                                                                                                   |
| FINRA_ADF_MPID_IND  | string[1]   | Indicates whether a FINRA participant ID is available for a BBO quote [currently unused]                                                                                                                                               |
| SOURCE              | string[1]   | Source from which an update originates                                                                                                                                                                                                 |
| RPI                 | string[1]   | Indicates the presence of Retail Price Improvement interest on bid and/or ask side                                                                                                                                                     |
| RESTRICTION_IND     | string[1]   | Indicates whether short selling is permitted                                                                                                                                                                                           |
| LULD_BBO_IND        | string[1]   | Indicates whether the bid/ask crosses the upper / lower LULD price bands                                                                                                                                                               |
| SIP_MSG_ID          | string[1]   | Identifies messages generated by the SIP ( - Originates from an exchange, E - UTP, S - Consolidated Tape System)                                                                                                                       |
| NBBO_LULD_IND       | string[1]   | Indicates whether the NBBO crosses the upper / lower LULD price bands                                                                                                                                                                  |
| FINRA_ADF_IND       | string[1]   | Indicates whether the quote reflects the FINRA BBO                                                                                                                                                                                     |
| TICKER              | string[16]  | Ticker symbol, as specified by the data source                                                                                                                                                                                         |
| BID_PRICE           | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE            | long        | Best bid size                                                                                                                                                                                                                          |
| ASK_PRICE           | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE            | long        | Best ask size                                                                                                                                                                                                                          |
| SEQ_NUM             | long        | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds                                                                                        |
| PARTICIPANT_TIME    | nsectime    | Event timestamp (e.g. trade execution time), as provided by one of the participant exchanges in a consolidated feed                                                                                                                    |
| FINRA_ADF_TIME      | nsectime    | Timestamp provided by a FINRA ADF                                                                                                                                                                                                      |
| SECURITY_STATUS_IND | string[2]   | Security status                                                                                                                                                                                                                        |
| OMDSEQ              | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP_SAMPLE - STAT

Static data, e.g. ISIN, description, security type

#### US_COMP_SAMPLE - STAT Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                                                            |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME        | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP          | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| CONSOLIDATED_TAPE  | string[1]   | Consolidated Tape on which a US security is published (A/B/C).                                                                                                                                                                         |
| TEST_SYMBOL        | string[1]   | Y - Test symbol, N - Not a test symbol                                                                                                                                                                                                 |
| NAME               | string[200] | Description of the instrument                                                                                                                                                                                                          |
| SIP_SYMBOL         | string[16]  | Ticker symbol used by the US Securities Information Processor (CTA / UTP)                                                                                                                                                              |
| PREV_SYMBOL        | string[16]  | Previous ticker symbol, in the event of a symbol change                                                                                                                                                                                |
| PRIMARY_MIC        | string[4]   | MIC of the instrument’s primary listing market, or the reference market for instruments traded on an MTF                                                                                                                               |
| SEC_TYPE           | string[30]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| NYSE_INDUSTRY_CODE | string[4]   | Industry classification, as defined by NYSE                                                                                                                                                                                            |
| LOT_SIZE           | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| TICK_PILOT_IND     | string[20]  | Specifies any tick size pilot initiatives in which the instrument is participating                                                                                                                                                     |
| LISTING_DATE       | string[8]   | Date when the instrument was listed (YYYYMMDD)                                                                                                                                                                                         |
| SHARES_OUTSTANDING | long        | Shares / quantity outstanding                                                                                                                                                                                                          |
| OMDSEQ             | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP_SAMPLE - TRD

Trades

#### US_COMP_SAMPLE - TRD Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME      | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP        | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCHANGE         | string[1]   | Exchange from which the update originates                                                                                                                                                                                              |
| COND             | string[4]   | Condition code                                                                                                                                                                                                                         |
| STOP_STOCK       | string[1]   | Y - Stopped stock trade, N - Not a stopped stock trade,  - Not applicable                                                                                                                                                              |
| SOURCE           | string[1]   | Source from which an update originates                                                                                                                                                                                                 |
| TRF              | string[1]   | Trade Reporting Facility used to report a trade (for trades reported to FINRA)                                                                                                                                                         |
| TTE              | string[1]   | Indicates whether a trade is exempt from the Trade Through Rule (1 - Trade Through Exempt, 0 - No Trade Through Exemption)                                                                                                             |
| TICKER           | string[16]  | Ticker symbol, as specified by the data source                                                                                                                                                                                         |
| PRICE            | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| DELETED_TIME     | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS      | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| SIZE             | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| CORR             | int         | Type of trade correction / cancellation                                                                                                                                                                                                |
| SEQ_NUM          | long        | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds                                                                                        |
| TRADE_ID         | string[20]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| PARTICIPANT_TIME | nsectime    | Event timestamp (e.g. trade execution time), as provided by one of the participant exchanges in a consolidated feed                                                                                                                    |
| TRF_TIME         | nsectime    | Time at which a trade was processed by the Trade Reporting Facility (for trades reported to FINRA)                                                                                                                                     |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |



## US_COMP_SAMPLE_BARS

Database includes the following tick types:

* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars



### US_COMP_SAMPLE_BARS - QTE_1M

1-minute quote bars

#### US_COMP_SAMPLE_BARS - QTE_1M Table Schema

| Field                 | Data Type   | Description                                                                                                                                                                                                                                       |
|-----------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME           | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                                    |
| TIMESTAMP             | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                           |
| FIRST_BID_TIME        | nsectime    | Time of the first best bid update in the current bar interval                                                                                                                                                                                     |
| FIRST_BID_PRICE       | double      | Price of the first best bid update in the current bar interval                                                                                                                                                                                    |
| FIRST_BID_SIZE        | long        | Size of the first best bid update in the current bar interval                                                                                                                                                                                     |
| FIRST_ASK_TIME        | nsectime    | Time of the first best ask update in the current bar interval                                                                                                                                                                                     |
| FIRST_ASK_PRICE       | double      | Price of the first best ask update in the current bar interval                                                                                                                                                                                    |
| FIRST_ASK_SIZE        | long        | Size of the first best ask update in the current bar interval                                                                                                                                                                                     |
| HIGH_BID_TIME         | nsectime    | Time of the bid quote that set HIGH_BID.  If there are multiple quotes at that price, the first one is used.                                                                                                                                      |
| HIGH_BID              | double      | Highest bid price in the current bar interval                                                                                                                                                                                                     |
| HIGH_BID_SIZE         | long        | Size of the bid quote that set HIGH_BID.  If there are multiple quotes at that price, the first one is used.                                                                                                                                      |
| ASK_PRICE_AT_HIGH_BID | double      | Ask price of the quote that set HIGH_BID.  If there are multiple bid quotes at HIGH_BID, the first one is used.                                                                                                                                   |
| ASK_SIZE_AT_HIGH_BID  | long        | Ask size of the quote that set HIGH_BID.  If there are multiple bid quotes at HIGH_BID, the first one is used.                                                                                                                                    |
| LOW_ASK_TIME          | nsectime    | Time of the bid quote that set LOW_ASK.  If there are multiple quotes at that price, the first one is used.                                                                                                                                       |
| LOW_ASK               | double      | Lowest ask price in the current bar interval                                                                                                                                                                                                      |
| LOW_ASK_SIZE          | long        | Size of the ask quote that set LOW_ASK.  If there are multiple quotes at that price, the first one is used.                                                                                                                                       |
| BID_PRICE_AT_LOW_ASK  | double      | Bid price of the quote that set LOW_ASK. If there are multiple ask quotes at LOW_ASK, the first one is used.                                                                                                                                      |
| BID_SIZE_LOW_ASK      | long        | Bid size of the quote that set LOW_ASK.  If there are multiple ask quotes at LOW_ASK, the first one is used.                                                                                                                                      |
| LAST_BID_TIME         | nsectime    | Time of the last best bid update in the current bar interval                                                                                                                                                                                      |
| LAST_BID_PRICE        | double      | Price of the last best bid update in the current bar interval                                                                                                                                                                                     |
| LAST_BID_SIZE         | long        | Size of the last best bid update in the current bar interval                                                                                                                                                                                      |
| LAST_ASK_TIME         | nsectime    | Time of the last best ask update in the current bar interval                                                                                                                                                                                      |
| LAST_ASK_PRICE        | double      | Price of the last best ask update in the current bar interval                                                                                                                                                                                     |
| LAST_ASK_SIZE         | long        | Size of the last best ask update in the current bar interval                                                                                                                                                                                      |
| MID_TWAP              | double      | Time-weighted average of the midpoint of the best bid/ask over the current bar interval.  [Note: One-sided or empty quotes are excluded from the calculation]                                                                                     |
| MID_MEDIAN            | double      | Median of the midpoint of the best bid/ask quotes over the current bar interval. [Note: One-sided or empty quotes are excluded from the calculation]                                                                                              |
| MID_LAST              | double      | Midpoint of the last best bid/ask in the current bar interval. [Note: One-sided or empty quotes are excluded from the calculation]                                                                                                                |
| SPREAD_MIN            | double      | Narrowest bid/ask spread, i.e. the lowest value of (best ask price - best bid price) over the current bar interval.   [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation] |
| SPREAD_MAX            | double      | Widest bid/ask spread, i.e. the highest value of (best ask price - best bid price) over the current bar interval.   [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation]   |
| SPREAD_TWAP           | double      | Time-weighted average of (best ask price - best bid price) over the current bar interval.  [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation]                            |
| SPREAD_MEDIAN         | double      | Median value of (best ask price - best bid price) over the current bar interval.   [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation]                                    |
| SPREAD_LAST           | double      | Last value of (best ask price - best bid price) over the current bar interval.  [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation]                                       |
| QUOTE_CURRENCY        | string[3]   | Currency in which a quote price is expressed.                                                                                                                                                                                                     |
| QUOTE_TICK_COUNT      | long        | Number of BBO quotes in the current bar interval                                                                                                                                                                                                  |
| CLOUD_DB              | string[32]  | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.                                                                                        |
| OMDSEQ                | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.            |

### US_COMP_SAMPLE_BARS - TRD_1D

Daily trade bars

#### US_COMP_SAMPLE_BARS - TRD_1D Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME      | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP        | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| FIRST_TIME       | nsectime    | Timestamp of the first eligible trade in the current bar interval                                                                                                                                                                      |
| FIRST            | double      | Price of the first eligible trade in the current bar interval                                                                                                                                                                          |
| FIRST_SIZE       | long        | Size of the first eligible trade in the current bar interval                                                                                                                                                                           |
| HIGH_TIME        | nsectime    | Timestamp of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                               |
| HIGH             | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| HIGH_SIZE        | long        | Size of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                    |
| LOW_TIME         | nsectime    | Timestamp of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                |
| LOW              | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| LOW_SIZE         | long        | Size of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                     |
| LAST_TIME        | nsectime    | Timestamp of the last eligible trade in the current bar interval                                                                                                                                                                       |
| LAST             | double      | Price of the last eligible trade in the current bar interval                                                                                                                                                                           |
| LAST_SIZE        | long        | Size of the last eligible trade in the current bar interval                                                                                                                                                                            |
| VWAP             | double      | Volume-weighted average price                                                                                                                                                                                                          |
| TWAP             | double      | TIme-weighted average price                                                                                                                                                                                                            |
| VOLUME           | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| TRADE_CURRENCY   | string[3]   | Currency in which a trade was executed.                                                                                                                                                                                                |
| TRADE_TICK_COUNT | long        | Number of eligible trades in the current bar interval                                                                                                                                                                                  |
| CLOUD_DB         | string[32]  | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.                                                                             |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP_SAMPLE_BARS - TRD_1M

1-minute trade bars

#### US_COMP_SAMPLE_BARS - TRD_1M Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME      | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP        | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| FIRST_TIME       | nsectime    | Timestamp of the first eligible trade in the current bar interval                                                                                                                                                                      |
| FIRST            | double      | Price of the first eligible trade in the current bar interval                                                                                                                                                                          |
| FIRST_SIZE       | long        | Size of the first eligible trade in the current bar interval                                                                                                                                                                           |
| HIGH_TIME        | nsectime    | Timestamp of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                               |
| HIGH             | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| HIGH_SIZE        | long        | Size of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                    |
| LOW_TIME         | nsectime    | Timestamp of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                |
| LOW              | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| LOW_SIZE         | long        | Size of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.                                                                                     |
| LAST_TIME        | nsectime    | Timestamp of the last eligible trade in the current bar interval                                                                                                                                                                       |
| LAST             | double      | Price of the last eligible trade in the current bar interval                                                                                                                                                                           |
| LAST_SIZE        | long        | Size of the last eligible trade in the current bar interval                                                                                                                                                                            |
| VWAP             | double      | Volume-weighted average price                                                                                                                                                                                                          |
| TWAP             | double      | TIme-weighted average price                                                                                                                                                                                                            |
| VOLUME           | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| TRADE_CURRENCY   | string[3]   | Currency in which a trade was executed.                                                                                                                                                                                                |
| TRADE_TICK_COUNT | long        | Number of eligible trades in the current bar interval                                                                                                                                                                                  |
| CLOUD_DB         | string[32]  | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.                                                                             |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP_SAMPLE_BARS - VWAP_1H

1-hour VWAP bars

#### US_COMP_SAMPLE_BARS - VWAP_1H Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| VWAP        | double      | Volume-weighted average price                                                                                                                                                                                                          |
| TWAP        | double      | TIme-weighted average price                                                                                                                                                                                                            |
| VOLUME      | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| CURRENCY    | string[64]  | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| CLOUD_DB    | string[32]  | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.                                                                             |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |



## US_COMP_SAMPLE_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### US_COMP_SAMPLE_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### US_COMP_SAMPLE_DAILY - DAY Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME            | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP              | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCHANGE               | string[4]   | Exchange from which the update originates                                                                                                                                                                                              |
| OPEN                   | double      | Open price for the current trading day                                                                                                                                                                                                 |
| HIGH                   | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW                    | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| CLOSE                  | double      | Closing price                                                                                                                                                                                                                          |
| VOLUME                 | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VWAP                   | double      | Volume-weighted average price                                                                                                                                                                                                          |
| PRICE_OPENING_AUCTION  | double      | Price of the Opening Auction                                                                                                                                                                                                           |
| VOLUME_OPENING_AUCTION | long        | Volume of the Opening Auction                                                                                                                                                                                                          |
| PRICE_CLOSING_AUCTION  | double      | Price of the Closing Auction                                                                                                                                                                                                           |
| VOLUME_CLOSING_AUCTION | long        | Volume of the Closing Auction                                                                                                                                                                                                          |
| VOLUME_MAIN_SESSION    | long        | Volume of the Main Trading Session                                                                                                                                                                                                     |
| VOLUME_PRE_MARKET      | long        | Volume of the Pre-Market Trading Session                                                                                                                                                                                               |
| VOLUME_POST_MARKET     | long        | Volume of the Post-Market Trading Session                                                                                                                                                                                              |
| VOLUME_ODD_LOT         | long        | Volume of the Odd Lot Trades                                                                                                                                                                                                           |
| VOLUME_ROUND_LOT       | long        | Volume of Round Lot Trades                                                                                                                                                                                                             |
| VOLUME_OFF_EXCHANGE    | long        | Volume of Off Exchange Trades                                                                                                                                                                                                          |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP_SAMPLE_DAILY - STAT

Static data, e.g. ISIN, description, security type

#### US_COMP_SAMPLE_DAILY - STAT Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                                                            |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME        | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP          | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| NAME               | string[200] | Description of the instrument                                                                                                                                                                                                          |
| SIP_SYMBOL         | string[16]  | Ticker symbol used by the US Securities Information Processor (CTA / UTP)                                                                                                                                                              |
| PREV_SYMBOL        | string[16]  | Previous ticker symbol, in the event of a symbol change                                                                                                                                                                                |
| PRIMARY_MIC        | string[4]   | MIC of the instrument’s primary listing market, or the reference market for instruments traded on an MTF                                                                                                                               |
| SEC_TYPE           | string[30]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| NYSE_INDUSTRY_CODE | string[4]   | Industry classification, as defined by NYSE                                                                                                                                                                                            |
| LOT_SIZE           | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| CONSOLIDATED_TAPE  | string[1]   | Consolidated Tape on which a US security is published (A/B/C).                                                                                                                                                                         |
| TEST_SYMBOL        | string[1]   | Y - Test symbol, N - Not a test symbol                                                                                                                                                                                                 |
| TICK_PILOT_IND     | string[20]  | Specifies any tick size pilot initiatives in which the instrument is participating                                                                                                                                                     |
| LISTING_DATE       | string[8]   | Date when the instrument was listed (YYYYMMDD)                                                                                                                                                                                         |
| SHARES_OUTSTANDING | long        | Shares / quantity outstanding                                                                                                                                                                                                          |
| OMDSEQ             | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
