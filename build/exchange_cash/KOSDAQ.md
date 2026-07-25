# Korea Exchange - Kosdaq

The Kosdaq market is the Korean stock market for small and medium companies, operated by Korea Exchange.

* Country: Korea [KR]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Seoul
* Start Date: 20080506
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for KOSDAQ`
* `Field Enumerations for KOSDAQ`
* `Trading Hours for KOSDAQ`
* `Recent Holidays for KOSDAQ`



Includes the following coverage:

#### KOSDAQ -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Depository Receipt |              8 | 0.4%         |
| Equity             |           1811 | 91.14%       |
| Index              |             33 | 1.66%        |
| Preferred Stock    |              3 | 0.15%        |
| Right              |             12 | 0.6%         |
| Unknown            |            119 | 5.99%        |
| Warrant            |              1 | 0.05%        |
| Total              |           1987 | 100%         |


Consists of 2 Databases

* `KOSDAQ`  - Tick Data
* `KOSDAQ_BARS`  - 1 Minute Bars




## KOSDAQ

Database includes the following tick types:

* IDX - Index values
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## KOSDAQ_BARS

Database includes the following tick types:

* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars


