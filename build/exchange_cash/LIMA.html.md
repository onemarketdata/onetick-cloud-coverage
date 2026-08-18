# Lima Stock Exchange

The Lima Stock Exchange is the official stock exchange of Peru where securities like stocks, bonds and derivatives are traded.

* Country: Peru [PE]
* Mkt Hours: 08:00-17:00
* Time Zone: America/Sao_Paulo
* Start Date: 20160627
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* [Table Schemas for LIMA](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/LIMA_schemas.html.md)
* [Field Enumerations for LIMA](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/LIMA_enumerations.html.md)
* [Trading Hours for LIMA](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/LIMA_trading_hours.html.md)
* [Recent Holidays for LIMA](https://cloudcoverage.docs.sol.onetick.com/exchange_cash/LIMA_holidays.html.md)



Includes the following coverage:

#### LIMA -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Bond            |            936 | 41.82%       |
| ETF             |            339 | 15.15%       |
| Equity          |            840 | 37.53%       |
| Index           |              3 | 0.13%        |
| Unknown         |            120 | 5.36%        |
| Total           |           2238 | 100%         |


Consists of 2 Databases

* [LIMA]()  - Tick Data
* [LIMA_BARS]()  - 1 Minute Bars




## LIMA

Database includes the following tick types:

* IDX - Index values
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## LIMA_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars


