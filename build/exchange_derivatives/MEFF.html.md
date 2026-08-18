# MEFF Exchange

MEFF is the Spanish derivatives exchange, offering trading in futures and options on Spanish equities, indices, and interest rates.

* Country: Spain [ES]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Madrid
* Start Date: 20091211
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* [Table Schemas for MEFF](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/MEFF_schemas.html.md)
* [Field Enumerations for MEFF](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/MEFF_enumerations.html.md)
* [Trading Hours for MEFF](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/MEFF_trading_hours.html.md)
* [Recent Holidays for MEFF](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/MEFF_holidays.html.md)



Includes the following coverage:

#### MEFF -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |           1743 | 1.96%        |
| Futures Spread  |             16 | 0.02%        |
| Option          |          87100 | 98.01%       |
| Unknown         |              6 | 0.01%        |
| Total           |          88865 | 100%         |


Consists of 3 Databases

* [MEFF]()  - Tick Data
* [MEFF_BARS]()  - 1 Minute Bars
* [MEFF_DAILY]()  - End of Day Metrics




## MEFF

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL - Market depth data, aggregated by price point (MBP)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





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



## Table Of Contents

* [MEFF Exchange Schemas](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/MEFF_schemas.html.md)
* [MEFF Exchange Enumerations](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/MEFF_enumerations.html.md)
* [MEFF Exchange Trading Hours](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/MEFF_trading_hours.html.md)
* [MEFF Exchange Market Holidays](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/MEFF_holidays.html.md)
