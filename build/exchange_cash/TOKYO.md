# Tokyo Stock Exchange (+ Fukuoka / Sapporo)

Trades, quotes and bars from the Tokyo Stock Exchange (TSE), Japan’s main stock exchange and part of Japan Exchange Group, with history from October 2008, plus the separate regional Fukuoka and Sapporo exchanges. Since April 2022 TSE equities have been listed on the Prime, Standard and Growth markets, alongside the TOKYO PRO Market for professional investors. Main benchmarks are TOPIX, calculated by TSE, and the Nikkei 225.

* Country: Japan [JP]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Tokyo
* Start Date: 20081001
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: Nikkei 225 Index [TDI_IDX::NE], TOPIX Index [TDI_IDX::TP]



Details are provided below

* `Table Schemas for TOKYO`
* `Field Enumerations for TOKYO`
* `Trading Hours for TOKYO`
* `Recent Holidays for TOKYO`



Includes the following coverage:

#### TOKYO -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| ETF             |            490 | 10.5%        |
| Equity          |           4097 | 87.82%       |
| Preferred Stock |              9 | 0.19%        |
| REIT            |             64 | 1.37%        |
| Test            |              5 | 0.11%        |
| Total           |           4665 | 100%         |


Consists of 3 Databases

* `TOKYO`  - Tick Data
* `TOKYO_BARS`  - 1 Minute Bars
* `TOKYO_DAILY`  - End of Day Metrics




## TOKYO

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## TOKYO_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## TOKYO_DAILY

Database includes the following tick types:

* STAT - Static data, e.g. ISIN, description, security type


