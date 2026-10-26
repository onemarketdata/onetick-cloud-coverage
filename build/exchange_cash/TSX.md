# Toronto Stock Exchange

The Toronto Stock Exchange is the largest equity market in Canada trading senior equities.

* Country: Canada [CA]
* Mkt Hours: 09:00-16:00
* Time Zone: America/Toronto
* Start Date: 20171101
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for TSX`
* `Field Enumerations for TSX`
* `Trading Hours for TSX`
* `Recent Holidays for TSX`



Includes the following coverage:

#### TSX -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Debenture          |             57 | 1.79%        |
| Depositary Receipt |            143 | 4.5%         |
| ETF                |           1868 | 58.8%        |
| Equity             |            704 | 22.16%       |
| Fund               |             27 | 0.85%        |
| Mutual Fund        |              3 | 0.09%        |
| Preferred Stock    |            277 | 8.72%        |
| REIT               |             33 | 1.04%        |
| Right              |              3 | 0.09%        |
| Test               |             45 | 1.42%        |
| Warrant            |             17 | 0.54%        |
| Total              |           3177 | 100%         |


Consists of 3 Databases

* `TSX`  - Tick Data
* `TSX_BARS`  - 1 Minute Bars
* `TSX_DAILY`  - End of Day Metrics




## TSX

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## TSX_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## TSX_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


