# Cboe DXE

Trades, quotes and bars from Cboe DXE, the Amsterdam-based EU order book that Cboe Europe launched in October 2019 so EU clients kept access to its services after Brexit, with history from October 2019. It has lit, dark, periodic auction and off-book segments and trades equities and ETFs listed across Europe, so use it for EU trading that moved from BXE and CXE. Covered stocks include constituents of the EURO STOXX 50, DAX, CAC 40 and AEX.  A consolidated tape for all European equity markets is provided in the EU_COMP dataset.

* Country: Austria Belgium Switzerland Czechia Germany Denmark Spain Finland France UK United Kindom Greece Hungary Ireland Iceland Italy Luxembourg Netherlands Norway Poland Portugal Sweden [AT BE CH CY CZ DE DK ES FI FR GB GR HU IE IS IT NL NO PL PT SE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Amsterdam
* Start Date: 20191001
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: STOXX 50 Index [TDI_IDX::VH], Euro STOXX 50 Index [TDI_IDX::XX]



Details are provided below

* `Table Schemas for DXE`
* `Field Enumerations for DXE`
* `Trading Hours for DXE`
* `Recent Holidays for DXE`



Includes the following coverage:

#### DXE -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| ETC             |            233 | 3.81%        |
| ETF             |           3152 | 51.55%       |
| ETN             |             88 | 1.44%        |
| Equity          |           2616 | 42.78%       |
| Test            |             26 | 0.43%        |
| Total           |           6115 | 100%         |


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


