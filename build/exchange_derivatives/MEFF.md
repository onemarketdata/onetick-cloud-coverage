# MEFF Exchange

Futures, options and spreads with Trades, Quotes, bars and book depth from MEFF, BME’s Spanish derivatives exchange, with futures from December 2009 and options from January 2025. Key contracts include IBEX 35 and Mini IBEX 35 futures and options, Spanish single-stock futures and options, and Spanish power futures.

* Country: Spain [ES]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Madrid
* Start Date: 20091211 - Futures, 20250102 - Options
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Arrival
* Key Indices:



Details are provided below

* `Table Schemas for MEFF`
* `Field Enumerations for MEFF`
* `Trading Hours for MEFF`
* `Recent Holidays for MEFF`



Includes the following coverage:

#### MEFF -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |           1705 | 1.91%        |
| Futures Spread  |              7 | 0.01%        |
| Option          |          87606 | 98.08%       |
| Unknown         |              7 | 0.01%        |
| Total           |          89325 | 100%         |


Consists of 3 Databases

* `MEFF`  - Tick Data
* `MEFF_BARS`  - 1 Minute Bars
* `MEFF_DAILY`  - End of Day Metrics




## MEFF

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* PRL - Market depth data, aggregated by price point (MBP)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type





## MEFF_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## MEFF_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


