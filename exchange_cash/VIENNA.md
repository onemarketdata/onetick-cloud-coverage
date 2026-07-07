# Vienna Stock Exchange

The Vienna Stock Exchange is the only stock exchange in Austria trading Austrian equities and bonds.

* Country: Austria [AT]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Berlin
* Start Date: 20120601
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for VIENNA`
* `Field Enumerations for VIENNA`
* `Trading Hours for VIENNA`
* `Recent Holidays for VIENNA`



Includes the following coverage:

#### VIENNA -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Bond               |          48196 | 84.71%       |
| Convertible Bond   |            290 | 0.51%        |
| Depository Receipt |             24 | 0.04%        |
| ETF                |            384 | 0.67%        |
| Equity             |           1046 | 1.84%        |
| Investment Fund    |              6 | 0.01%        |
| Municipal Bond     |             43 | 0.08%        |
| Preferred Stock    |             15 | 0.03%        |
| Structured Product |           6893 | 12.11%       |
| Total              |          56897 | 100%         |


Consists of 4 Databases

* `VIENNA`  - Tick Data
* `VIENNA_BARS`  - 1 Minute Bars
* `VIENNA_DAILY`  - End of Day Metrics
* `VIENNA_LATEST`  - Real Time Latest Values




## VIENNA

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL - Market depth data, aggregated by price point (MBP)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## VIENNA_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## VIENNA_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type





## VIENNA_LATEST

Database includes the following tick types:

* TRD - Trades
* QTE - Best bid / offer quotes


