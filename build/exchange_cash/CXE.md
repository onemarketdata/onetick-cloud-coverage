# Cboe CXE (Chi-X Europe)

Trades, quotes and bars from Cboe CXE (formerly Chi-X Europe), with history from January 2009. It is one of Cboe’s two pan-European order books, with lit, dark and off-book segments plus Cboe Large in Scale (LIS) block trading, and trades equities and ETFs across many European markets. Covered stocks include constituents of the FTSE 100, DAX, CAC 40 and EURO STOXX 50.

* Country: Austria Belgium Switzerland Czechia Germany Denmark Spain Finland France UK United Kindom Greece Hungary Ireland Iceland Italy Luxembourg Netherlands Norway Poland Portugal Sweden [AT BE CH CY CZ DE DK ES FI FR GB GR HU IE IS IT NL NO PL PT SE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/London
* Start Date: 20090119
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: STOXX 50 Index [TDI_IDX::VH], Euro STOXX 50 Index [TDI_IDX::XX]



Details are provided below

* `Table Schemas for CXE`
* `Field Enumerations for CXE`
* `Trading Hours for CXE`
* `Recent Holidays for CXE`



Includes the following coverage:

#### CXE -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Depository Receipt |             36 | 0.37%        |
| ETC                |            514 | 5.24%        |
| ETF                |           5477 | 55.8%        |
| ETN                |            206 | 2.1%         |
| Equity             |           3547 | 36.14%       |
| Test               |             26 | 0.26%        |
| Unknown            |              9 | 0.09%        |
| Total              |           9815 | 100%         |


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


