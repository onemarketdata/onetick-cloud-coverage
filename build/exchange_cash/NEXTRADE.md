# Nextrade ATS

Trades, Quotes and Book depth from Nextrade (NXT), South Korea’s first licensed alternative trading system, which launched in March 2025 to compete with the Korea Exchange, with history from September 2026. NXT offers pre-market and after-market sessions outside regular Korea Exchange hours and trades KOSPI- and KOSDAQ-listed stocks.  A consolidated tape for both Korean equity markets is provided in the KR_COMP dataset.

* Country: Korea [KR]
* Mkt Hours: 09:00-15:20
* Time Zone: Asia/Seoul
* Start Date: 20260917
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes
* Timestamp Type: Exchange (Matching Engine)
* Key Indices: KOSPI 200 [TDI_IDX::KM]



Details are provided below

* `Table Schemas for NEXTRADE`
* `Field Enumerations for NEXTRADE`
* `Trading Hours for NEXTRADE`
* `Recent Holidays for NEXTRADE`



Includes the following coverage:

#### NEXTRADE -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Depository Receipt |              9 | 0.34%        |
| Equity             |           2604 | 98.26%       |
| Investment Fund    |              1 | 0.04%        |
| Preferred Stock    |             13 | 0.49%        |
| REIT               |             23 | 0.87%        |
| Total              |           2650 | 100%         |


Consists of 2 Databases

* `NEXTRADE`  - Tick Data
* `NEXTRADE_DAILY`  - End of Day Metrics




## NEXTRADE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## NEXTRADE_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


