# Borsa Italiana Derivatives (IDEM)

Futures and spreads with Trades, Quotes and bars from Euronext Derivatives Milan (formerly IDEM), Borsa Italiana’s derivatives market, now part of Euronext, with history from April 2011. Key contracts include FTSE MIB index futures and mini futures, single-stock futures on Italian companies, and Italian power futures.

* Country: Italy [IT]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Rome
* Start Date: 20110411
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices:



Details are provided below

* `Table Schemas for IDEM`
* `Field Enumerations for IDEM`
* `Trading Hours for IDEM`
* `Recent Holidays for IDEM`



Includes the following coverage:

#### IDEM -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |            632 | 97.98%       |
| Futures Spread  |             13 | 2.02%        |
| Total           |            645 | 100%         |


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





## IDEM_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars





## IDEM_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


