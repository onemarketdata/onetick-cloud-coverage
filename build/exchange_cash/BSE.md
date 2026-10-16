# BSE (Bombay Stock Exchange)

The Bombay Stock Exchange is one of the largest securities markets. It is located on Dalal Street, Mumbai and lists over 6000 companies.

* Country: India [IN]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Kolkata
* Start Date: 20140930 - Equities, 20260209 - Derivatives
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for BSE`
* `Field Enumerations for BSE`
* `Trading Hours for BSE`
* `Recent Holidays for BSE`



Includes the following coverage:

#### BSE -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Corporate Bond  |           9987 | 16.89%       |
| ETF             |            105 | 0.18%        |
| Equity          |           6729 | 11.38%       |
| Future          |            641 | 1.08%        |
| Futures Spread  |             63 | 0.11%        |
| Government Bond |           2696 | 4.56%        |
| Option          |          38012 | 64.27%       |
| Option Spread   |            657 | 1.11%        |
| Unknown         |            254 | 0.43%        |
| Total           |          59144 | 100%         |


Consists of 3 Databases

* `BSE`  - Tick Data
* `BSE_BARS`  - 1 Minute Bars
* `BSE_DAILY`  - End of Day Metrics




## BSE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## BSE_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## BSE_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


