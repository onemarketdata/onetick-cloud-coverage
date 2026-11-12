# CBOT Futures

Futures and spreads with Trades, Quotes, bars, book depth and real-time data from the Chicago Board of Trade (CBOT), part of CME Group, with history from November 2009. CBOT lists the benchmark grain and oilseed futures (corn, soybeans, wheat, soybean oil and soybean meal), US Treasury note and bond futures, and E-mini Dow futures.

* Country: USA United States [US]
* Mkt Hours: 00:00-24:00
* Time Zone: America/Chicago
* Start Date: 20091109
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Arrival (from 20091109), Exchange (Matching Engine) from 20190331
* Key Indices:



Details are provided below

* `Table Schemas for CBOT`
* `Field Enumerations for CBOT`
* `Trading Hours for CBOT`
* `Recent Holidays for CBOT`



Includes the following coverage:

#### CBOT -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Future             |           1329 | 23.28%       |
| Futures Spread     |           4356 | 76.3%        |
| Interest Rate Swap |             24 | 0.42%        |
| Total              |           5709 | 100%         |


Consists of 4 Databases

* `CBOT`  - Tick Data
* `CBOT_BARS`  - 1 Minute Bars
* `CBOT_DAILY`  - End of Day Metrics
* `CBOT_LATEST`  - Real Time Latest Values




## CBOT

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* FIXING - Fixing prices
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* RFQ - Data related to a Request for Quote
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## CBOT_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* LAT_1M - 1-minute Latency bars for real time delivered data
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## CBOT_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type





## CBOT_LATEST

Database includes the following tick types:

* SNAP - Latest Trade & Quote / NBBO Prices for all Instruments in the venue
* SNAP_QTE - Latest Quotes for all Instruments in the venue
* SNAP_TRD - Latest Trade Prices for all Traded Instruments in the venue


