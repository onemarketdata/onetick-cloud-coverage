# US ETF Constituents Schemas

US ETF Values, Constituents and Constituent Weightings




## OQD_ETF

Database includes the following tick types:

* CASH - Cash Position
* CONSTITUENTS - Constituents
* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* DES - Static data, e.g. ISIN, description, security type
* FX_RATE - Forex Rate
* PCF - Portfolio Composition File Content
* PCF_LONG - Portfolio Composition File Detail



### OQD_ETF - CASH

Cash Position

#### OQD_ETF - CASH Table Schema

| Field          | Data Type   | Description                                                                                                                                                                                                                            |
|----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME    | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP      | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| CURRENCY       | string[12]  | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| ESTIMATED_CASH | double      | Estimated cash per ETF creation unit                                                                                                                                                                                                   |
| TOTAL_CASH     | double      | Total cash per ETF creation unit                                                                                                                                                                                                       |
| DELETED_TIME   | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS    | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### OQD_ETF - CONSTITUENTS

Constituents

#### OQD_ETF - CONSTITUENTS Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME   | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP     | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| TICKER        | string[32]  | Ticker symbol, as specified by the data source                                                                                                                                                                                         |
| NAME          | string[128] | Description of the instrument                                                                                                                                                                                                          |
| BSYM          | string[32]  | Bloomberg Symbol                                                                                                                                                                                                                       |
| FIGI          | string[32]  | Financial Instrument Global Identifier, identifying an individual instrument traded on a specific venue                                                                                                                                |
| FIGI_COMP     | string[32]  | Composite Financial Instrument Global Identifier, identifying an individual instrument traded across venues                                                                                                                            |
| MIC           | string[16]  | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| OPERATING_MIC | string[16]  | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| ULT_ID        | string[32]  | Ultimus Identifier                                                                                                                                                                                                                     |
| OID           | string[16]  | OneMarketData ID                                                                                                                                                                                                                       |
| DELETED_TIME  | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS   | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### OQD_ETF - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### OQD_ETF - DAY Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME     | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP       | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| CURRENCY        | string[12]  | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| FUND_AUM        | double      | Fund Assets Under Management                                                                                                                                                                                                           |
| SHARE_CLASS_AUM | double      | Share Class Assets Under Management                                                                                                                                                                                                    |
| LAST_PRICE      | double      | Price of the last eligible trade                                                                                                                                                                                                       |
| NAV             | double      | Net Asset Value                                                                                                                                                                                                                        |
| OFFICIAL_NAV    | double      | Official Net Asset Value                                                                                                                                                                                                               |
| DELETED_TIME    | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS     | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### OQD_ETF - DES

Static data, e.g. ISIN, description, security type

#### OQD_ETF - DES Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                                                            |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME        | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP          | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| TICKER             | string[12]  | Ticker symbol, as specified by the data source                                                                                                                                                                                         |
| BBG                | string[12]  | Bloomberg Ticker                                                                                                                                                                                                                       |
| DESCRIPTION        | string[64]  | Description of the instrument                                                                                                                                                                                                          |
| DATA_SOURCE        | string[32]  | Source of Data                                                                                                                                                                                                                         |
| REF_DATE           | string[12]  | Reference Date                                                                                                                                                                                                                         |
| NAV_DATE           | string[12]  | Net Asset Value Date                                                                                                                                                                                                                   |
| CURRENCY           | string[12]  | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| SHARES_OUT         | double      | Shares Outstanding                                                                                                                                                                                                                     |
| CREATION_UNIT_SIZE | double      | ETF Creation Unit Size                                                                                                                                                                                                                 |
| CALC_UNIT_SIZE     | double      | ETF Calculation Unit Size                                                                                                                                                                                                              |
| DELETED_TIME       | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS        | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| OMDSEQ             | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### OQD_ETF - FX_RATE

Forex Rate

#### OQD_ETF - FX_RATE Table Schema

| Field        | Data Type   | Description                                                                                                                                                                                                                            |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME  | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP    | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| BASE         | string[12]  | FX Rate Base Currency                                                                                                                                                                                                                  |
| TERM         | string[12]  | FX Rate Term Currency                                                                                                                                                                                                                  |
| RATE         | double      | FX Cross Rate                                                                                                                                                                                                                          |
| DELETED_TIME | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS  | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### OQD_ETF - PCF

Portfolio Composition File Content

#### OQD_ETF - PCF Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME     | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP       | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| TICKER          | string[32]  | Ticker symbol, as specified by the data source                                                                                                                                                                                         |
| NAME            | string[128] | Description of the instrument                                                                                                                                                                                                          |
| BSYM            | string[32]  | Bloomberg Symbol                                                                                                                                                                                                                       |
| FIGI            | string[32]  | Financial Instrument Global Identifier, identifying an individual instrument traded on a specific venue                                                                                                                                |
| FIGI_COMP       | string[32]  | Composite Financial Instrument Global Identifier, identifying an individual instrument traded across venues                                                                                                                            |
| MIC             | string[16]  | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| OPERATING_MIC   | string[16]  | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| ULT_ID          | string[32]  | Ultimus Identifier                                                                                                                                                                                                                     |
| OID             | string[16]  | OneMarketData ID                                                                                                                                                                                                                       |
| CURRENCY        | string[8]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| WEIGHT          | double      | Constituent Weight                                                                                                                                                                                                                     |
| NUMBER_OF_UNITS | double      | ETF Constituent Units                                                                                                                                                                                                                  |
| FX_RATE         | double      | FX Cross Rate                                                                                                                                                                                                                          |
| CALC_PRICE      | double      | Calculated Price                                                                                                                                                                                                                       |
| CALC_CCY        | string[16]  | Calculated Price Currency                                                                                                                                                                                                              |
| CLOSE           | double      | Closing price                                                                                                                                                                                                                          |
| CLOSE_CCY       | string[8]   | Currency in which the instrument’s price is expressed                                                                                                                                                                                  |
| PRICE_DATE      | string[12]  | Price Date                                                                                                                                                                                                                             |
| DELETED_TIME    | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS     | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### OQD_ETF - PCF_LONG

Portfolio Composition File Detail

#### OQD_ETF - PCF_LONG Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME     | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP       | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| ISIN            | string[32]  | ISIN code                                                                                                                                                                                                                              |
| RIC             | string[32]  | Refinitiv Instrument Code                                                                                                                                                                                                              |
| CUSIP           | string[32]  | CUSIP code                                                                                                                                                                                                                             |
| SEDOL           | string[32]  | SEDOL code                                                                                                                                                                                                                             |
| FIGI            | string[32]  | Financial Instrument Global Identifier, identifying an individual instrument traded on a specific venue                                                                                                                                |
| FIGI_COMP       | string[32]  | Composite Financial Instrument Global Identifier, identifying an individual instrument traded across venues                                                                                                                            |
| ULT_ID          | string[32]  | Ultimus Identifier                                                                                                                                                                                                                     |
| OID             | string[16]  | OneMarketData ID                                                                                                                                                                                                                       |
| REF_LISTING_ID  | string[32]  | ETF Reference Listing ID                                                                                                                                                                                                               |
| BSYM            | string[32]  | Bloomberg Symbol                                                                                                                                                                                                                       |
| TICKER          | string[32]  | Ticker symbol, as specified by the data source                                                                                                                                                                                         |
| NAME            | string[128] | Description of the instrument                                                                                                                                                                                                          |
| MIC             | string[16]  | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| OPERATING_MIC   | string[16]  | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| PRIMARY         | string[8]   | Is Primary (True/False)                                                                                                                                                                                                                |
| LOT_SIZE        | double      | All standard order sizes must be an integer multiple of the Lot Size                                                                                                                                                                   |
| LISTING_DATE    | string[16]  | Date when the instrument was listed (YYYYMMDD)                                                                                                                                                                                         |
| CFI_CODE        | string[16]  | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                              |
| COUNTRY_OF_INC  | string[12]  | Country of Incorporation                                                                                                                                                                                                               |
| CURRENCY        | string[8]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| ASSET_TYPE      | string[128] | Instrument Asset Type                                                                                                                                                                                                                  |
| GICS_CODE       | string[16]  | GICS Industry Code                                                                                                                                                                                                                     |
| WEIGHT          | double      | Constituent Weight                                                                                                                                                                                                                     |
| NUMBER_OF_UNITS | double      | ETF Constituent Units                                                                                                                                                                                                                  |
| FX_RATE         | double      | FX Cross Rate                                                                                                                                                                                                                          |
| CALC_PRICE      | double      | Calculated Price                                                                                                                                                                                                                       |
| CALC_CCY        | string[16]  | Calculated Price Currency                                                                                                                                                                                                              |
| CLOSE           | double      | Closing price                                                                                                                                                                                                                          |
| CLOSE_CCY       | string[8]   | Currency in which the instrument’s price is expressed                                                                                                                                                                                  |
| PRICE_DATE      | string[12]  | Price Date                                                                                                                                                                                                                             |
| DELETED_TIME    | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS     | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
