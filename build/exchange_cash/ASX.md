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
| Bond               |            428 | 8.34%        |
| Convertible Bond   |             38 | 0.74%        |
| Depository Receipt |             71 | 1.38%        |
| ETF                |            380 | 7.41%        |
| ETP                |             88 | 1.72%        |
| Equity             |           1779 | 34.69%       |
| Government Bond    |             89 | 1.74%        |
| Index              |             44 | 0.86%        |
| Unknown            |             72 | 1.4%         |
| Warrant            |           2140 | 41.72%       |
| Total              |           5129 | 100%         |


Consists of 2 Databases

* `ASX`  - Tick Data
* `ASX_BARS`  - 1 Minute Bars




## ASX

Database includes the following tick types:

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


