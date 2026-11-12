# ICE Europe Financials

Futures, options and spreads with Trades, Quotes, bars, book depth and real-time data from ICE Futures Europe’s financial markets, with history from September 2014. Key contracts are short-term interest rate (STIR) futures and options such as SONIA and Euribor, long gilt futures, and FTSE 100 and MSCI index futures.

* Country: UK United Kindom [GB]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/London
* Start Date: 20140929
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Arrival
* Key Indices:



Details are provided below

* `Table Schemas for ICE_EU_FIN`
* `Field Enumerations for ICE_EU_FIN`
* `Trading Hours for ICE_EU_FIN`
* `Recent Holidays for ICE_EU_FIN`



Includes the following coverage:

#### ICE_EU_FIN -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |           7664 | 3.54%        |
| Futures Spread  |           2293 | 1.06%        |
| Option          |         204644 | 94.41%       |
| Option Spread   |           2162 | 1.0%         |
| Total           |         216763 | 100%         |


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


