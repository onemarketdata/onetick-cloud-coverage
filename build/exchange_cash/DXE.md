# Cboe DXE

Cboe DXE is Cboe’s institutional equities trading book, providing trading across 23 European markets.

* Country: Austria Belgium Switzerland Czechia Germany Denmark Spain Finland France UK United Kindom Greece Hungary Ireland Iceland Italy Luxembourg Netherlands Norway Poland Portugal Sweden [AT BE CH CY CZ DE DK ES FI FR GB GR HU IE IS IT NL NO PL PT SE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Amsterdam
* Start Date: 20191001
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for DXE`
* `Field Enumerations for DXE`
* `Trading Hours for DXE`
* `Recent Holidays for DXE`



Includes the following coverage:

#### DXE -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| ETC             |            224 | 3.78%        |
| ETF             |           3121 | 52.7%        |
| ETN             |             86 | 1.45%        |
| Equity          |           2465 | 41.62%       |
| Test            |             26 | 0.44%        |
| Total           |           5922 | 100%         |


Consists of 3 Databases

* `DXE`  - Tick Data
* `DXE_BARS`  - 1 Minute Bars
* `DXE_DAILY`  - End of Day Metrics




## DXE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## DXE_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## DXE_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


