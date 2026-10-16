# Korea Consolidated Equities

Consolidated data from all Korean equities exchanges.

* Country: Korea [KR]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Seoul
* Start Date: 20080506
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for KR_COMP`
* `Field Enumerations for KR_COMP`
* `Trading Hours for KR_COMP`
* `Recent Holidays for KR_COMP`



Includes the following coverage:

#### KR_COMP -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Depository Receipt |             10 | 0.14%        |
| ETF                |           1178 | 16.36%       |
| ETN                |            372 | 5.17%        |
| Equity             |           2707 | 37.6%        |
| Index              |             97 | 1.35%        |
| Mutual Fund        |              1 | 0.01%        |
| Preferred Stock    |            114 | 1.58%        |
| REIT               |             23 | 0.32%        |
| Right              |             28 | 0.39%        |
| Unknown            |            166 | 2.31%        |
| Warrant            |           2503 | 34.77%       |
| Total              |           7199 | 100%         |


Consists of 3 Databases

* `KR_COMP`  - Tick Data
* `KR_COMP_BARS`  - 1 Minute Bars
* `KR_COMP_DAILY`  - End of Day Metrics




## KR_COMP

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IDX - Index values
* NBBO - National Best Bid / Offer quotes
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## KR_COMP_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## KR_COMP_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


