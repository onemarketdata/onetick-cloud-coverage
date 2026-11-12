# Warsaw Stock Exchange - Derivatives

Futures and options with Trades, Quotes,  bars and book depth from the derivatives market of the Warsaw Stock Exchange (GPW), with history from November 2022. The flagship contracts are futures and options on the WIG20 index of Poland’s largest companies, first listed in 1998 as the exchange’s first derivatives, alongside mWIG40 index futures, single-stock futures and USD, EUR, GBP and CHF currency futures against the zloty.

* Country: Poland [PL]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Warsaw
* Start Date: 20221121
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Arrival
* Key Indices:



Details are provided below

* `Table Schemas for WARSAW_FUT`
* `Field Enumerations for WARSAW_FUT`
* `Trading Hours for WARSAW_FUT`
* `Recent Holidays for WARSAW_FUT`



Includes the following coverage:

#### WARSAW_FUT -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |            172 | 36.6%        |
| Option          |            298 | 63.4%        |
| Total           |            470 | 100%         |


Consists of 2 Databases

* `WARSAW_FUT`  - Tick Data
* `WARSAW_FUT_DAILY`  - End of Day Metrics




## WARSAW_FUT

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## WARSAW_FUT_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


