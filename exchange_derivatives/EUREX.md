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
| Future          |          23600 | 3.27%        |
| Futures Spread  |           5635 | 0.78%        |
| Option          |         685483 | 95.07%       |
| Option Spread   |           6302 | 0.87%        |
| Unknown         |             24 | 0.0%         |
| Total           |         721044 | 100%         |


Consists of 4 Databases

* `EUREX`  - Tick Data
* `EUREX_BARS`  - 1 Minute Bars
* `EUREX_DAILY`  - End of Day Metrics
* `EUREX_LATEST`  - Real Time Latest Values




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




