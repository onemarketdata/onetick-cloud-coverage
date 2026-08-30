# Australian Stock Exchange

The Australian Stock Exchange (ASX) offers trading in equities, bonds, ETFs, derivatives, and other securities issued by Australian companies.

* Country: Australia [AU]
* Mkt Hours: 08:00-17:00
* Time Zone: Australia/Sydney
* Start Date: 20080506
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for ASX`
* `Field Enumerations for ASX`
* `Trading Hours for ASX`
* `Recent Holidays for ASX`



Includes the following coverage:

#### ASX -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Bond               |            419 | 7.87%        |
| Convertible Bond   |             38 | 0.71%        |
| Depository Receipt |             73 | 1.37%        |
| ETF                |            375 | 7.04%        |
| ETP                |             88 | 1.65%        |
| Equity             |           1791 | 33.63%       |
| Government Bond    |             89 | 1.67%        |
| Index              |             43 | 0.81%        |
| Unknown            |             75 | 1.41%        |
| Warrant            |           2334 | 43.83%       |
| Total              |           5325 | 100%         |


Consists of 2 Databases

* `ASX`  - Tick Data
* `ASX_BARS`  - 1 Minute Bars




## ASX

Database includes the following tick types:

* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## ASX_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars


