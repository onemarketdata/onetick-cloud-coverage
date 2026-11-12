# Nasdaq Nordic - Derivatives

Futures, options and spreads with Trades, Quotes, bars and book depth from Nasdaq’s Nordic derivatives markets, with history from January 2017. Key contracts include OMX Stockholm 30 index futures and options, single-stock options and futures on Nordic companies, and Nordic interest rate derivatives.

* Country: Sweden Denmark Finland [SE DK FI]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Stockholm
* Start Date: 20170102
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Arrival
* Key Indices:



Details are provided below

* `Table Schemas for NORDIC_FUT`
* `Field Enumerations for NORDIC_FUT`
* `Trading Hours for NORDIC_FUT`
* `Recent Holidays for NORDIC_FUT`



Includes the following coverage:

#### NORDIC_FUT -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Forward         |           1826 | 2.43%        |
| Future          |           2887 | 3.83%        |
| Futures Spread  |              8 | 0.01%        |
| Option          |          70518 | 93.65%       |
| Option Spread   |             51 | 0.07%        |
| Unknown         |              6 | 0.01%        |
| Total           |          75296 | 100%         |


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


