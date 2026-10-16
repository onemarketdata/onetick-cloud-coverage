# Shanghai Stock Exchange - Equities

The Shanghai Stock Exchange (SSE) offers trading in A-shares, B-shares, bonds, and other securities issued by Chinese companies.

* Country: China [CN]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Hong_Kong
* Start Date: 20150126
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for SHANGHAI`
* `Field Enumerations for SHANGHAI`
* `Trading Hours for SHANGHAI`
* `Recent Holidays for SHANGHAI`



Includes the following coverage:

#### SHANGHAI -  Coverage

| Security Type    |   # of Symbols | % of Total   |
|------------------|----------------|--------------|
| Bond             |          15666 | 60.35%       |
| Convertible Bond |           1050 | 4.05%        |
| Corporate Bond   |           1591 | 6.13%        |
| ETF              |            996 | 3.84%        |
| Equity           |           2429 | 9.36%        |
| Government Bond  |           4138 | 15.94%       |
| REIT             |             61 | 0.24%        |
| Repo             |              9 | 0.03%        |
| Unknown          |             17 | 0.07%        |
| Total            |          25957 | 100%         |


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


