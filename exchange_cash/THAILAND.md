# Stock Exchange of Thailand

The Stock Exchange of Thailand facilitates trading in Thai company stocks, bonds, derivatives and other products.

* Country: Thailand [TH]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Bangkok
* Start Date: 20140930
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for THAILAND`
* `Field Enumerations for THAILAND`
* `Trading Hours for THAILAND`
* `Recent Holidays for THAILAND`



Includes the following coverage:

#### THAILAND -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| ETF                |             13 | 0.23%        |
| Equity             |           2179 | 38.79%       |
| Fund               |             41 | 0.73%        |
| Index              |             58 | 1.03%        |
| NVDR               |           1428 | 25.42%       |
| Preferred Stock    |             16 | 0.28%        |
| REIT               |             64 | 1.14%        |
| Structured Product |           1727 | 30.74%       |
| Unknown            |              4 | 0.07%        |
| Warrant            |             88 | 1.57%        |
| Total              |           5618 | 100%         |


Consists of 3 Databases

* `THAILAND`  - Tick Data
* `THAILAND_BARS`  - 1 Minute Bars
* `THAILAND_DAILY`  - End of Day Metrics




## THAILAND

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IDX - Index values
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL - Market depth data, aggregated by price point (MBP)
* PRL_ODD_LOT - Odd lot orderbook data, for exchanges that have a separate book for odd lots
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## THAILAND_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## THAILAND_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type
* TRD_1D - Daily trade bars


