# US Consolidated Equities (exc. OTC) Schemas

Consolidated data from all US equities exchanges excluding OTC traded securities.  Provides from the US SIP (CTA/UTP)




## US_COMP

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* NBBO - National Best Bid / Offer quotes
* NBBO_COMP - Best National Best Bid / Offer quotes from Even and Odd Lots
* QTE - Best bid / offer quotes
* QTE_COMP - Best Bid & Offer Quotes from Even and Odd Lots
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### US_COMP - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### US_COMP - DAY Table Schema

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
| TRADE_COUNT            | long        | Number of trades on the current trading day                                                                                                                                                                                            |
| TRADE_VALUE            | double      | Total monetary value traded on the current trading day.  Note: The value will typically be rounded to the nearest integer.                                                                                                             |
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

### US_COMP - LULD

Limit Up / Limit Down price levels

#### US_COMP - LULD Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| SEQ_NUM     | long        | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds                                                                                        |
| LOW_LIMIT   | double      | Lower trading limit / circuit breaker level                                                                                                                                                                                            |
| HIGH_LIMIT  | double      | Upper trading limit / circuit breaker level                                                                                                                                                                                            |
| LULD_IND    | string[1]   | Type of Limit Up / Limit Down (LULD) price update                                                                                                                                                                                      |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP - MKT

Market phase / instrument status information

#### US_COMP - MKT Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME            | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP              | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME              | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| EXCHANGE               | string[1]   | Exchange from which the update originates                                                                                                                                                                                              |
| SEQ_NUM                | long        | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds                                                                                        |
| TRADING_STATUS         | string[1]   | Indicates whether the instrument is subject to a halt or suspension                                                                                                                                                                    |
| REASON_CODE            | string[6]   | Reason for an instrument status update                                                                                                                                                                                                 |
| SHORT_SALE_RESTRICTION | string[1]   | Indicates whether short selling is permitted                                                                                                                                                                                           |
| PARTICIPANT_TIME       | nsectime    | Event timestamp (e.g. trade execution time), as provided by one of the participant exchanges in a consolidated feed                                                                                                                    |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP - NBBO

National Best Bid / Offer quotes

#### US_COMP - NBBO Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME    | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP      | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| BID_PRICE      | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE       | int         | Best bid size                                                                                                                                                                                                                          |
| BID_SIZE_TOTAL | int         | Total size at the (national) best bid price across all participant markets                                                                                                                                                             |
| BID_EXCHANGE   | string[1]   | Exchange that set the best bid                                                                                                                                                                                                         |
| ASK_PRICE      | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE       | int         | Best ask size                                                                                                                                                                                                                          |
| ASK_SIZE_TOTAL | int         | Total size at the (national) best ask price across all participant markets                                                                                                                                                             |
| ASK_EXCHANGE   | string[1]   | Exchange that set the best ask                                                                                                                                                                                                         |
| IS_PRE_OPEN    | int         | Indicates whether a quote originates from the period before (1) or after (0) the instrument has opened on the primary market                                                                                                           |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP - NBBO_COMP

Best National Best Bid / Offer quotes from Even and Odd Lots

#### US_COMP - NBBO_COMP Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME    | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP      | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| BID_PRICE      | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE       | int         | Best bid size                                                                                                                                                                                                                          |
| BID_SIZE_TOTAL | int         | Total size at the (national) best bid price across all participant markets                                                                                                                                                             |
| BID_EXCHANGE   | string[1]   | Exchange that set the best bid                                                                                                                                                                                                         |
| ASK_PRICE      | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE       | int         | Best ask size                                                                                                                                                                                                                          |
| ASK_SIZE_TOTAL | int         | Total size at the (national) best ask price across all participant markets                                                                                                                                                             |
| ASK_EXCHANGE   | string[1]   | Exchange that set the best ask                                                                                                                                                                                                         |
| IS_PRE_OPEN    | int         | Indicates whether a quote originates from the period before (1) or after (0) the instrument has opened on the primary market                                                                                                           |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP - QTE

Best bid / offer quotes

#### US_COMP - QTE Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                                                            |
|---------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME         | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP           | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME           | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| SEQ_NUM             | long        | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds                                                                                        |
| EXCHANGE            | string[1]   | Exchange from which the update originates                                                                                                                                                                                              |
| SOURCE              | string[1]   | Source from which an update originates                                                                                                                                                                                                 |
| BID_PRICE           | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE            | long        | Best bid size                                                                                                                                                                                                                          |
| ASK_PRICE           | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE            | long        | Best ask size                                                                                                                                                                                                                          |
| QUOTE_COND          | string[1]   | Indicates any special conditions applicable to a quote                                                                                                                                                                                 |
| RPI                 | string[1]   | Indicates the presence of Retail Price Improvement interest on bid and/or ask side                                                                                                                                                     |
| RESTRICTION_IND     | string[1]   | Indicates whether short selling is permitted                                                                                                                                                                                           |
| NBBO_IND            | string[1]   | Indicates whether the quote affects the NBBO                                                                                                                                                                                           |
| SIP_MSG_ID          | string[1]   | Identifies messages generated by the SIP ( - Originates from an exchange, E - UTP, S - Consolidated Tape System)                                                                                                                       |
| LULD_BBO_IND        | string[1]   | Indicates whether the bid/ask crosses the upper / lower LULD price bands                                                                                                                                                               |
| NBBO_LULD_IND       | string[1]   | Indicates whether the NBBO crosses the upper / lower LULD price bands                                                                                                                                                                  |
| FINRA_ADF_TIME      | nsectime    | Timestamp provided by a FINRA ADF                                                                                                                                                                                                      |
| FINRA_ADF_IND       | string[1]   | Indicates whether the quote reflects the FINRA BBO                                                                                                                                                                                     |
| FINRA_BBO_IND       | string[1]   | Indicates whether the quote affects the FINRA BBO [currently unused]                                                                                                                                                                   |
| FINRA_ADF_MPID_IND  | string[1]   | Indicates whether a FINRA participant ID is available for a BBO quote [currently unused]                                                                                                                                               |
| SECURITY_STATUS_IND | string[2]   | Security status                                                                                                                                                                                                                        |
| PARTICIPANT_TIME    | nsectime    | Event timestamp (e.g. trade execution time), as provided by one of the participant exchanges in a consolidated feed                                                                                                                    |
| COND                | string[1]   | Condition code                                                                                                                                                                                                                         |
| CORR                | string[1]   | Type of trade correction / cancellation                                                                                                                                                                                                |
| TICKER              | string[16]  | Ticker symbol, as specified by the data source                                                                                                                                                                                         |
| OMDSEQ              | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP - QTE_COMP

Best Bid & Offer Quotes from Even and Odd Lots

#### US_COMP - QTE_COMP Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME     | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP       | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME       | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| SEQ_NUM         | long        | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds                                                                                        |
| EXCHANGE        | string[1]   | Exchange from which the update originates                                                                                                                                                                                              |
| SOURCE          | string[1]   | Source from which an update originates                                                                                                                                                                                                 |
| BID_PRICE       | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE        | int         | Best bid size                                                                                                                                                                                                                          |
| ASK_PRICE       | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE        | int         | Best ask size                                                                                                                                                                                                                          |
| QUOTE_COND      | string[1]   | Indicates any special conditions applicable to a quote                                                                                                                                                                                 |
| RPI             | string[1]   | Indicates the presence of Retail Price Improvement interest on bid and/or ask side                                                                                                                                                     |
| RESTRICTION_IND | string[1]   | Indicates whether short selling is permitted                                                                                                                                                                                           |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP - STAT

Static data, e.g. ISIN, description, security type

#### US_COMP - STAT Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                                                            |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME        | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP          | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| NAME               | string[200] | Description of the instrument                                                                                                                                                                                                          |
| SIP_SYMBOL         | string[16]  | Ticker symbol used by the US Securities Information Processor (CTA / UTP)                                                                                                                                                              |
| PREV_SYMBOL        | string[16]  | Previous ticker symbol, in the event of a symbol change                                                                                                                                                                                |
| PRIMARY_MIC        | string[4]   | MIC of the instrument’s primary listing market, or the reference market for instruments traded on an MTF                                                                                                                               |
| SEC_TYPE           | string[30]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| CURRENCY           | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| NYSE_INDUSTRY_CODE | string[4]   | Industry classification, as defined by NYSE                                                                                                                                                                                            |
| LOT_SIZE           | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| CONSOLIDATED_TAPE  | string[1]   | Consolidated Tape on which a US security is published (A/B/C).                                                                                                                                                                         |
| TEST_SYMBOL        | string[1]   | Y - Test symbol, N - Not a test symbol                                                                                                                                                                                                 |
| TICK_PILOT_IND     | string[20]  | Specifies any tick size pilot initiatives in which the instrument is participating                                                                                                                                                     |
| LISTING_DATE       | string[8]   | Date when the instrument was listed (YYYYMMDD)                                                                                                                                                                                         |
| SHARES_OUTSTANDING | long        | Shares / quantity outstanding                                                                                                                                                                                                          |
| OMDSEQ             | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP - TRD

Trades

#### US_COMP - TRD Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME      | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP        | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME        | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| TRF_TIME         | nsectime    | Time at which a trade was processed by the Trade Reporting Facility (for trades reported to FINRA)                                                                                                                                     |
| EXCHANGE         | string[1]   | Exchange from which the update originates                                                                                                                                                                                              |
| TRF              | string[1]   | Trade Reporting Facility used to report a trade (for trades reported to FINRA)                                                                                                                                                         |
| SOURCE           | string[1]   | Source from which an update originates                                                                                                                                                                                                 |
| PRICE            | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE             | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| FRACTIONAL_SIZE  | double      | Trade size, as a floating-point number                                                                                                                                                                                                 |
| AGGRESSOR_SIDE   | string[1]   | Indicates whether a trade resulted from an incoming buy or sell order.                                                                                                                                                                 |
| TRADE_TYPE       | string[4]   | Type of trade                                                                                                                                                                                                                          |
| TRADE_PERIOD     | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                       |
| BOOK_TYPE        | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                            |
| STOP_STOCK       | string[1]   | Y - Stopped stock trade, N - Not a stopped stock trade,  - Not applicable                                                                                                                                                              |
| TTE              | string[1]   | Indicates whether a trade is exempt from the Trade Through Rule (1 - Trade Through Exempt, 0 - No Trade Through Exemption)                                                                                                             |
| TRADE_ID         | string[20]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| SEQ_NUM          | long        | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds                                                                                        |
| CORR             | int         | Type of trade correction / cancellation                                                                                                                                                                                                |
| PARTICIPANT_TIME | nsectime    | Event timestamp (e.g. trade execution time), as provided by one of the participant exchanges in a consolidated feed                                                                                                                    |
| COND             | string[4]   | Condition code                                                                                                                                                                                                                         |
| TICKER           | string[16]  | Ticker symbol, as specified by the data source                                                                                                                                                                                         |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| DELETED_TIME     | nsectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS      | byte        | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |



## US_COMP_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* LAT_1M - 1-minute Latency bars for real time delivered data
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars



### US_COMP_BARS - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### US_COMP_BARS - DAY Table Schema

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

### US_COMP_BARS - LAT_1M

1-minute Latency bars for real time delivered data

#### US_COMP_BARS - LAT_1M Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME            | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP              | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| AVG_LATENCY_COLLECTION | double      | Average Latency of Real Time Collection.  Difference between Exchange timestamp and collection timestamp.                                                                                                                              |
| MAX_LATENCY_COLLECTION | double      | Maximum Latency of Real Time Collection.  Difference between Exchange timestamp and collection timestamp.                                                                                                                              |
| AVG_LATENCY_LOAD       | double      | Average Latency of Real Time Loading.  Difference between the collection timestamp and availability within the Memory Database.                                                                                                        |
| MAX_LATENCY_LOAD       | double      | Maximum Latency of Real Time Loading.  Difference between the collection timestamp and availability within the Memory Database.                                                                                                        |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP_BARS - MKT

Market phase / instrument status information

#### US_COMP_BARS - MKT Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME            | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP              | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| OMD_STATUS             | string[64]  | Indicates an instrument’s current trading status. Values are normalized across all DBs.                                                                                                                                                |
| EXCH_TIME              | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| EXCHANGE               | string[1]   | Exchange from which the update originates                                                                                                                                                                                              |
| SEQ_NUM                | long        | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds                                                                                        |
| TRADING_STATUS         | string[1]   | Indicates whether the instrument is subject to a halt or suspension                                                                                                                                                                    |
| REASON_CODE            | string[6]   | Reason for an instrument status update                                                                                                                                                                                                 |
| SHORT_SALE_RESTRICTION | string[1]   | Indicates whether short selling is permitted                                                                                                                                                                                           |
| PARTICIPANT_TIME       | nsectime    | Event timestamp (e.g. trade execution time), as provided by one of the participant exchanges in a consolidated feed                                                                                                                    |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP_BARS - QTE_1M

1-minute quote bars

#### US_COMP_BARS - QTE_1M Table Schema

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

### US_COMP_BARS - TRD_1D

Daily trade bars

#### US_COMP_BARS - TRD_1D Table Schema

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
| BUY_VOLUME       | long        | Traded volume originating from incoming buy orders.  Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| SELL_VOLUME      | long        | Traded volume originating from incoming sell orders. Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| TRADE_CURRENCY   | string[3]   | Currency in which a trade was executed.                                                                                                                                                                                                |
| TRADE_TICK_COUNT | long        | Number of eligible trades in the current bar interval                                                                                                                                                                                  |
| CLOUD_DB         | string[32]  | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.                                                                             |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP_BARS - TRD_1M

1-minute trade bars

#### US_COMP_BARS - TRD_1M Table Schema

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
| BUY_VOLUME       | long        | Traded volume originating from incoming buy orders.  Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| SELL_VOLUME      | long        | Traded volume originating from incoming sell orders. Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.                   |
| TRADE_CURRENCY   | string[3]   | Currency in which a trade was executed.                                                                                                                                                                                                |
| TRADE_TICK_COUNT | long        | Number of eligible trades in the current bar interval                                                                                                                                                                                  |
| CLOUD_DB         | string[32]  | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.                                                                             |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP_BARS - VWAP_1H

1-hour VWAP bars

#### US_COMP_BARS - VWAP_1H Table Schema

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



## US_COMP_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* EVENT - Events such as Earnings, and Company Conference Calls
* STAT - Static data, e.g. ISIN, description, security type



### US_COMP_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### US_COMP_DAILY - DAY Table Schema

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
| TRADE_COUNT            | long        | Number of trades on the current trading day                                                                                                                                                                                            |
| TRADE_VALUE            | double      | Total monetary value traded on the current trading day.  Note: The value will typically be rounded to the nearest integer.                                                                                                             |
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

### US_COMP_DAILY - EVENT

Events such as Earnings, and Company Conference Calls

#### US_COMP_DAILY - EVENT Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME     | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP       | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EVENT_TYPE      | string[40]  | Type of Event. EARNING_DATE or COMPANY_CONFERENCE_CALL                                                                                                                                                                                 |
| EVENT_CONDITION | string[20]  | Event Condition                                                                                                                                                                                                                        |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP_DAILY - STAT

Static data, e.g. ISIN, description, security type

#### US_COMP_DAILY - STAT Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                                                            |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME        | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP          | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| NAME               | string[200] | Description of the instrument                                                                                                                                                                                                          |
| SIP_SYMBOL         | string[16]  | Ticker symbol used by the US Securities Information Processor (CTA / UTP)                                                                                                                                                              |
| PREV_SYMBOL        | string[16]  | Previous ticker symbol, in the event of a symbol change                                                                                                                                                                                |
| PRIMARY_MIC        | string[4]   | MIC of the instrument’s primary listing market, or the reference market for instruments traded on an MTF                                                                                                                               |
| SEC_TYPE           | string[30]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| CURRENCY           | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| NYSE_INDUSTRY_CODE | string[4]   | Industry classification, as defined by NYSE                                                                                                                                                                                            |
| LOT_SIZE           | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| CONSOLIDATED_TAPE  | string[1]   | Consolidated Tape on which a US security is published (A/B/C).                                                                                                                                                                         |
| TEST_SYMBOL        | string[1]   | Y - Test symbol, N - Not a test symbol                                                                                                                                                                                                 |
| TICK_PILOT_IND     | string[20]  | Specifies any tick size pilot initiatives in which the instrument is participating                                                                                                                                                     |
| LISTING_DATE       | string[8]   | Date when the instrument was listed (YYYYMMDD)                                                                                                                                                                                         |
| SHARES_OUTSTANDING | long        | Shares / quantity outstanding                                                                                                                                                                                                          |
| OMDSEQ             | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |



## US_COMP_LATEST

Database includes the following tick types:

* SNAP - Latest Trade & Quote / NBBO Prices for all Instruments in the venue
* SNAP_NBBO - Latest NBBO for all Instruments in the venue
* SNAP_TRD - Latest Trade Prices for all Traded Instruments in the venue



### US_COMP_LATEST - SNAP

Latest Trade & Quote / NBBO Prices for all Instruments in the venue

#### US_COMP_LATEST - SNAP Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                               |
|---------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME         | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                            |
| TIMESTAMP           | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                   |
| PRICE               | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross |
| SIZE                | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross          |
| TRADE_CURRENCY      | string[3]   | Currency in which a trade was executed.                                                                                                                                                                   |
| OPEN                | double      | Open price for the current trading day                                                                                                                                                                    |
| CLOSE               | double      | Closing price                                                                                                                                                                                             |
| CLOSE_DATE          | string[10]  | Date for Closing Price                                                                                                                                                                                    |
| LATENCY_LOAD        | long        | Latency in milliseconds for the time duration between data collection and in-memory database load                                                                                                         |
| LATENCY_COLLECTION  | long        | Latency in milliseconds for the time duration between exchange publishing and data collection                                                                                                             |
| VOLUME              | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                         |
| VOLUME_MAIN_SESSION | long        | Volume of the Main Trading Session                                                                                                                                                                        |
| VOLUME_EXTENDED     | long        | Volume of the Pre and Post-Market Trading Sessions                                                                                                                                                        |
| HIGH                | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                               |
| LOW                 | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                |
| SYMBOL              | string[64]  | Exchange Symbol                                                                                                                                                                                           |
| LAST_TRADE_TIME     | nsectime    | Last Trade Time                                                                                                                                                                                           |
| BID_PRICE           | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                          |
| ASK_PRICE           | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                          |
| LAST_QUOTE_TIME     | nsectime    | Last Quote Time                                                                                                                                                                                           |

### US_COMP_LATEST - SNAP_NBBO

Latest NBBO for all Instruments in the venue

#### US_COMP_LATEST - SNAP_NBBO Table Schema

| Field          | Data Type   | Description                                                                                                                                                    |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME    | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate) |
| TIMESTAMP      | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                        |
| BID_PRICE      | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                               |
| BID_SIZE       | long        | Best bid size                                                                                                                                                  |
| ASK_PRICE      | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                               |
| ASK_SIZE       | long        | Best ask size                                                                                                                                                  |
| QUOTE_CURRENCY | string[3]   | Currency in which a quote price is expressed.                                                                                                                  |
| SYMBOL         | string[64]  | Exchange Symbol                                                                                                                                                |
| TICK_TIME      | nsectime    | Timestamp for latest Trade / Quote or NBBO Update                                                                                                              |

### US_COMP_LATEST - SNAP_TRD

Latest Trade Prices for all Traded Instruments in the venue

#### US_COMP_LATEST - SNAP_TRD Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                               |
|---------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME         | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                            |
| TIMESTAMP           | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                   |
| PRICE               | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross |
| SIZE                | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross          |
| TRADE_CURRENCY      | string[3]   | Currency in which a trade was executed.                                                                                                                                                                   |
| OPEN                | double      | Open price for the current trading day                                                                                                                                                                    |
| CLOSE               | double      | Closing price                                                                                                                                                                                             |
| CLOSE_DATE          | string[10]  | Date for Closing Price                                                                                                                                                                                    |
| LATENCY_LOAD        | long        | Latency in milliseconds for the time duration between data collection and in-memory database load                                                                                                         |
| LATENCY_COLLECTION  | long        | Latency in milliseconds for the time duration between exchange publishing and data collection                                                                                                             |
| VOLUME              | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                         |
| VOLUME_MAIN_SESSION | long        | Volume of the Main Trading Session                                                                                                                                                                        |
| VOLUME_EXTENDED     | long        | Volume of the Pre and Post-Market Trading Sessions                                                                                                                                                        |
| HIGH                | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                               |
| LOW                 | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                |
| SYMBOL              | string[64]  | Exchange Symbol                                                                                                                                                                                           |
| TICK_TIME           | nsectime    | Timestamp for latest Trade / Quote or NBBO Update                                                                                                                                                         |



## US_COMP_MKT_SHARE

Database includes the following tick types:

* QTE_NBBO_DAY - Daily Quote Metrics by Venue related to the NBBO
* TRD_NBBO_DAY - Daily Trade Metrics by Venue related to the NBBO



### US_COMP_MKT_SHARE - QTE_NBBO_DAY

Daily Quote Metrics by Venue related to the NBBO

#### US_COMP_MKT_SHARE - QTE_NBBO_DAY Table Schema

| Field                   | Data Type   | Description                                                                                                                                                    |
|-------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME             | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate) |
| TIMESTAMP               | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                        |
| NBBO_DURATION           | double      | Main Session Duration in seconds that a valid NBBO is present                                                                                                  |
| AT_NBBO_BOTH_DURATION   | double      | Main Session Duration in seconds for the exchange to be at both the NBBO Bid and Ask                                                                           |
| AT_NBBO_BID_DURATION    | double      | Main Session Duration in seconds for the exchange to be at the NBBO Bid                                                                                        |
| AT_NBBO_ASK_DURATION    | double      | Main Session Duration in seconds for the exchange to be at the NBBO Ask                                                                                        |
| AT_NBBO_EITHER_DURATION | double      | Main Session Duration in seconds for the exchange to be at either or both the NBBO Bid or Ask                                                                  |
| AT_NBBO_BOTH_SIZE       | double      | Main Session Time Weighted Average of the sum of BID_SIZE and ASK_SIZE from Exchange, when at the NBBO                                                         |
| AT_NBBO_BID_SIZE        | double      | Main Session Time Weighted Average of the BID_SIZE from Exchange, when at the NBBO Bid                                                                         |
| AT_NBBO_ASK_SIZE        | double      | Main Session Time Weighted Average of the ASK_SIZE from Exchange, when at the NBBO Ask                                                                         |
| AT_NBBO_EITHER_SIZE     | double      | Main Session Time Weighted Average of the Bid and Ask Size from Exchange, when at either or both the NBBO Bid or Ask.  Size not at NBBO is not included.       |
| EXCHANGE                | string[1]   | Exchange from which the update originates                                                                                                                      |

### US_COMP_MKT_SHARE - TRD_NBBO_DAY

Daily Trade Metrics by Venue related to the NBBO

#### US_COMP_MKT_SHARE - TRD_NBBO_DAY Table Schema

| Field                       | Data Type   | Description                                                                                                                                                    |
|-----------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME                 | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate) |
| TIMESTAMP                   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                        |
| TRADE_VALUE                 | double      | Total monetary value traded on the current trading day.  Note: The value will typically be rounded to the nearest integer.                                     |
| TRADE_COUNT                 | double      | Number of trades on the current trading day                                                                                                                    |
| VOLUME                      | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                              |
| TRADE_VALUE_MAIN_SESSION    | double      | Main Session Trade Value                                                                                                                                       |
| VOLUME_MAIN_SESSION         | double      | Volume of the Main Trading Session                                                                                                                             |
| TRADE_COUNT_MAIN_SESSION    | double      | Main Session Trade Count                                                                                                                                       |
| TRADE_VALUE_AT_MID          | double      | Main Session Traded Value for Trades at the NBBO Mid                                                                                                           |
| TRADE_VALUE_AT_NBBO         | double      | Main Session Traded Value for Trades at the NBBO                                                                                                               |
| TRADE_VALUE_INSIDE_NBBO     | double      | Main Session Traded Value for Trades inside the NBBO, excluding Mid                                                                                            |
| TRADE_VALUE_OUTSIDE_NBBO    | double      | Main Session Traded Value for Trades outside the NBBO                                                                                                          |
| TRADE_COUNT_AT_MID          | double      | Main Session Trade Count for Trades at the NBBO Mid                                                                                                            |
| TRADE_COUNT_AT_NBBO         | double      | Main Session Trade Count for Trades at the NBBO                                                                                                                |
| TRADE_COUNT_INSIDE_NBBO     | double      | Main Session Trade Count for Trades inside the NBBO, excluding Mid                                                                                             |
| TRADE_COUNT_OUTSIDE_NBBO    | double      | Main Session Trade Count for Trades outside the NBBO                                                                                                           |
| VOLUME_AT_MID               | double      | Main Session Volume for Trades at the NBBO Mid                                                                                                                 |
| VOLUME_AT_NBBO              | double      | Main Session Volume for Trades at the NBBO                                                                                                                     |
| VOLUME_INSIDE_NBBO          | double      | Main Session Volume for Trades inside the NBBO, excluding Mid                                                                                                  |
| VOLUME_OUTSIDE_NBBO         | double      | Main Session Volume for Trades outside the NBBO                                                                                                                |
| VOLUME_OPENING_AUCTION      | double      | Volume of the Opening Auction                                                                                                                                  |
| VOLUME_CLOSING_AUCTION      | double      | Volume of the Closing Auction                                                                                                                                  |
| VOLUME_ODD_LOT              | double      | Volume of the Odd Lot Trades                                                                                                                                   |
| VOLUME_ROUND_LOT            | double      | Volume of Round Lot Trades                                                                                                                                     |
| VOLUME_PRE_MARKET           | double      | Volume of the Pre-Market Trading Session                                                                                                                       |
| VOLUME_POST_MARKET          | double      | Volume of the Post-Market Trading Session                                                                                                                      |
| TRADE_COUNT_OPENING_AUCTION | double      | Trade Count for Opening Auction Trades                                                                                                                         |
| TRADE_COUNT_CLOSING_AUCTION | double      | Trade Count for Closing Auction Trades                                                                                                                         |
| TRADE_COUNT_ODD_LOT         | double      | Trade Count for Odd Lot Trades                                                                                                                                 |
| TRADE_COUNT_ROUND_LOT       | double      | Trade Count for Round Lot Trades                                                                                                                               |
| TRADE_COUNT_PRE_MARKET      | double      | Trade Count of the Pre-Market Trading Session                                                                                                                  |
| TRADE_COUNT_POST_MARKET     | double      | Trade Count of the Post-Market Trading Session                                                                                                                 |
| TRADE_VALUE_OPENING_AUCTION | double      | Trade Value for Opening Auction Trades                                                                                                                         |
| TRADE_VALUE_CLOSING_AUCTION | double      | Trade Value for Closing Auction Trades                                                                                                                         |
| TRADE_VALUE_ODD_LOT         | double      | Traded Value for Odd Lot Trades                                                                                                                                |
| TRADE_VALUE_ROUND_LOT       | double      | Traded Value for Round Lot Trades                                                                                                                              |
| TRADE_VALUE_PRE_MARKET      | double      | Trade Value of the Pre-Market Trading Session                                                                                                                  |
| TRADE_VALUE_POST_MARKET     | double      | Trade Value of the Post-Market Trading Session                                                                                                                 |
| TRADE_VALUE_BLOCK           | double      | Block Traded Value where block is a trade with value > $200,000 or volume > 10,000                                                                             |
| BLOCK_VOLUME                | double      | Total volume of block trades executed on the current day                                                                                                       |
| TRADE_COUNT_BLOCK           | double      | Block Count where block is a trade with value > $200,000 or volume > 10,000                                                                                    |
| EXCHANGE                    | string[1]   | Exchange from which the update originates                                                                                                                      |



## US_COMP_TCA

Database includes the following tick types:

* TRD_TCA - Trades enriched with pravailing quotes / nbbo and offsets



### US_COMP_TCA - TRD_TCA

Trades enriched with pravailing quotes / nbbo and offsets

#### US_COMP_TCA - TRD_TCA Table Schema

| Field             | Data Type   | Description                                                                                                                                                                                                                            |
|-------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME       | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP         | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME         | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| TRF_TIME          | nsectime    | Time at which a trade was processed by the Trade Reporting Facility (for trades reported to FINRA)                                                                                                                                     |
| SEQ_NUM           | long        | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds                                                                                        |
| EXCHANGE          | string[1]   | Exchange from which the update originates                                                                                                                                                                                              |
| TRF               | string[1]   | Trade Reporting Facility used to report a trade (for trades reported to FINRA)                                                                                                                                                         |
| SOURCE            | string[1]   | Source from which an update originates                                                                                                                                                                                                 |
| PRICE             | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SIZE              | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| FRACTIONAL_SIZE   | double      | Trade size, as a floating-point number                                                                                                                                                                                                 |
| AGGRESSOR_SIDE    | string[1]   | Indicates whether a trade resulted from an incoming buy or sell order.                                                                                                                                                                 |
| TRADE_TYPE        | string[4]   | Type of trade                                                                                                                                                                                                                          |
| TRADE_PERIOD      | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                       |
| BOOK_TYPE         | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                            |
| STOP_STOCK        | string[1]   | Y - Stopped stock trade, N - Not a stopped stock trade,  - Not applicable                                                                                                                                                              |
| TTE               | string[1]   | Indicates whether a trade is exempt from the Trade Through Rule (1 - Trade Through Exempt, 0 - No Trade Through Exemption)                                                                                                             |
| TRADE_ID          | string[20]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| CORR              | int         | Type of trade correction / cancellation                                                                                                                                                                                                |
| PARTICIPANT_TIME  | nsectime    | Event timestamp (e.g. trade execution time), as provided by one of the participant exchanges in a consolidated feed                                                                                                                    |
| COND              | string[4]   | Condition code                                                                                                                                                                                                                         |
| TICKER            | string[16]  | Ticker symbol, as specified by the data source                                                                                                                                                                                         |
| TICK_STATUS       | byte        | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| DELETED_TIME      | nsectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| ASK_PRICE         | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_PRICE         | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| MID_PRICE         | double      | Midpoint of the best bid/ask; set to null (NaN) if the book is crossed                                                                                                                                                                 |
| MID_PRICE_B60000  | double      | Mid Price back 60s before the Trade Execution                                                                                                                                                                                          |
| MID_PRICE_B30000  | double      | Mid Price back 30s before the Trade Execution                                                                                                                                                                                          |
| MID_PRICE_B10000  | double      | Mid Price back 10s before the Trade Execution                                                                                                                                                                                          |
| MID_PRICE_B1000   | double      | Mid Price back 1s before the Trade Execution                                                                                                                                                                                           |
| MID_PRICE_B100    | double      | Mid Price back 100ms before the Trade Execution                                                                                                                                                                                        |
| MID_PRICE_B10     | double      | Mid Price back 10ms before the Trade Execution                                                                                                                                                                                         |
| MID_PRICE_F10     | double      | Mid Price forward 10ms after the Trade Execution                                                                                                                                                                                       |
| MID_PRICE_F100    | double      | Mid Price forward 100ms after the Trade Execution                                                                                                                                                                                      |
| MID_PRICE_F500    | double      | Mid Price forward 500ms after the Trade Execution                                                                                                                                                                                      |
| MID_PRICE_F1000   | double      | Mid Price forward 1s after the Trade Execution                                                                                                                                                                                         |
| MID_PRICE_F2000   | double      | Mid Price forward 2s after the Trade Execution                                                                                                                                                                                         |
| MID_PRICE_F5000   | double      | Mid Price forward 5s after the Trade Execution                                                                                                                                                                                         |
| MID_PRICE_F10000  | double      | Mid Price forward 10s after the Trade Execution                                                                                                                                                                                        |
| MID_PRICE_F30000  | double      | Mid Price forward 30s after the Trade Execution                                                                                                                                                                                        |
| MID_PRICE_F60000  | double      | Mid Price forward 1min after the Trade Execution                                                                                                                                                                                       |
| MID_PRICE_F90000  | double      | Mid Price forward 90s after the Trade Execution                                                                                                                                                                                        |
| MID_PRICE_F120000 | double      | Mid Price forward 2mins after the Trade Execution                                                                                                                                                                                      |
| MID_PRICE_F180000 | double      | Mid Price forward 3mins after the Trade Execution                                                                                                                                                                                      |
| MID_PRICE_F300000 | double      | Mid Price forward 5mins after the Trade Execution                                                                                                                                                                                      |
| MID_PRICE_F600000 | double      | Mid Price forward 10mins after the Trade Execution                                                                                                                                                                                     |
| MID_PRICE_F900000 | double      | Mid Price forward 15mins after the Trade Execution                                                                                                                                                                                     |
| OMDSEQ            | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
