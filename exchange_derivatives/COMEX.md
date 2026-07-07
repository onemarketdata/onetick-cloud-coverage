# COMEX Futures

COMEX is a division of the CME Group, offering trading in metal futures and options.

* Country: USA United States [US]
* Mkt Hours: 00:00-24:00
* Time Zone: America/Chicago
* Start Date: 20091109
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for COMEX`
* `Field Enumerations for COMEX`
* `Trading Hours for COMEX`
* `Recent Holidays for COMEX`



Includes the following coverage:

#### COMEX -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |           1372 | 10.3%        |
| Futures Spread  |          11944 | 89.7%        |
| Total           |          13316 | 100%         |


Consists of 4 Databases

* `COMEX`  - Tick Data
* `COMEX_BARS`  - 1 Minute Bars
* `COMEX_DAILY`  - End of Day Metrics
* `COMEX_LATEST`  - Real Time Latest Values




## COMEX

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* RFQ - Data related to a Request for Quote
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## COMEX_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* LAT_1M - 1-minute Latency bars for real time delivered data
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## COMEX_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type





## COMEX_LATEST

Database includes the following tick types:

* TRD - Trades
* QTE - Best bid / offer quotes


