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
| Debenture          |             59 | 1.89%        |
| Depositary Receipt |            132 | 4.22%        |
| ETF                |           1804 | 57.67%       |
| Equity             |            722 | 23.08%       |
| Fund               |             29 | 0.93%        |
| Mutual Fund        |              3 | 0.1%         |
| Preferred Stock    |            278 | 8.89%        |
| REIT               |             34 | 1.09%        |
| Right              |              3 | 0.1%         |
| Test               |             45 | 1.44%        |
| Warrant            |             19 | 0.61%        |
| Total              |           3128 | 100%         |


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
* TRD_1D - Daily trade bars


