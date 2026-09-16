# ICE Europe Financials

ICE Europe Financials facilitates trading in interest rate, equity index, and FX futures and options contracts across European financial markets.

* Country: UK United Kindom [GB]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/London
* Start Date: 20180730
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for ICE_EU_FIN`
* `Field Enumerations for ICE_EU_FIN`
* `Trading Hours for ICE_EU_FIN`
* `Recent Holidays for ICE_EU_FIN`



Includes the following coverage:

#### ICE_EU_FIN -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |           7603 | 3.43%        |
| Futures Spread  |           1903 | 0.86%        |
| Option          |         209624 | 94.64%       |
| Option Spread   |           2373 | 1.07%        |
| Total           |         221503 | 100%         |


Consists of 4 Databases

* `ICE_EU_FIN`  - Tick Data
* `ICE_EU_FIN_BARS`  - 1 Minute Bars
* `ICE_EU_FIN_DAILY`  - End of Day Metrics
* `ICE_EU_FIN_LATEST`  - Real Time Latest Values




## ICE_EU_FIN

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## ICE_EU_FIN_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* LAT_1M - 1-minute Latency bars for real time delivered data
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars





## ICE_EU_FIN_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type





## ICE_EU_FIN_LATEST

Database includes the following tick types:

* SNAP - Latest Trade & Quote / NBBO Prices for all Instruments in the venue
* SNAP_QTE - Latest Quotes for all Instruments in the venue
* SNAP_TRD - Latest Trade Prices for all Traded Instruments in the venue


