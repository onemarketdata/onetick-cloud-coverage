# Eurex Exchange

Futures, options and spreads with Trades, Quotes, bars, book depth and real-time data from Eurex, Deutsche Borse Group’s Frankfurt-based derivatives exchange and Europe’s largest, with futures from November 2009 and options from August 2019. Key contracts include Euro-Bund, Euro-Bobl, Euro-Schatz and Euro-Buxl futures on German government bonds and EURO STOXX 50 and DAX index futures and options. Eurex also lists derivatives on French, Italian, Spanish and Swiss government bonds and on other European indices and single stocks.

* Country: Germany [DE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Berlin
* Start Date: 20091109 - Futures, 20190809 - Options
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Arrival
* Key Indices:



Details are provided below

* `Table Schemas for EUREX`
* `Field Enumerations for EUREX`
* `Trading Hours for EUREX`
* `Recent Holidays for EUREX`



Includes the following coverage:

#### EUREX -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |          23035 | 3.19%        |
| Futures Spread  |           5902 | 0.82%        |
| Option          |         686983 | 94.99%       |
| Option Spread   |           6954 | 0.96%        |
| Unknown         |            323 | 0.04%        |
| Total           |         723197 | 100%         |


Consists of 5 Databases

* `EUREX`  - Tick Data
* `EUREX_BARS`  - 1 Minute Bars
* `EUREX_DAILY`  - End of Day Metrics
* `EUREX_L2`  - Tick Data
* `EUREX_LATEST`  - Real Time Latest Values




## EUREX

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
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





## EUREX_L2

Database includes the following tick types:

* PRL - Market depth data, aggregated by price point (MBP)





## EUREX_LATEST

Database includes the following tick types:

* SNAP - Latest Trade & Quote / NBBO Prices for all Instruments in the venue
* SNAP_QTE - Latest Quotes for all Instruments in the venue
* SNAP_TRD - Latest Trade Prices for all Traded Instruments in the venue


