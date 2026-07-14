# Global FX (Spots, Forwards, NDFs)

Global Forex markets offer trading in spot, forward, and non-deliverable forward (NDF) contracts on various currency pairs.

* Country: Global [Global]
* Mkt Hours: 00:00-24:00
* Time Zone: UTC
* Start Date: 20080507
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for GLOBAL_FX`
* `Field Enumerations for GLOBAL_FX`
* `Trading Hours for GLOBAL_FX`
* `Recent Holidays for GLOBAL_FX`



Includes the following coverage:

#### GLOBAL_FX -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| FX Forward      |           4915 | 56.32%       |
| FX NDF          |            252 | 2.89%        |
| FX Spot         |           3560 | 40.79%       |
| Total           |           8727 | 100%         |


Consists of 3 Databases

* `GLOBAL_FX`  - Tick Data
* `GLOBAL_FX_BARS`  - 1 Minute Bars
* `GLOBAL_FX_DAILY`  - End of Day Metrics




## GLOBAL_FX

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IDX - Index values
* INTRADAY - Intraday Bid / Offer Quotes
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type





## GLOBAL_FX_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* QTE_1M - 1-minute quote bars





## GLOBAL_FX_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


