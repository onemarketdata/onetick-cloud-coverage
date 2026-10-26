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
| Bond               |           2861 | 4.98%        |
| Convertible Bond   |             49 | 0.09%        |
| Corporate Bond     |          41454 | 72.11%       |
| Depository Receipt |            134 | 0.23%        |
| ETC                |            320 | 0.56%        |
| ETF                |           4053 | 7.05%        |
| ETN                |            870 | 1.51%        |
| Equity             |           4649 | 8.09%        |
| Government Bond    |           1026 | 1.78%        |
| Structured Product |           1874 | 3.26%        |
| Test               |             53 | 0.09%        |
| Warrant            |            141 | 0.25%        |
| Total              |          57484 | 100%         |


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





## LSE_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type





## LSE_LATEST

Database includes the following tick types:

* SNAP - Latest Trade & Quote / NBBO Prices for all Instruments in the venue
* SNAP_QTE - Latest Quotes for all Instruments in the venue
* SNAP_TRD - Latest Trade Prices for all Traded Instruments in the venue


