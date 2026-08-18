# Nasdaq CXC

Nasdaq CXC is Nasdaq’s dark pool ATS that allows participants to execute orders anonymously at or better than the NBBO without displaying quotes.

* Country: Canada [CA]
* Mkt Hours: 09:00-16:00
* Time Zone: America/Toronto
* Start Date: 20170529
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes



Details are provided below

* [Table Schemas for CXC](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/CXC_schemas.html.md)
* [Field Enumerations for CXC](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/CXC_enumerations.html.md)
* [Trading Hours for CXC](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/CXC_trading_hours.html.md)
* [Recent Holidays for CXC](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/CXC_holidays.html.md)



Includes the following coverage:

#### CXC -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Debenture          |             65 | 1.07%        |
| Depositary Receipt |            205 | 3.38%        |
| ETF                |           2075 | 34.26%       |
| Equity             |           3299 | 54.47%       |
| Preferred Stock    |            289 | 4.77%        |
| Right              |              4 | 0.07%        |
| Test               |             35 | 0.58%        |
| Unknown            |              3 | 0.05%        |
| Warrant            |             82 | 1.35%        |
| Total              |           6057 | 100%         |


Consists of 2 Databases

* [CXC]()  - Tick Data
* [CXC_DAILY]()  - End of Day Metrics




## CXC

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## CXC_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



## Table Of Contents

* [Nasdaq CXC Schemas](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/CXC_schemas.html.md)
* [Nasdaq CXC Enumerations](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/CXC_enumerations.html.md)
* [Nasdaq CXC Trading Hours](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/CXC_trading_hours.html.md)
* [Nasdaq CXC Market Holidays](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/CXC_holidays.html.md)
