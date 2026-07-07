# Warsaw Stock Exchange - Derivatives

Warsaw Stock Exchange operates a financial instruments exchange. The Exchange trades equities, fixed income, derivatives, listings, bonds, subscription rights.

* Country: Poland [PL]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Berlin
* Start Date: 20221121
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for WARSAW_FUT`
* `Field Enumerations for WARSAW_FUT`
* `Trading Hours for WARSAW_FUT`
* `Recent Holidays for WARSAW_FUT`



Includes the following coverage:

#### WARSAW_FUT -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |            172 | 38.91%       |
| Option          |            270 | 61.09%       |
| Total           |            442 | 100%         |


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


