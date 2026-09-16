# US Consolidated Equity Replay for Intraday / CEP Schemas

Consolidated data from all US equities exchanges, replayed and available for testing intraday access plus CEP / stream processing




## US_COMP_REPLAY

Database includes the following tick types:

* MKT - Market phase / instrument status information
* NBBO - National Best Bid / Offer quotes
* QTE - Best bid / offer quotes
* TRD - Trades



### US_COMP_REPLAY - MKT

Market phase / instrument status information

#### US_COMP_REPLAY - MKT Table Schema

| Field                  | Data Type   | Description                                                                                                                                                                                                                            |
|------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME            | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP              | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| SHORT_SALE_RESTRICTION | string[1]   | Indicates whether short selling is permitted                                                                                                                                                                                           |
| TRADING_STATUS         | string[1]   | Indicates whether the instrument is subject to a halt or suspension                                                                                                                                                                    |
| REASON_CODE            | string[6]   | Reason for an instrument status update                                                                                                                                                                                                 |
| OMDSEQ                 | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP_REPLAY - NBBO

National Best Bid / Offer quotes

#### US_COMP_REPLAY - NBBO Table Schema

| Field        | Data Type   | Description                                                                                                                                                                                                                            |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME  | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP    | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| BID_PRICE    | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE     | int         | Best bid size                                                                                                                                                                                                                          |
| BID_EXCHANGE | string[2]   | Exchange that set the best bid                                                                                                                                                                                                         |
| ASK_PRICE    | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE     | int         | Best ask size                                                                                                                                                                                                                          |
| ASK_EXCHANGE | string[2]   | Exchange that set the best ask                                                                                                                                                                                                         |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP_REPLAY - QTE

Best bid / offer quotes

#### US_COMP_REPLAY - QTE Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME      | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP        | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME        | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| EXCHANGE         | string[1]   | Exchange from which the update originates                                                                                                                                                                                              |
| SOURCE           | string[1]   | Source from which an update originates                                                                                                                                                                                                 |
| BID_PRICE        | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_SIZE         | long        | Best bid size                                                                                                                                                                                                                          |
| ASK_PRICE        | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| ASK_SIZE         | long        | Best ask size                                                                                                                                                                                                                          |
| QUOTE_COND       | string[1]   | Indicates any special conditions applicable to a quote                                                                                                                                                                                 |
| RPI              | string[1]   | Indicates the presence of Retail Price Improvement interest on bid and/or ask side                                                                                                                                                     |
| RESTRICTION_IND  | string[1]   | Indicates whether short selling is permitted                                                                                                                                                                                           |
| NBBO_LULD_IND    | string[1]   | Indicates whether the NBBO crosses the upper / lower LULD price bands                                                                                                                                                                  |
| PARTICIPANT_TIME | nsectime    | Event timestamp (e.g. trade execution time), as provided by one of the participant exchanges in a consolidated feed                                                                                                                    |
| COND             | string[1]   | Condition code                                                                                                                                                                                                                         |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_COMP_REPLAY - TRD

Trades

#### US_COMP_REPLAY - TRD Table Schema

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
| PARTICIPANT_TIME | nsectime    | Event timestamp (e.g. trade execution time), as provided by one of the participant exchanges in a consolidated feed                                                                                                                    |
| COND             | string[4]   | Condition code                                                                                                                                                                                                                         |
| TICK_STATUS      | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| DELETED_TIME     | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
