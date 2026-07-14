# CME Group Futures & Options

The CME Group operates derivatives exchanges ( CBOT COMEX NYMEX CME Globex ) offering trading in futures and options across asset classes like agriculture, energy, metals, interest rates, equities, and cryptocurrencies. MGEX is for trading agricultural futures and options.  This CME Database includes Book Depth MBO data and additional fields that are not supported in the other CME Databases.

* Country: USA United States [US]
* Mkt Hours: 00:00-24:00
* Time Zone: America/Chicago
* Start Date: 20190331
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for CME`
* `Field Enumerations for CME`
* `Trading Hours for CME`
* `Recent Holidays for CME`



Includes the following coverage:

#### CME -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Future             |          51146 | 5.48%        |
| Futures Spread     |          93886 | 10.06%       |
| Interest Rate Swap |             24 | 0.0%         |
| Option             |         691974 | 74.16%       |
| Option Spread      |          96113 | 10.3%        |
| Total              |         933143 | 100%         |


Consists of 3 Databases

* `CME`  - Tick Data
* `CME_BARS`  - 1 Minute Bars
* `CME_DAILY`  - End of Day Metrics




## CME

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





## CME_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## CME_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


