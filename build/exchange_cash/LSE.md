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
| Bond               |           2824 | 5.03%        |
| Convertible Bond   |             49 | 0.09%        |
| Corporate Bond     |          40252 | 71.67%       |
| Depository Receipt |            135 | 0.24%        |
| ETC                |            317 | 0.56%        |
| ETF                |           3964 | 7.06%        |
| ETN                |            863 | 1.54%        |
| Equity             |           4676 | 8.33%        |
| Government Bond    |           1018 | 1.81%        |
| Structured Product |           1855 | 3.3%         |
| Test               |             68 | 0.12%        |
| Warrant            |            142 | 0.25%        |
| Total              |          56163 | 100%         |


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


