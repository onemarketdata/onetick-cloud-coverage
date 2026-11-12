# Xetra Exchange

Trades, quotes, bars and book depth, with real-time data, from Xetra, Deutsche B?rse’s electronic trading platform and Germany’s main venue for equities and ETFs, with history from January 2012. Xetra’s closing auction sets the reference prices for German stocks. Covered stocks include constituents of the DAX, MDAX, SDAX and TecDAX.  A consolidated tape for all European equity markets is provided in the EU_COMP dataset.

* Country: Germany [DE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Berlin
* Start Date: 20120102
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Arrival
* Key Indices: DAX Index [TDI_IDX::DA]



Details are provided below

* `Table Schemas for XETRA`
* `Field Enumerations for XETRA`
* `Trading Hours for XETRA`
* `Recent Holidays for XETRA`



Includes the following coverage:

#### XETRA -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| ETC             |            206 | 3.73%        |
| ETF             |           3172 | 57.43%       |
| ETN             |            388 | 7.03%        |
| Equity          |           1757 | 31.81%       |
| Total           |           5523 | 100%         |


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
* LAT_1M - 1-minute Latency bars for real time delivered data
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


