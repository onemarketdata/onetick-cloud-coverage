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
| Bond               |            426 | 8.03%        |
| Convertible Bond   |             38 | 0.72%        |
| Depository Receipt |             73 | 1.38%        |
| ETF                |            375 | 7.06%        |
| ETP                |             88 | 1.66%        |
| Equity             |           1786 | 33.65%       |
| Government Bond    |             89 | 1.68%        |
| Index              |             43 | 0.81%        |
| Unknown            |             91 | 1.71%        |
| Warrant            |           2299 | 43.31%       |
| Total              |           5308 | 100%         |


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


