# Euronext Oslo - Equities

The Oslo Stock Exchange (Oslo Bors) is the only regulated market for trading equities, equity certificates and bonds in Norway.

* Country: Norway [NO]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Oslo
* Start Date: 20120102
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for OSLO`
* `Field Enumerations for OSLO`
* `Trading Hours for OSLO`
* `Recent Holidays for OSLO`



Includes the following coverage:

#### OSLO -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Equity          |            300 | 100.0%       |
| Total           |            300 | 100%         |


Consists of 4 Databases

* `OSLO`  - Tick Data
* `OSLO_BARS`  - 1 Minute Bars
* `OSLO_DAILY`  - End of Day Metrics
* `OSLO_LATEST`  - Real Time Latest Values




## OSLO

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## OSLO_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## OSLO_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type





## OSLO_LATEST

Database includes the following tick types:

* SNAP - Latest Trade & Quote / NBBO Prices for all Instruments in the venue
* SNAP_QTE - Latest Quotes for all Instruments in the venue
* SNAP_TRD - Latest Trade Prices for all Traded Instruments in the venue


