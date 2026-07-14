# SIX Swiss Exchange

The SIX Swiss Exchange is Switzerland’s principal stock exchange located in Zurich.

* Country: Switzerland [CH]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Zurich
* Start Date: 20120103
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for SWISS`
* `Field Enumerations for SWISS`
* `Trading Hours for SWISS`
* `Recent Holidays for SWISS`



Includes the following coverage:

#### SWISS -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Bond            |           2990 | 41.4%        |
| ETC             |              1 | 0.01%        |
| ETF             |           2261 | 31.31%       |
| Equity          |           1969 | 27.26%       |
| Right           |              1 | 0.01%        |
| Total           |           7222 | 100%         |


Consists of 4 Databases

* `SWISS`  - Tick Data
* `SWISS_BARS`  - 1 Minute Bars
* `SWISS_DAILY`  - End of Day Metrics
* `SWISS_LATEST`  - Real Time Latest Values




## SWISS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## SWISS_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## SWISS_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type





## SWISS_LATEST

Database includes the following tick types:

* SNAP - Latest Trade & Quote / NBBO Prices for all Instruments in the venue
* SNAP_QTE - Latest Quotes for all Instruments in the venue
* SNAP_TRD - Latest Trade Prices for all Traded Instruments in the venue


