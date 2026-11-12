# Euronext Dublin (Irish Stock Exchange)

Trades, quotes, bars and book depth from Euronext Dublin (formerly the Irish Stock Exchange), with real-time data and history from June 2012. It covers the main market and Euronext Growth Dublin, and Dublin is also one of the world’s largest venues for listing debt securities and investment funds. Covered stocks include constituents of the ISEQ 20 and ISEQ All-Share.  A consolidated tape for all European equity markets is provided in the EU_COMP dataset.

* Country: Ireland [IE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Dublin
* Start Date: 20120601
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Arrival
* Key Indices: ISEQ 20 Price Index [EURONEXT_IDX::ISE20], ISEQ All-Share [EURONEXT_IDX::ISEQ]



Details are provided below

* `Table Schemas for DUBLIN`
* `Field Enumerations for DUBLIN`
* `Trading Hours for DUBLIN`
* `Recent Holidays for DUBLIN`



Includes the following coverage:

#### DUBLIN -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Equity          |             25 | 100.0%       |
| Total           |             25 | 100%         |


Consists of 4 Databases

* `DUBLIN`  - Tick Data
* `DUBLIN_BARS`  - 1 Minute Bars
* `DUBLIN_DAILY`  - End of Day Metrics
* `DUBLIN_LATEST`  - Real Time Latest Values




## DUBLIN

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## DUBLIN_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* LAT_1M - 1-minute Latency bars for real time delivered data
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## DUBLIN_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type





## DUBLIN_LATEST

Database includes the following tick types:

* SNAP - Latest Trade & Quote / NBBO Prices for all Instruments in the venue
* SNAP_QTE - Latest Quotes for all Instruments in the venue
* SNAP_TRD - Latest Trade Prices for all Traded Instruments in the venue


