# Global FX (Spots, Forwards, NDFs)

Global forex spot, forward and non-deliverable forward (NDF) rates for major, minor and emerging-market currency pairs, with history from May 2008 including quotes, 1 minute bars and daily closes. NDF coverage lets you analyse restricted currencies such as the Indian rupee, Korean won and Brazilian real, which are not freely settled offshore.

* Country: Global [Global]
* Mkt Hours: 00:00-24:00
* Time Zone: UTC
* Start Date: 20080507
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices:



Details are provided below

* `Table Schemas for GLOBAL_FX`
* `Field Enumerations for GLOBAL_FX`
* `Trading Hours for GLOBAL_FX`
* `Recent Holidays for GLOBAL_FX`



Includes the following coverage:

#### GLOBAL_FX -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| FX Forward      |           4925 | 56.69%       |
| FX NDF          |            252 | 2.9%         |
| FX Spot         |           3510 | 40.41%       |
| Total           |           8687 | 100%         |


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


