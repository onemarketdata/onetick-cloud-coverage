# CME Group Futures & Options

Futures, options and spreads with Trades, Qutoes, bars and market-by-order (MBO) book depth from CME Group’s exchanges, CME, CBOT, NYMEX and COMEX, all traded on the CME Globex platform, with history from March 2019. Products span agriculture, energy, metals, interest rates, equity indices, FX and cryptocurrencies. It also covers Minneapolis hard red spring wheat contracts from MGEX (now MIAX Futures), which traded on CME Globex until 2025. This database includes MBO book depth and additional fields that are not available in the other CME databases.

* Country: USA United States [US]
* Mkt Hours: 00:00-24:00
* Time Zone: America/Chicago
* Start Date: 20190331
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Exchange (Matching Engine)
* Key Indices:



Details are provided below

* `Table Schemas for CME`
* `Field Enumerations for CME`
* `Trading Hours for CME`
* `Recent Holidays for CME`



Includes the following coverage:

#### CME -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |             38 | 0.1%         |
| Futures Spread  |             43 | 0.11%        |
| Option          |          10904 | 28.48%       |
| Option Spread   |          27307 | 71.31%       |
| Total           |          38292 | 100%         |


Consists of 3 Databases

* `CME`  - Tick Data
* `CME_BARS`  - 1 Minute Bars
* `CME_DAILY`  - End of Day Metrics




## CME

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* FIXING - Fixing prices
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* RFQ - Data related to a Request for Quote
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## CME_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## CME_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


