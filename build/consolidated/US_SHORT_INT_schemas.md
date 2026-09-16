# FINRA - US Equities Short Interest / Short Volume Schemas

FINRA US Equity short interest summary every two weeks, plus trade reports, and daily short volume through Trade Reporting Facilities.  FINRA Daily Short Sale Volume is stored in the DAY table.  This is populated daily.  Monthly Short Sale Volume is stored in the TRD and SHORT_INT tables, and is populated monthly, approximately 8 days after the month is complete.  The TRD table reports data per day, while the SHORT_INT table reports data twice per month.




## US_SHORT_INT

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* SHORT_INT - Short Interest Statistics every 2 weeks
* TRD - Trades
* STAT - Static data, e.g. ISIN, description, security type



### US_SHORT_INT - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### US_SHORT_INT - DAY Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                                                            |
|---------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME         | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP           | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| SHORT_VOLUME        | double      | Total short selling volume on the current trading day                                                                                                                                                                                  |
| SHORT_EXEMPT_VOLUME | double      | Total short selling volume exempt from Regulation SHO restrictions                                                                                                                                                                     |
| VOLUME              | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| TRF                 | string[4]   | Trade Reporting Facility used to report a trade (for trades reported to FINRA)                                                                                                                                                         |
| OMDSEQ              | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_SHORT_INT - SHORT_INT

Short Interest Statistics every 2 weeks

#### US_SHORT_INT - SHORT_INT Table Schema

| Field                   | Data Type   | Description                                                                                                                                                                                                                            |
|-------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME             | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP               | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| SHORT_INT               | double      | Total short position held in the security                                                                                                                                                                                              |
| PREV_SHORT_INT          | double      | Previous short interest                                                                                                                                                                                                                |
| AVG_DAILY_VOLUME        | double      | Average daily traded volume                                                                                                                                                                                                            |
| SHORT_INT_DAYS_TO_COVER | double      | Short interest as a multiple of the average daily volume                                                                                                                                                                               |
| SHORT_INT_CHG_PCT       | double      | Short interest percentage change                                                                                                                                                                                                       |
| SHORT_INT_CHG           | double      | Short interest net change                                                                                                                                                                                                              |
| OMDSEQ                  | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_SHORT_INT - TRD

Trades

#### US_SHORT_INT - TRD Table Schema

| Field       | Data Type   | Description                                                                                                                                                                                                                            |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP   | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| TRF         | string[1]   | Trade Reporting Facility used to report a trade (for trades reported to FINRA)                                                                                                                                                         |
| SIZE        | int         | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| PRICE       | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
| SHORT_TYPE  | string[1]   | Type of short sale                                                                                                                                                                                                                     |
| OMDSEQ      | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### US_SHORT_INT - STAT

Static data, e.g. ISIN, description, security type

#### US_SHORT_INT - STAT Table Schema

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
