# MIAX Futures Exchange

MIAX Futures provides the Minneapolis Grain Exchange, offering trading in Hard Red Spring Wheat Futures & Options.

* Country: USA United States [US]
* Mkt Hours: 17:00-14:20
* Time Zone: America/New_York
* Start Date: 20250630
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for MIAX_FUT`
* `Field Enumerations for MIAX_FUT`
* `Trading Hours for MIAX_FUT`
* `Recent Holidays for MIAX_FUT`



Includes the following coverage:

#### MIAX_FUT -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |             15 | 1.61%        |
| Futures Spread  |             33 | 3.55%        |
| Option          |            882 | 94.84%       |
| Total           |            930 | 100%         |


Consists of 3 Databases

* `MIAX_FUT`  - Tick Data
* `MIAX_FUT_BARS`  - 1 Minute Bars
* `MIAX_FUT_DAILY`  - End of Day Metrics




## MIAX_FUT

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## MIAX_FUT_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## MIAX_FUT_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


