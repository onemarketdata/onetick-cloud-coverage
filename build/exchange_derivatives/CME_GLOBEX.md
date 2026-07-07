# CME Globex Futures

CME Globex is the electronic trading platform of the CME Group, offering trading in futures and options across asset classes.

* Country: USA United States [US]
* Mkt Hours: 00:00-24:00
* Time Zone: America/Chicago
* Start Date: 20091109
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for CME_GLOBEX`
* `Field Enumerations for CME_GLOBEX`
* `Trading Hours for CME_GLOBEX`
* `Recent Holidays for CME_GLOBEX`



Includes the following coverage:

#### CME_GLOBEX -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |           5045 | 33.75%       |
| Futures Spread  |           9901 | 66.25%       |
| Total           |          14946 | 100%         |


Consists of 4 Databases

* `CME_GLOBEX`  - Tick Data
* `CME_GLOBEX_BARS`  - 1 Minute Bars
* `CME_GLOBEX_DAILY`  - End of Day Metrics
* `CME_GLOBEX_LATEST`  - Real Time Latest Values




## CME_GLOBEX

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





## CME_GLOBEX_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* LAT_1M - 1-minute Latency bars for real time delivered data
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## CME_GLOBEX_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type





## CME_GLOBEX_LATEST

Database includes the following tick types:

* TRD - Trades
* QTE - Best bid / offer quotes


