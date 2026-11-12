# Singapore Exchange (SGX)

Trades, quotes and bars from the Singapore Exchange (SGX) securities market, with history from July 2014, covering the Mainboard and Catalist as well as ETFs, REITs and bonds. Covered stocks include constituents of the Straits Times Index (STI); index values are in ST_IDX.

* Country: Singapore [SG]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Singapore
* Start Date: 20140701
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: Straits Times Index [TDI_IDX::ST]



Details are provided below

* `Table Schemas for SGX`
* `Field Enumerations for SGX`
* `Trading Hours for SGX`
* `Recent Holidays for SGX`



Includes the following coverage:

#### SGX -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Bond               |           9239 | 87.66%       |
| Depository Receipt |             44 | 0.42%        |
| ETF                |            110 | 1.04%        |
| Equity             |            569 | 5.4%         |
| Investment Fund    |              3 | 0.03%        |
| Preferred Stock    |              2 | 0.02%        |
| REIT               |             26 | 0.25%        |
| Right              |              2 | 0.02%        |
| Structured Product |            524 | 4.97%        |
| Unit Trust         |             20 | 0.19%        |
| Total              |          10539 | 100%         |


Consists of 3 Databases

* `SGX`  - Tick Data
* `SGX_BARS`  - 1 Minute Bars
* `SGX_DAILY`  - End of Day Metrics




## SGX

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* QTE_BUY_IN - BBO quotes for trading on the Buy-in market (e.g. SGX, Kuwait)
* QTE_ODD_LOT - BBO quotes from the Odd Lot book, for exchanges that have a separate order book for odd lots
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## SGX_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## SGX_DAILY

Database includes the following tick types:

* STAT - Static data, e.g. ISIN, description, security type


