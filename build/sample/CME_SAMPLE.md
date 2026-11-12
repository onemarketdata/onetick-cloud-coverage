# CME Group (PCAP) Sample

A sample of the CME Group database covering a subset of symbols from CME Group’s four exchanges (CME, CBOT, NYMEX and COMEX), traded on the CME Globex electronic platform, between January 2, 2024 and March 31, 2024. Captured from PCAP, it includes trades, quotes, book depth and bars for futures, options and spreads on CL (WTI Crude Oil), ES (E-mini S&P 500), GC (Gold), NG (Henry Hub Natural Gas), NQ (E-mini Nasdaq-100) and ZC (Corn).

* Country: USA United States [US]
* Mkt Hours: 00:00-24:00
* Time Zone: America/Chicago
* Start Date: 20240102
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Exchange (Matching Engine)
* Key Indices:



Details are provided below

* `Table Schemas for CME_SAMPLE`
* `Field Enumerations for CME_SAMPLE`
* `Trading Hours for CME_SAMPLE`
* `Recent Holidays for CME_SAMPLE`



Includes the following coverage:

#### CME_SAMPLE -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |            346 | 100.0%       |
| Total           |            346 | 100%         |


Consists of 3 Databases

* `CME_SAMPLE`  - Tick Data
* `CME_SAMPLE_BARS`  - 1 Minute Bars
* `CME_SAMPLE_DAILY`  - End of Day Metrics




## CME_SAMPLE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* FIXING - Fixing prices
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* RFQ - Data related to a Request for Quote
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## CME_SAMPLE_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## CME_SAMPLE_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


