# Cboe CXE (Chi-X Europe)

Cboe CXE, formerly Chi-X Europe, is a pan-European equities exchange and multilateral trading facility operated by Cboe Global Markets.

* Country: Austria Belgium Switzerland Czechia Germany Denmark Spain Finland France UK United Kindom Greece Hungary Ireland Iceland Italy Luxembourg Netherlands Norway Poland Portugal Sweden [AT BE CH CY CZ DE DK ES FI FR GB GR HU IE IS IT NL NO PL PT SE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/London
* Start Date: 20090119
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for CXE`
* `Field Enumerations for CXE`
* `Trading Hours for CXE`
* `Recent Holidays for CXE`



Includes the following coverage:

#### CXE -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Depository Receipt |             36 | 0.38%        |
| ETC                |            489 | 5.21%        |
| ETF                |           5366 | 57.12%       |
| ETN                |            176 | 1.87%        |
| Equity             |           3300 | 35.13%       |
| Test               |             26 | 0.28%        |
| Unknown            |              1 | 0.01%        |
| Total              |           9394 | 100%         |


Consists of 3 Databases

* `CXE`  - Tick Data
* `CXE_BARS`  - 1 Minute Bars
* `CXE_DAILY`  - End of Day Metrics




## CXE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## CXE_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## CXE_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


