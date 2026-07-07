# US Consolidated Equity Replay for Intraday / CEP Schemas

Consolidated data from all US equities exchanges, replayed and available for testing intraday access plus CEP / stream processing




## US_COMP_REPLAY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* NBBO - National Best Bid / Offer quotes
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades



### US_COMP_REPLAY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### US_COMP_REPLAY - DAY Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOSE                  | double      | Closing price                                                                                                                                                                                                                          |
| EXCHANGE               | string[4]   | Exchange from which the update originates                                                                                                                                                                                              |
| HIGH                   | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW                    | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN                   | double      | Open price for the current trading day                                                                                                                                                                                                 |
| PRICE_CLOSING_AUCTION  | double      | Price of the Closing Auction                                                                                                                                                                                                           |
| PRICE_OPENING_AUCTION  | double      | Price of the Opening Auction                                                                                                                                                                                                           |
| VOLUME                 | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VOLUME_CLOSING_AUCTION | long        | Volume of the Closing Auction                                                                                                                                                                                                          |
| VOLUME_MAIN_SESSION    | long        | Volume of the Main Trading Session                                                                                                                                                                                                     |
| VOLUME_ODD_LOT         | long        | Volume of the Odd Lot Trades                                                                                                                                                                                                           |
| VOLUME_OFF_EXCHANGE    | long        | Volume of Off Exchange Trades                                                                                                                                                                                                          |
| VOLUME_OPENING_AUCTION | long        | Volume of the Opening Auction                                                                                                                                                                                                          |
| VOLUME_POST_MARKET     | long        | Volume of the Post-Market Trading Session                                                                                                                                                                                              |
| VOLUME_PRE_MARKET      | long        | Volume of the Pre-Market Trading Session                                                                                                                                                                                               |
| VOLUME_ROUND_LOT       | long        | Volume of Round Lot Trades                                                                                                                                                                                                             |
| VWAP                   | double      | Volume-weighted average price                                                                                                                                                                                                          |

### US_COMP_REPLAY - IND

Indicative pricing, e.g. indicative auction prices and imbalance

#### US_COMP_REPLAY - IND Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                                                            |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCHANGE           | string[1]   | Exchange from which the update originates                                                                                                                                                                                              |
| EXCH_TIME          | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| IMB_SIDE           | string[1]   | Indicates if one side of the orderbook has excess executable orders during an auction phase.                                                                                                                                           |
| IMB_VOLUME         | long        | Size of an auction imbalance, i.e. the excess volume of orders on the side indicated by IMB_SIDE                                                                                                                                       |
| IND_TYPE           | string[1]   | Type of indicative price update                                                                                                                                                                                                        |
| OMDSEQ             | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPENING_RANGE_HIGH | double      | Upper end of the expected opening price range                                                                                                                                                                                          |
| OPENING_RANGE_LOW  | double      | Lower end of the expected opening price range                                                                                                                                                                                          |
| PARTICIPANT_TIME   | nsectime    | Event timestamp (e.g. trade execution time), as provided by one of the participant exchanges in a consolidated feed                                                                                                                    |
| SEQ_NUM            | long        | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds                                                                                        |

### US_COMP_REPLAY - LULD

Limit Up / Limit Down price levels

#### US_COMP_REPLAY - LULD Table Schema

| Field      | Data Type   | Description                                                                                                                                                                                                                            |
|------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HIGH_LIMIT | double      | Upper trading limit / circuit breaker level                                                                                                                                                                                            |
| LOW_LIMIT  | double      | Lower trading limit / circuit breaker level                                                                                                                                                                                            |
| LULD_IND   | string[2]   | Type of Limit Up / Limit Down (LULD) price update                                                                                                                                                                                      |
| OMDSEQ     | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| SEQ_NUM    | long        | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds                                                                                        |

### US_COMP_REPLAY - MKT

Market phase / instrument status information

#### US_COMP_REPLAY - MKT Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCHANGE               | string[1]   | Exchange from which the update originates                                                                                                                                                                                              |
| EXCH_TIME              | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PARTICIPANT_TIME       | nsectime    | Event timestamp (e.g. trade execution time), as provided by one of the participant exchanges in a consolidated feed                                                                                                                    |
| REASON_CODE            | string[6]   | Reason for an instrument status update                                                                                                                                                                                                 |
| SEQ_NUM                | long        | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds                                                                                        |
| SHORT_SALE_RESTRICTION | string[1]   | Indicates whether short selling is permitted                                                                                                                                                                                           |
| TRADING_STATUS         | string[1]   | Indicates whether the instrument is subject to a halt or suspension                                                                                                                                                                    |

### US_COMP_REPLAY - NBBO

National Best Bid / Offer quotes

#### US_COMP_REPLAY - NBBO Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_EXCHANGE   | string[2]   | Exchange that set the best ask                                                                                                                                                                                                         |
| ASK_PRICE      | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE       | int         | Best ask size                                                                                                                                                                                                                          |
| ASK_SIZE_TOTAL | int         | Total size at the (national) best ask price across all participant markets                                                                                                                                                             |
| BID_EXCHANGE   | string[2]   | Exchange that set the best bid                                                                                                                                                                                                         |
| BID_PRICE      | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE       | int         | Best bid size                                                                                                                                                                                                                          |
| BID_SIZE_TOTAL | int         | Total size at the (national) best bid price across all participant markets                                                                                                                                                             |
| IS_PRE_OPEN    | int         | Indicates whether a quote originates from the period before (1) or after (0) the instrument has opened on the primary market                                                                                                           |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP_REPLAY - QTE

Best bid / offer quotes

#### US_COMP_REPLAY - QTE Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                                                            |
|---------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_PRICE           | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE            | long        | Best ask size                                                                                                                                                                                                                          |
| BID_PRICE           | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE            | long        | Best bid size                                                                                                                                                                                                                          |
| COND                | string[1]   | Condition code                                                                                                                                                                                                                         |
| CORR                | string[1]   | Type of trade correction / cancellation                                                                                                                                                                                                |
| DELETED_TIME        | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| EXCHANGE            | string[1]   | Exchange from which the update originates                                                                                                                                                                                              |
| EXCH_TIME           | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| FINRA_ADF_IND       | string[1]   | Indicates whether the quote reflects the FINRA BBO                                                                                                                                                                                     |
| FINRA_ADF_MPID_IND  | string[1]   | Indicates whether a FINRA participant ID is available for a BBO quote [currently unused]                                                                                                                                               |
| FINRA_ADF_TIME      | nsectime    | Timestamp provided by a FINRA ADF                                                                                                                                                                                                      |
| FINRA_BBO_IND       | string[1]   | Indicates whether the quote affects the FINRA BBO [currently unused]                                                                                                                                                                   |
| LULD_BBO_IND        | string[1]   | Indicates whether the bid/ask crosses the upper / lower LULD price bands                                                                                                                                                               |
| NBBO_IND            | string[1]   | Indicates whether the quote affects the NBBO                                                                                                                                                                                           |
| NBBO_LULD_IND       | string[1]   | Indicates whether the NBBO crosses the upper / lower LULD price bands                                                                                                                                                                  |
| OMDSEQ              | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PARTICIPANT_TIME    | nsectime    | Event timestamp (e.g. trade execution time), as provided by one of the participant exchanges in a consolidated feed                                                                                                                    |
| QUOTE_COND          | string[1]   | Indicates any special conditions applicable to a quote                                                                                                                                                                                 |
| RESTRICTION_IND     | string[1]   | Indicates whether short selling is permitted                                                                                                                                                                                           |
| RPI                 | string[1]   | Indicates the presence of Retail Price Improvement interest on bid and/or ask side                                                                                                                                                     |
| SECURITY_STATUS_IND | string[2]   | Security status                                                                                                                                                                                                                        |
| SEQ_NUM             | long        | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds                                                                                        |
| SIP_MSG_ID          | string[1]   | Identifies messages generated by the SIP ( - Originates from an exchange, E - UTP, S - Consolidated Tape System)                                                                                                                       |
| SOURCE              | string[1]   | Source from which an update originates                                                                                                                                                                                                 |
| TICKER              | string[16]  | Ticker symbol, as specified by the data source                                                                                                                                                                                         |
| TICK_STATUS         | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |

### US_COMP_REPLAY - STAT

Static data, e.g. ISIN, description, security type

#### US_COMP_REPLAY - STAT Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                                                            |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONSOLIDATED_TAPE  | string[1]   | Consolidated Tape on which a US security is published (A/B/C).                                                                                                                                                                         |
| LISTING_DATE       | string[8]   | Date when the instrument was listed (YYYYMMDD)                                                                                                                                                                                         |
| LOT_SIZE           | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| NAME               | string[200] | Description of the instrument                                                                                                                                                                                                          |
| NYSE_INDUSTRY_CODE | string[4]   | Industry classification, as defined by NYSE                                                                                                                                                                                            |
| OMDSEQ             | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PREV_SYMBOL        | string[16]  | Previous ticker symbol, in the event of a symbol change                                                                                                                                                                                |
| PRIMARY_MIC        | string[4]   | MIC of the instrument’s primary listing market, or the reference market for instruments traded on an MTF                                                                                                                               |
| SEC_TYPE           | string[30]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                |
| SHARES_OUTSTANDING | long        | Shares / quantity outstanding                                                                                                                                                                                                          |
| SIP_SYMBOL         | string[16]  | Ticker symbol used by the US Securities Information Processor (CTA / UTP)                                                                                                                                                              |
| TEST_SYMBOL        | string[1]   | Y - Test symbol, N - Not a test symbol                                                                                                                                                                                                 |
| TICK_PILOT_IND     | string[20]  | Specifies any tick size pilot initiatives in which the instrument is participating                                                                                                                                                     |

### US_COMP_REPLAY - TRD

Trades

#### US_COMP_REPLAY - TRD Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AGGRESSOR_SIDE   | string[1]   | Indicates whether a trade resulted from an incoming buy or sell order.                                                                                                                                                                 |
| BOOK_TYPE        | string[1]   | Type of order book or trading mechanism through which a trade was executed.                                                                                                                                                            |
| COND             | string[4]   | Condition code                                                                                                                                                                                                                         |
| CORR             | int         | Type of trade correction / cancellation                                                                                                                                                                                                |
| DELETED_TIME     | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| EXCHANGE         | string[1]   | Exchange from which the update originates                                                                                                                                                                                              |
| EXCH_TIME        | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| FRACTIONAL_SIZE  | double      | Trade size, as a floating-point number                                                                                                                                                                                                 |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PARTICIPANT_TIME | nsectime    | Event timestamp (e.g. trade execution time), as provided by one of the participant exchanges in a consolidated feed                                                                                                                    |
| PRICE            | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SEQ_NUM          | long        | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds                                                                                        |
| SIZE             | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| SOURCE           | string[1]   | Source from which an update originates                                                                                                                                                                                                 |
| STOP_STOCK       | string[1]   | Y - Stopped stock trade, N - Not a stopped stock trade,  - Not applicable                                                                                                                                                              |
| TICKER           | string[16]  | Ticker symbol, as specified by the data source                                                                                                                                                                                         |
| TICK_STATUS      | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| TRADE_ID         | string[20]  | Trade identifier, generally the ID assigned by the matching engine                                                                                                                                                                     |
| TRADE_PERIOD     | string[1]   | Market period during which a trade was executed.                                                                                                                                                                                       |
| TRADE_TYPE       | string[4]   | Type of trade                                                                                                                                                                                                                          |
| TRF              | string[1]   | Trade Reporting Facility used to report a trade (for trades reported to FINRA)                                                                                                                                                         |
| TRF_TIME         | nsectime    | Time at which a trade was processed by the Trade Reporting Facility (for trades reported to FINRA)                                                                                                                                     |
| TTE              | string[1]   | Indicates whether a trade is exempt from the Trade Through Rule (1 - Trade Through Exempt, 0 - No Trade Through Exemption)                                                                                                             |
