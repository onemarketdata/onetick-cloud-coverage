# Lima Stock Exchange

The Lima Stock Exchange is the official stock exchange of Peru where securities like stocks, bonds and derivatives are traded.

* Country: Peru [PE]
* Mkt Hours: 08:00-17:00
* Time Zone: America/Lima
* Start Date: 20160627
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for LIMA`
* `Field Enumerations for LIMA`
* `Trading Hours for LIMA`
* `Recent Holidays for LIMA`



Includes the following coverage:

#### LIMA -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Bond            |            466 | 34.14%       |
| ETF             |            341 | 24.98%       |
| Equity          |            452 | 33.11%       |
| Index           |              3 | 0.22%        |
| Unknown         |            103 | 7.55%        |
| Total           |           1365 | 100%         |


Consists of 2 Databases

* `LIMA`  - Tick Data
* `LIMA_BARS`  - 1 Minute Bars




## LIMA

Database includes the following tick types:

* IDX - Index values
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## LIMA_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars


