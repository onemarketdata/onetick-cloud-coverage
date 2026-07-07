# ASX 24 (Sydney Futures Exchange)

ASX 24, formerly the Sydney Futures Exchange, offers trading in futures and options on interest rates, equities, commodities, and currencies.

* Country: Australia [AU]
* Mkt Hours: 08:00-17:00
* Time Zone: Australia/Sydney
* Start Date: 20110411
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for ASX_FUT`
* `Field Enumerations for ASX_FUT`
* `Trading Hours for ASX_FUT`
* `Recent Holidays for ASX_FUT`



Includes the following coverage:

#### ASX_FUT -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |            705 | 28.23%       |
| Futures Spread  |           1792 | 71.77%       |
| Total           |           2497 | 100%         |


Consists of 3 Databases

* `ASX_FUT`  - Tick Data
* `ASX_FUT_BARS`  - 1 Minute Bars
* `ASX_FUT_DAILY`  - End of Day Metrics




## ASX_FUT

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## ASX_FUT_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## ASX_FUT_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type
* TRD_1D - Daily trade bars


