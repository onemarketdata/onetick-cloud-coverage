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
| Bond               |            435 | 8.48%        |
| Convertible Bond   |             38 | 0.74%        |
| Depository Receipt |             72 | 1.4%         |
| ETF                |            383 | 7.47%        |
| ETP                |             89 | 1.74%        |
| Equity             |           1784 | 34.8%        |
| Government Bond    |             88 | 1.72%        |
| Index              |             44 | 0.86%        |
| Unknown            |             76 | 1.48%        |
| Warrant            |           2118 | 41.31%       |
| Total              |           5127 | 100%         |


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


