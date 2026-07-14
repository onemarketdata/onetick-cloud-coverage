# Borsa Italiana Derivatives (IDEM)

IDEM is the derivatives market operated by Borsa Italiana (Italian Stock Exchange), trading equity, energy and fixed income derivatives

* Country: Italy [IT]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Rome
* Start Date: 20110411
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for IDEM`
* `Field Enumerations for IDEM`
* `Trading Hours for IDEM`
* `Recent Holidays for IDEM`



Includes the following coverage:

#### IDEM -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |            581 | 97.48%       |
| Futures Spread  |             15 | 2.52%        |
| Total           |            596 | 100%         |


Consists of 3 Databases

* `IDEM`  - Tick Data
* `IDEM_BARS`  - 1 Minute Bars
* `IDEM_DAILY`  - End of Day Metrics




## IDEM

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## IDEM_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## IDEM_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type
* TRD_1D - Daily trade bars


