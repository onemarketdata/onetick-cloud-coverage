# Nasdaq Nordic - Derivatives

In addition to equities, Nasdaq Nordic also offers trading in Nordic derivatives like stock options and futures.

* Country: Sweden Denmark Finland [SE DK FI]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Stockholm
* Start Date: 20170102
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for NORDIC_FUT`
* `Field Enumerations for NORDIC_FUT`
* `Trading Hours for NORDIC_FUT`
* `Recent Holidays for NORDIC_FUT`



Includes the following coverage:

#### NORDIC_FUT -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Forward         |           1810 | 2.45%        |
| Future          |           2852 | 3.87%        |
| Futures Spread  |              8 | 0.01%        |
| Option          |          69044 | 93.61%       |
| Option Spread   |             35 | 0.05%        |
| Unknown         |              6 | 0.01%        |
| Total           |          73755 | 100%         |


Consists of 3 Databases

* `NORDIC_FUT`  - Tick Data
* `NORDIC_FUT_BARS`  - 1 Minute Bars
* `NORDIC_FUT_DAILY`  - End of Day Metrics




## NORDIC_FUT

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## NORDIC_FUT_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## NORDIC_FUT_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type
* TRD_1D - Daily trade bars


