# Korea Consolidated Equities

Consolidated trades, NBBO, exchange quotes and bars for Korean equities from the Korea Exchange (KRX), covering both its KOSPI main board and KOSDAQ growth market, and NextTrade, with history from May 2008. Index data is also included, covering benchmarks such as the KOSPI, KOSPI 200 and KOSDAQ Composite, so stocks and their benchmarks can be analysed in one database.

* Country: Korea [KR]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Seoul
* Start Date: 20080506
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: KOSPI 200 [TDI_IDX], KM



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
| ETF                |           1185 | 15.78%       |
| ETN                |            377 | 5.02%        |
| Equity             |           2704 | 36.01%       |
| Index              |             97 | 1.29%        |
| Mutual Fund        |              1 | 0.01%        |
| Preferred Stock    |            114 | 1.52%        |
| REIT               |             23 | 0.31%        |
| Right              |             27 | 0.36%        |
| Unknown            |            169 | 2.25%        |
| Warrant            |           2801 | 37.31%       |
| Total              |           7508 | 100%         |


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


