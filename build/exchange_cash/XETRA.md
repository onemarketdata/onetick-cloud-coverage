# Xetra Exchange

Xetra is an electronic trading system operated by Deutsche Boerse for trading equities and other securities.

* Country: Germany [DE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Berlin
* Start Date: 20120102
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for XETRA`
* `Field Enumerations for XETRA`
* `Trading Hours for XETRA`
* `Recent Holidays for XETRA`



Includes the following coverage:

#### XETRA -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| ETC             |            205 | 4.04%        |
| ETF             |           3050 | 60.12%       |
| ETN             |            382 | 7.53%        |
| Equity          |           1434 | 28.27%       |
| Right           |              1 | 0.02%        |
| Unknown         |              1 | 0.02%        |
| Total           |           5073 | 100%         |


Consists of 4 Databases

* `XETRA`  - Tick Data
* `XETRA_BARS`  - 1 Minute Bars
* `XETRA_DAILY`  - End of Day Metrics
* `XETRA_LATEST`  - Real Time Latest Values




## XETRA

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL - Market depth data, aggregated by price point (MBP)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## XETRA_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## XETRA_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type





## XETRA_LATEST

Database includes the following tick types:

* SNAP - Latest Trade & Quote / NBBO Prices for all Instruments in the venue
* SNAP_QTE - Latest Quotes for all Instruments in the venue
* SNAP_TRD - Latest Trade Prices for all Traded Instruments in the venue


