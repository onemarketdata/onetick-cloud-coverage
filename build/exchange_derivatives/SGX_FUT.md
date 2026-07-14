# Singapore Exchange - Equity + Fixed Income Derivatives

The Singapore Exchange ( SGX ) offers trading in equity and fixed income derivatives.

* Country: Singapore [SG]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Singapore
* Start Date: 20110509
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for SGX_FUT`
* `Field Enumerations for SGX_FUT`
* `Trading Hours for SGX_FUT`
* `Recent Holidays for SGX_FUT`



Includes the following coverage:

#### SGX_FUT -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |           1206 | 35.67%       |
| Futures Spread  |           2175 | 64.33%       |
| Total           |           3381 | 100%         |


Consists of 3 Databases

* `SGX_FUT`  - Tick Data
* `SGX_FUT_BARS`  - 1 Minute Bars
* `SGX_FUT_DAILY`  - End of Day Metrics




## SGX_FUT

Database includes the following tick types:

* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## SGX_FUT_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## SGX_FUT_DAILY

Database includes the following tick types:

* STAT - Static data, e.g. ISIN, description, security type


