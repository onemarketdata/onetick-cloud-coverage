# Korea Exchange - Kosdaq

Trades, quotes and bars from the KOSDAQ market of the Korea Exchange, Korea’s market for growth, technology and small- and mid-cap companies, with history from May 2008. Index data includes the KOSDAQ Composite and KOSDAQ 150.  A consolidated tape for both Korean equity markets is provided in the KR_COMP dataset.

* Country: Korea [KR]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Seoul
* Start Date: 20080506
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: KOSPI 200 [TDI_IDX::KM]



Details are provided below

* `Table Schemas for KOSDAQ`
* `Field Enumerations for KOSDAQ`
* `Trading Hours for KOSDAQ`
* `Recent Holidays for KOSDAQ`



Includes the following coverage:

#### KOSDAQ -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Depository Receipt |              9 | 0.45%        |
| Equity             |           1813 | 90.74%       |
| Index              |             33 | 1.65%        |
| Preferred Stock    |              3 | 0.15%        |
| Right              |              7 | 0.35%        |
| Unknown            |            132 | 6.61%        |
| Warrant            |              1 | 0.05%        |
| Total              |           1998 | 100%         |


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


