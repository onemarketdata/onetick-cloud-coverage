# London Stock Exchange - UK Market

The London Stock Exchange’s UK market facilitates trading in UK-based companies listed on its Main Market and AIM.

* Country: UK United Kindom [GB]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/London
* Start Date: 20120103
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for LSE`
* `Field Enumerations for LSE`
* `Trading Hours for LSE`
* `Recent Holidays for LSE`



Includes the following coverage:

#### LSE -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Bond               |           2760 | 5.16%        |
| Convertible Bond   |             47 | 0.09%        |
| Corporate Bond     |          37774 | 70.62%       |
| Depository Receipt |            136 | 0.25%        |
| ETC                |            319 | 0.6%         |
| ETF                |           3874 | 7.24%        |
| ETN                |            851 | 1.59%        |
| Equity             |           4706 | 8.8%         |
| Government Bond    |           1004 | 1.88%        |
| Structured Product |           1814 | 3.39%        |
| Test               |             68 | 0.13%        |
| Warrant            |            135 | 0.25%        |
| Total              |          53488 | 100%         |


Consists of 4 Databases

* `LSE`  - Tick Data
* `LSE_BARS`  - 1 Minute Bars
* `LSE_DAILY`  - End of Day Metrics
* `LSE_LATEST`  - Real Time Latest Values




## LSE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## LSE_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* LAT_1M - 1-minute Latency bars for real time delivered data
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars



