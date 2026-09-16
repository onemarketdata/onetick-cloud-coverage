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
| Depository Receipt |             10 | 0.13%        |
| ETF                |           1171 | 15.68%       |
| ETN                |            375 | 5.02%        |
| Equity             |           2701 | 36.16%       |
| Index              |             97 | 1.3%         |
| Mutual Fund        |              1 | 0.01%        |
| Preferred Stock    |            114 | 1.53%        |
| REIT               |             23 | 0.31%        |
| Right              |             27 | 0.36%        |
| Unknown            |            168 | 2.25%        |
| Warrant            |           2783 | 37.26%       |
| Total              |           7470 | 100%         |


Consists of 3 Databases

* `KR_COMP`  - Tick Data
* `KR_COMP_BARS`  - 1 Minute Bars
* `KR_COMP_DAILY`  - End of Day Metrics




## KR_COMP

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IDX - Index values
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


