# Australian Consolidated Equities

Consolidated data from all Australian equities exchanges.

* Country: Australia [AU]
* Mkt Hours: 08:00-17:00
* Time Zone: Australia/Sydney
* Start Date: 20080506
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for AU_COMP`
* `Field Enumerations for AU_COMP`
* `Trading Hours for AU_COMP`
* `Recent Holidays for AU_COMP`



Includes the following coverage:

#### AU_COMP -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Bond               |              7 | 0.25%        |
| Convertible Bond   |             38 | 1.37%        |
| Depository Receipt |             71 | 2.55%        |
| ETF                |            399 | 14.35%       |
| ETP                |             88 | 3.17%        |
| Equity             |           1786 | 64.24%       |
| Unknown            |             94 | 3.38%        |
| Warrant            |            297 | 10.68%       |
| Total              |           2780 | 100%         |


Consists of 3 Databases

* `AU_COMP`  - Tick Data
* `AU_COMP_BARS`  - 1 Minute Bars
* `AU_COMP_DAILY`  - End of Day Metrics




## AU_COMP

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* NBBO - National Best Bid / Offer quotes
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## AU_COMP_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## AU_COMP_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


