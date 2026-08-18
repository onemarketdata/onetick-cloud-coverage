# Cboe EDGA

Cboe EDGA Exchange (EDGA) is a U.S. equities market that transitioned from an inverted to a tier-free, maker-taker pricing structure. It offers unique features like hidden price improvement, retail priority, and periodic auctions to optimize order execution

* Country: USA United States [US]
* Mkt Hours: 09:30-16:00
* Time Zone: America/New_York
* Start Date: 20250501
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes



Details are provided below

* [Table Schemas for EDGA](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/EDGA_schemas.html.md)
* [Field Enumerations for EDGA](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/EDGA_enumerations.html.md)
* [Trading Hours for EDGA](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/EDGA_trading_hours.html.md)
* [Recent Holidays for EDGA](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/EDGA_holidays.html.md)



Includes the following coverage:

#### EDGA -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| ADR                |            402 | 3.08%        |
| Corporate Bond     |             57 | 0.44%        |
| ETF                |           5422 | 41.53%       |
| ETN                |             51 | 0.39%        |
| ETV                |             88 | 0.67%        |
| Equity             |           5212 | 39.92%       |
| Fund               |            338 | 2.59%        |
| Preferred Stock    |            438 | 3.36%        |
| Right              |            112 | 0.86%        |
| Structured Product |            158 | 1.21%        |
| Test               |             21 | 0.16%        |
| Unit               |            304 | 2.33%        |
| Unknown            |             12 | 0.09%        |
| Warrant            |            440 | 3.37%        |
| Total              |          13055 | 100%         |


Consists of 2 Databases

* [EDGA]()  - Tick Data
* [EDGA_DAILY]()  - End of Day Metrics




## EDGA

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## EDGA_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



## Table Of Contents

* [Cboe EDGA Schemas](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/EDGA_schemas.html.md)
* [Cboe EDGA Enumerations](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/EDGA_enumerations.html.md)
* [Cboe EDGA Trading Hours](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/EDGA_trading_hours.html.md)
* [Cboe EDGA Market Holidays](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/EDGA_holidays.html.md)
