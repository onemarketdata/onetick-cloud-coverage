# Hong Kong Futures Exchange

The Hong Kong Futures Exchange (HKFE) offers trading in futures and options on equities, indices, interest rates, and commodities.

* Country: Hong Kong SAR China [HK]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Hong_Kong
* Start Date: 20091110
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for HKFE`
* `Field Enumerations for HKFE`
* `Trading Hours for HKFE`
* `Recent Holidays for HKFE`



Includes the following coverage:

#### HKFE -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |           1232 | 44.11%       |
| Futures Spread  |           1561 | 55.89%       |
| Total           |           2793 | 100%         |


Consists of 2 Databases

* `HKFE`  - Tick Data
* `HKFE_BARS`  - 1 Minute Bars




## HKFE

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## HKFE_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars


