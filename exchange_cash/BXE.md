# Cboe BXE (BATS Europe)

Cboe BXE, formerly BATS Europe, is a pan-European MTF offering trading in equities, ETFs, and other securities across multiple European markets.

* Country: Austria Belgium Switzerland Czechia Germany Denmark Spain Finland France UK United Kindom Greece Hungary Ireland Iceland Italy Luxembourg Netherlands Norway Poland Portugal Sweden [AT BE CH CY CZ DE DK ES FI FR GB GR HU IE IS IT NL NO PL PT SE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/London
* Start Date: 20110704
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for BXE`
* `Field Enumerations for BXE`
* `Trading Hours for BXE`
* `Recent Holidays for BXE`



Includes the following coverage:

#### BXE -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Depository Receipt |             36 | 0.38%        |
| ETC                |            489 | 5.21%        |
| ETF                |           5367 | 57.13%       |
| ETN                |            176 | 1.87%        |
| Equity             |           3300 | 35.13%       |
| Test               |             26 | 0.28%        |
| Total              |           9394 | 100%         |


Consists of 3 Databases

* `BXE`  - Tick Data
* `BXE_BARS`  - 1 Minute Bars
* `BXE_DAILY`  - End of Day Metrics




## BXE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## BXE_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## BXE_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


