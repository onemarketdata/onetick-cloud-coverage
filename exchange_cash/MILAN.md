# Euronext Milan (Borsa Italiana) - Equities

Borsa Italiana is Italy’s main stock exchange located in Milan, facilitating trading in Italian equities.

* Country: Italy [IT]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Rome
* Start Date: 20120102
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for MILAN`
* `Field Enumerations for MILAN`
* `Trading Hours for MILAN`
* `Recent Holidays for MILAN`



Includes the following coverage:

#### MILAN -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Bond            |              2 | 0.04%        |
| ETF             |           2437 | 53.86%       |
| Equity          |           2010 | 44.42%       |
| Investment Fund |             72 | 1.59%        |
| Preferred Stock |              4 | 0.09%        |
| Total           |           4525 | 100%         |


Consists of 4 Databases

* `MILAN`  - Tick Data
* `MILAN_BARS`  - 1 Minute Bars
* `MILAN_DAILY`  - End of Day Metrics
* `MILAN_LATEST`  - Real Time Latest Values




## MILAN

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## MILAN_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* LAT_1M - 1-minute Latency bars for real time delivered data
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars



