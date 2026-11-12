# London Metal Exchange

Futures, options, spreads and indices with Trades, Quotes and bars from the London Metal Exchange (LME), with history from August 2013. LME prices are the global reference for industrial metals such as copper, aluminium, zinc, nickel, lead and tin, and its prompt-date structure lets contracts settle on daily, weekly or monthly dates up to several years out.

* Country: UK United Kindom [GB]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/London
* Start Date: 20130805
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices:



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
| Future          |           6695 | 39.98%       |
| Futures Spread  |           9081 | 54.23%       |
| Option          |            966 | 5.77%        |
| Total           |          16745 | 100%         |


Consists of 3 Databases

* `LME`  - Tick Data
* `LME_BARS`  - 1 Minute Bars
* `LME_DAILY`  - End of Day Metrics




## LME

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IDX - Index values
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


