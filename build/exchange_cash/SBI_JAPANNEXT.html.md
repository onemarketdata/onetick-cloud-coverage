# Japannext J-Market

Japannext operates the J-Market, an alternative trading system for Japanese equities.

* Country: Japan [JP]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Tokyo
* Start Date: 20140318
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* [Table Schemas for SBI_JAPANNEXT](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/SBI_JAPANNEXT_schemas.html.md)
* [Field Enumerations for SBI_JAPANNEXT](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/SBI_JAPANNEXT_enumerations.html.md)
* [Trading Hours for SBI_JAPANNEXT](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/SBI_JAPANNEXT_trading_hours.html.md)
* [Recent Holidays for SBI_JAPANNEXT](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/SBI_JAPANNEXT_holidays.html.md)



Includes the following coverage:

#### SBI_JAPANNEXT -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Total           |            477 | 100%         |


Consists of 2 Databases

* [SBI_JAPANNEXT]()  - Tick Data
* [SBI_JAPANNEXT_BARS]()  - 1 Minute Bars




## SBI_JAPANNEXT

Database includes the following tick types:

* MKT - Market phase / instrument status information
* PRL - Market depth data, aggregated by price point (MBP)
* QTE - Best bid / offer quotes
* TRD - Trades





## SBI_JAPANNEXT_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars


