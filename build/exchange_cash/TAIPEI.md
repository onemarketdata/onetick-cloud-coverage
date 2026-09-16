# Taipei Exchange

The Taipei Exchange is a stock exchange in Taiwan that trades Taiwanese equities and bonds.

* Country: Taiwan [TW]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Taipei
* Start Date: 20160602
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for TAIPEI`
* `Field Enumerations for TAIPEI`
* `Trading Hours for TAIPEI`
* `Recent Holidays for TAIPEI`



Includes the following coverage:

#### TAIPEI -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Corporate Bond  |            395 | 3.22%        |
| ETF             |            118 | 0.96%        |
| ETN             |              7 | 0.06%        |
| Equity          |           1257 | 10.25%       |
| Index           |            102 | 0.83%        |
| Investment Fund |              3 | 0.02%        |
| Preferred Stock |              1 | 0.01%        |
| Unknown         |             31 | 0.25%        |
| Warrant         |          10349 | 84.39%       |
| Total           |          12263 | 100%         |


Consists of 3 Databases

* `TAIPEI`  - Tick Data
* `TAIPEI_BARS`  - 1 Minute Bars
* `TAIPEI_DAILY`  - End of Day Metrics




## TAIPEI

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IDX - Index values
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* QTE_ODD_LOT - BBO quotes from the Odd Lot book, for exchanges that have a separate order book for odd lots
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## TAIPEI_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## TAIPEI_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


