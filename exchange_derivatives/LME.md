# London Metal Exchange

The London Metal Exchange (LME) is the world’s largest market for trading base metals futures and options.

* Country: UK United Kindom [GB]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/London
* Start Date: 20130805
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for LME`
* `Field Enumerations for LME`
* `Trading Hours for LME`
* `Recent Holidays for LME`



Includes the following coverage:

#### LME -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| FX              |              3 | 0.02%        |
| Future          |           6899 | 36.05%       |
| Futures Spread  |          10836 | 56.63%       |
| Option          |           1398 | 7.31%        |
| Total           |          19136 | 100%         |


Consists of 3 Databases

* `LME`  - Tick Data
* `LME_BARS`  - 1 Minute Bars
* `LME_DAILY`  - End of Day Metrics




## LME

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IDX - Index values
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## LME_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## LME_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


