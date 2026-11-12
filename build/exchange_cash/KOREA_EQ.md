# Korea Exchange - Equities (KOSPI)

Trades, quotes and bars from the Korea Exchange’s KOSPI market, where Korea’s large-cap stocks such as Samsung Electronics and SK Hynix trade, with history from May 2008. Index data is included, covering the KOSPI and KOSPI 200. A consolidated tape for both Korean equity markets is provided in the KR_COMP dataset.

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

* `Table Schemas for KOREA_EQ`
* `Field Enumerations for KOREA_EQ`
* `Trading Hours for KOREA_EQ`
* `Recent Holidays for KOREA_EQ`



Includes the following coverage:

#### KOREA_EQ -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Depository Receipt |              1 | 0.09%        |
| Equity             |            891 | 77.41%       |
| Index              |             64 | 5.56%        |
| Mutual Fund        |              1 | 0.09%        |
| Preferred Stock    |            111 | 9.64%        |
| REIT               |             23 | 2.0%         |
| Right              |             20 | 1.74%        |
| Unknown            |             37 | 3.21%        |
| Warrant            |              3 | 0.26%        |
| Total              |           1151 | 100%         |


Consists of 2 Databases

* `KOREA_EQ`  - Tick Data
* `KOREA_EQ_BARS`  - 1 Minute Bars




## KOREA_EQ

Database includes the following tick types:

* IDX - Index values
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## KOREA_EQ_BARS

Database includes the following tick types:

* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars


