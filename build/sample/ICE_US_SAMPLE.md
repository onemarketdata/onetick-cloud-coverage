# ICE US Sample

A sample of the ICE Futures U.S. database covering a subset of symbols between January 2, 2024 and March 31, 2024. ICE Futures U.S. is the main US venue for soft commodities and the U.S. Dollar Index. The sample includes trades, quotes, book depth and bars for futures, options and spreads on CC (Cocoa), CT (Cotton No. 2), KC (Coffee C) and DX (U.S. Dollar Index).

* Country: USA United States [US]
* Mkt Hours: 09:30-16:00
* Time Zone: America/New_York
* Start Date: 20240102
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Arrival
* Key Indices:



Details are provided below

* `Table Schemas for ICE_US_SAMPLE`
* `Field Enumerations for ICE_US_SAMPLE`
* `Trading Hours for ICE_US_SAMPLE`
* `Recent Holidays for ICE_US_SAMPLE`



Includes the following coverage:

#### ICE_US_SAMPLE -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |             40 | 100.0%       |
| Total           |             40 | 100%         |


Consists of 2 Databases

* `ICE_US_SAMPLE`  - Tick Data
* `ICE_US_SAMPLE_BARS`  - 1 Minute Bars




## ICE_US_SAMPLE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## ICE_US_SAMPLE_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars


