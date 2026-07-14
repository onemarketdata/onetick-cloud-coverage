# Euronext Milan (Borsa Italiana) - Equities

Borsa Italiana is Italy’s main stock exchange located in Milan, facilitating trading in Italian equities.

* Country: Italy [IT]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Rome
* Start Date: 20120102
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for MILAN`
* `Field Enumerations for MILAN`
* `Trading Hours for MILAN`
* `Recent Holidays for MILAN`



Includes the following coverage:

#### MILAN -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Bond            |              2 | 0.04%        |
| ETF             |           2442 | 53.91%       |
| Equity          |           2011 | 44.39%       |
| Investment Fund |             72 | 1.59%        |
| Preferred Stock |              3 | 0.07%        |
| Total           |           4530 | 100%         |


Consists of 4 Databases

* `MILAN`  - Tick Data
* `MILAN_BARS`  - 1 Minute Bars
* `MILAN_DAILY`  - End of Day Metrics
* `MILAN_LATEST`  - Real Time Latest Values




## MILAN

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## MILAN_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* LAT_1M - 1-minute Latency bars for real time delivered data
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## MILAN_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type





## MILAN_LATEST

Database includes the following tick types:

* SNAP - Latest Trade & Quote / NBBO Prices for all Instruments in the venue
* SNAP_QTE - Latest Quotes for all Instruments in the venue
* SNAP_TRD - Latest Trade Prices for all Traded Instruments in the venue


