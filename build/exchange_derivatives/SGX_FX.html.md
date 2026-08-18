# Singapore Exchange - FX Derivatives

The Singapore Exchange ( SGX ) offers trading in foreign exchange derivatives

* Country: Singapore [SG]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Singapore
* Start Date: 20140908
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* [Table Schemas for SGX_FX](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/SGX_FX_schemas.html.md)
* [Field Enumerations for SGX_FX](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/SGX_FX_enumerations.html.md)
* [Trading Hours for SGX_FX](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/SGX_FX_trading_hours.html.md)
* [Recent Holidays for SGX_FX](https://cloudcoverage.docs.sol.onetick.com/exchange_derivatives/SGX_FX_holidays.html.md)



Includes the following coverage:

#### SGX_FX -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |            391 | 27.55%       |
| Futures Spread  |           1028 | 72.45%       |
| Total           |           1419 | 100%         |


Consists of 3 Databases

* [SGX_FX]()  - Tick Data
* [SGX_FX_BARS]()  - 1 Minute Bars
* [SGX_FX_DAILY]()  - End of Day Metrics




## SGX_FX

Database includes the following tick types:

* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## SGX_FX_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## SGX_FX_DAILY

Database includes the following tick types:

* STAT - Static data, e.g. ISIN, description, security type


