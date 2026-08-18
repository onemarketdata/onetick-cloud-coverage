# Shanghai Futures Exchange

The Shanghai Futures Exchange is one of China’s four futures exchanges, trading futures contracts across asset classes like metals, energy, chemicals and more.

* Country: China [CN]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Hong_Kong
* Start Date: 20151012
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* [Table Schemas for SHFE](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/SHFE_schemas.html.md)
* [Field Enumerations for SHFE](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/SHFE_enumerations.html.md)
* [Trading Hours for SHFE](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/SHFE_trading_hours.html.md)
* [Recent Holidays for SHFE](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/SHFE_holidays.html.md)



Includes the following coverage:

#### SHFE -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |            238 | 3.34%        |
| Option          |           6880 | 96.66%       |
| Total           |           7118 | 100%         |


Consists of 3 Databases

* [SHFE]()  - Tick Data
* [SHFE_BARS]()  - 1 Minute Bars
* [SHFE_DAILY]()  - End of Day Metrics




## SHFE

Database includes the following tick types:

* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## SHFE_BARS

Database includes the following tick types:

* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## SHFE_DAILY

Database includes the following tick types:

* STAT - Static data, e.g. ISIN, description, security type



## Table Of Contents

* [Shanghai Futures Exchange Schemas](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/SHFE_schemas.html.md)
* [Shanghai Futures Exchange Enumerations](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/SHFE_enumerations.html.md)
* [Shanghai Futures Exchange Trading Hours](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/SHFE_trading_hours.html.md)
* [Shanghai Futures Exchange Market Holidays](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/SHFE_holidays.html.md)
