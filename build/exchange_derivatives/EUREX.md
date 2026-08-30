# Eurex Exchange

Eurex Exchange is a German derivatives exchange which primarily offers trading in European based derivatives. The products traded on this exchange vary from German and Swiss debt instruments to European stocks and various stock indexes

* Country: Germany [DE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Berlin
* Start Date: 20091109 - Futures, 20190809 - Options
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for EUREX`
* `Field Enumerations for EUREX`
* `Trading Hours for EUREX`
* `Recent Holidays for EUREX`



Includes the following coverage:

#### EUREX -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |          23399 | 3.35%        |
| Futures Spread  |           5737 | 0.82%        |
| Option          |         663542 | 95.01%       |
| Option Spread   |           5571 | 0.8%         |
| Unknown         |            112 | 0.02%        |
| Total           |         698361 | 100%         |


Consists of 5 Databases

* `EUREX`  - Tick Data
* `EUREX_BARS`  - 1 Minute Bars
* `EUREX_DAILY`  - End of Day Metrics
* `EUREX_LATEST`  - Real Time Latest Values
* `EUREX_L2`  - Tick Data




## EUREX

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* SEC_GROUP -  Group Reference
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## EUREX_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* LAT_1M - 1-minute Latency bars for real time delivered data
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## EUREX_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type
* TRD_1D - Daily trade bars





## EUREX_LATEST

Database includes the following tick types:

* SNAP - Latest Trade & Quote / NBBO Prices for all Instruments in the venue
* SNAP_QTE - Latest Quotes for all Instruments in the venue
* SNAP_TRD - Latest Trade Prices for all Traded Instruments in the venue





## EUREX_L2

Database includes the following tick types:

* PRL - Market depth data, aggregated by price point (MBP)


