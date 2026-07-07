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
| CURRENCY       | string[12]  | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| DELETED_TIME   | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| ESTIMATED_CASH | double      | Estimated cash per ETF creation unit                                                                                                                                                                                                   |
| OMDSEQ         | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| TICK_STATUS    | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| TOTAL_CASH     | double      | Total cash per ETF creation unit                                                                                                                                                                                                       |

### OQD_ETF - CONSTITUENTS

Constituents

#### OQD_ETF - CONSTITUENTS Table Schema

| Field         | Data Type   | Description                                                                                                                                                                                                                            |
|---------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BSYM          | string[32]  | Bloomberg Symbol                                                                                                                                                                                                                       |
| DELETED_TIME  | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| FIGI          | string[32]  | Financial Instrument Global Identifier, identifying an individual instrument traded on a specific venue                                                                                                                                |
| FIGI_COMP     | string[32]  | Composite Financial Instrument Global Identifier, identifying an individual instrument traded across venues                                                                                                                            |
| MIC           | string[16]  | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| NAME          | string[128] | Description of the instrument                                                                                                                                                                                                          |
| OID           | string[16]  | OneMarketData ID                                                                                                                                                                                                                       |
| OMDSEQ        | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPERATING_MIC | string[16]  | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| TICK_STATUS   | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| TICKER        | string[32]  | Ticker symbol, as specified by the data source                                                                                                                                                                                         |
| ULT_ID        | string[32]  | Ultimus Identifier                                                                                                                                                                                                                     |

### OQD_ETF - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### OQD_ETF - DAY Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CURRENCY        | string[12]  | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| DELETED_TIME    | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| FUND_AUM        | double      | Fund Assets Under Management                                                                                                                                                                                                           |
| LAST_PRICE      | double      | Price of the last eligible trade                                                                                                                                                                                                       |
| NAV             | double      | Net Asset Value                                                                                                                                                                                                                        |
| OFFICIAL_NAV    | double      | Official Net Asset Value                                                                                                                                                                                                               |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| SHARE_CLASS_AUM | double      | Share Class Assets Under Management                                                                                                                                                                                                    |
| TICK_STATUS     | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |

### OQD_ETF - DES

Static data, e.g. ISIN, description, security type

#### OQD_ETF - DES Table Schema

| Field              | Data Type   | Description                                                                                                                                                                                                                            |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BBG                | string[12]  | Bloomberg Ticker                                                                                                                                                                                                                       |
| CALC_UNIT_SIZE     | double      | ETF Calculation Unit Size                                                                                                                                                                                                              |
| CREATION_UNIT_SIZE | double      | ETF Creation Unit Size                                                                                                                                                                                                                 |
| CURRENCY           | string[12]  | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| DATA_SOURCE        | string[32]  | Source of Data                                                                                                                                                                                                                         |
| DELETED_TIME       | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| DESCRIPTION        | string[64]  | Description of the instrument                                                                                                                                                                                                          |
| NAV_DATE           | string[12]  | Net Asset Value Date                                                                                                                                                                                                                   |
| OMDSEQ             | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| REF_DATE           | string[12]  | Reference Date                                                                                                                                                                                                                         |
| SHARES_OUT         | double      | Shares Outstanding                                                                                                                                                                                                                     |
| TICK_STATUS        | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| TICKER             | string[12]  | Ticker symbol, as specified by the data source                                                                                                                                                                                         |

### OQD_ETF - FX_RATE

Forex Rate

#### OQD_ETF - FX_RATE Table Schema

| Field        | Data Type   | Description                                                                                                                                                                                                                            |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BASE         | string[12]  | FX Rate Base Currency                                                                                                                                                                                                                  |
| DELETED_TIME | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| RATE         | double      | FX Cross Rate                                                                                                                                                                                                                          |
| TERM         | string[12]  | FX Rate Term Currency                                                                                                                                                                                                                  |
| TICK_STATUS  | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |

### OQD_ETF - PCF

Portfolio Composition File Content

#### OQD_ETF - PCF Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BSYM            | string[32]  | Bloomberg Symbol                                                                                                                                                                                                                       |
| CALC_CCY        | string[16]  | Calculated Price Currency                                                                                                                                                                                                              |
| CALC_PRICE      | double      | Calculated Price                                                                                                                                                                                                                       |
| CLOSE           | double      | Closing price                                                                                                                                                                                                                          |
| CLOSE_CCY       | string[8]   | Currency in which the instrument’s price is expressed                                                                                                                                                                                  |
| CURRENCY        | string[8]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| DELETED_TIME    | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| FIGI            | string[32]  | Financial Instrument Global Identifier, identifying an individual instrument traded on a specific venue                                                                                                                                |
| FIGI_COMP       | string[32]  | Composite Financial Instrument Global Identifier, identifying an individual instrument traded across venues                                                                                                                            |
| FX_RATE         | double      | FX Cross Rate                                                                                                                                                                                                                          |
| MIC             | string[16]  | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| NAME            | string[128] | Description of the instrument                                                                                                                                                                                                          |
| NUMBER_OF_UNITS | double      | ETF Constituent Units                                                                                                                                                                                                                  |
| OID             | string[16]  | OneMarketData ID                                                                                                                                                                                                                       |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPERATING_MIC   | string[16]  | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                     |
| PRICE_DATE      | string[12]  | Price Date                                                                                                                                                                                                                             |
| TICK_STATUS     | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| TICKER          | string[32]  | Ticker symbol, as specified by the data source                                                                                                                                                                                         |
| ULT_ID          | string[32]  | Ultimus Identifier                                                                                                                                                                                                                     |
| WEIGHT          | double      | Constituent Weight                                                                                                                                                                                                                     |

### OQD_ETF - PCF_LONG

Portfolio Composition File Detail

#### OQD_ETF - PCF_LONG Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASSET_TYPE      | string[128] | Instrument Asset Type                                                                                                                                                                                                                  |
| BSYM            | string[32]  | Bloomberg Symbol                                                                                                                                                                                                                       |
| CALC_CCY        | string[16]  | Calculated Price Currency                                                                                                                                                                                                              |
| CALC_PRICE      | double      | Calculated Price                                                                                                                                                                                                                       |
| CFI_CODE        | string[16]  | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                              |
| CLOSE           | double      | Closing price                                                                                                                                                                                                                          |
| CLOSE_CCY       | string[8]   | Currency in which the instrument’s price is expressed                                                                                                                                                                                  |
| COUNTRY_OF_INC  | string[12]  | Country of Incorporation                                                                                                                                                                                                               |
| CURRENCY        | string[8]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| CUSIP           | string[32]  | CUSIP code                                                                                                                                                                                                                             |
| DELETED_TIME    | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| FIGI            | string[32]  | Financial Instrument Global Identifier, identifying an individual instrument traded on a specific venue                                                                                                                                |
