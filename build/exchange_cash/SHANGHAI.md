# Shanghai Stock Exchange - Equities

Trades, quotes, bars and book depth from the Shanghai Stock Exchange (SSE), with history from January 2015, covering the main board and STAR Market, A-shares and B-shares, and Shanghai-Hong Kong Stock Connect. Covered stocks include constituents of the SSE Composite, SSE 50 and CSI 300; index values are in SHANGHAI_IDX.

* Country: China [CN]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Hong_Kong
* Start Date: 20150126
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Arrival (from 20150126), Exchange (Matching Engine) from 20250110
* Key Indices: Shanghai SE Composite Index [TDI_IDX::SH]



Details are provided below

* `Table Schemas for SHANGHAI`
* `Field Enumerations for SHANGHAI`
* `Trading Hours for SHANGHAI`
* `Recent Holidays for SHANGHAI`



Includes the following coverage:

#### SHANGHAI -  Coverage

| Security Type    |   # of Symbols | % of Total   |
|------------------|----------------|--------------|
| Bond             |          15795 | 60.61%       |
| Convertible Bond |           1049 | 4.03%        |
| Corporate Bond   |           1571 | 6.03%        |
| ETF              |           1000 | 3.84%        |
| Equity           |           2427 | 9.31%        |
| Government Bond  |           4132 | 15.86%       |
| REIT             |             61 | 0.23%        |
| Repo             |              9 | 0.03%        |
| Unknown          |             17 | 0.07%        |
| Total            |          26061 | 100%         |


Consists of 3 Databases

* `SHANGHAI`  - Tick Data
* `SHANGHAI_BARS`  - 1 Minute Bars
* `SHANGHAI_DAILY`  - End of Day Metrics




## SHANGHAI

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## SHANGHAI_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## SHANGHAI_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


