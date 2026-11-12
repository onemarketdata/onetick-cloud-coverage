# Thailand Futures Exchange

Futures, options and spreads with Trades, Quotes and bars from Thailand Futures Exchange (TFEX), part of the Stock Exchange of Thailand group, with history from November 2020. Key contracts include SET50 index futures and options, single-stock futures, gold futures and USD/THB futures.

* Country: Thailand [TH]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Bangkok
* Start Date: 20201102
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices:



Details are provided below

* `Table Schemas for THAILAND_FUT`
* `Field Enumerations for THAILAND_FUT`
* `Trading Hours for THAILAND_FUT`
* `Recent Holidays for THAILAND_FUT`



Includes the following coverage:

#### THAILAND_FUT -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |            571 | 49.01%       |
| Futures Spread  |            398 | 34.16%       |
| Option          |            196 | 16.82%       |
| Total           |           1165 | 100%         |


Consists of 3 Databases

* `THAILAND_FUT`  - Tick Data
* `THAILAND_FUT_BARS`  - 1 Minute Bars
* `THAILAND_FUT_DAILY`  - End of Day Metrics




## THAILAND_FUT

Database includes the following tick types:

* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## THAILAND_FUT_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## THAILAND_FUT_DAILY

Database includes the following tick types:

* STAT - Static data, e.g. ISIN, description, security type


