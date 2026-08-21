# US Consolidated Equities (exc. OTC)

Consolidated data from all US equities exchanges excluding OTC traded securities.  Provides from the US SIP (CTA/UTP)

* Country: USA United States [US]
* Mkt Hours: 09:30-16:00
* Time Zone: America/New_York
* Start Date: 19930104
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for US_COMP`
* `Field Enumerations for US_COMP`
* `Trading Hours for US_COMP`
* `Recent Holidays for US_COMP`



Includes the following coverage:

#### US_COMP -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| ADR                |            401 | 3.04%        |
| Corporate Bond     |             56 | 0.42%        |
| ETF                |           5523 | 41.84%       |
| ETN                |             44 | 0.33%        |
| ETV                |             89 | 0.67%        |
| Equity             |           5267 | 39.9%        |
| Fund               |            337 | 2.55%        |
| Preferred Stock    |            439 | 3.33%        |
| Right              |            121 | 0.92%        |
| Structured Product |            159 | 1.2%         |
| Unit               |            312 | 2.36%        |
| Unknown            |             12 | 0.09%        |
| Warrant            |            441 | 3.34%        |
| Total              |          13201 | 100%         |


Consists of 6 Databases

* `US_COMP`  - Tick Data
* `US_COMP_BARS`  - 1 Minute Bars
* `US_COMP_DAILY`  - End of Day Metrics
* `US_COMP_LATEST`  - Real Time Latest Values
* `US_COMP_MKT_SHARE`  - Market Share End of Day Metrics
* `US_COMP_TCA`  - Enriched Trades for TCA




## US_COMP

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* NBBO - National Best Bid / Offer quotes
* NBBO_COMP - Best National Best Bid / Offer quotes from Even and Odd Lots
* QTE - Best bid / offer quotes
* QTE_COMP - Best Bid & Offer Quotes from Even and Odd Lots
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## US_COMP_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## US_COMP_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* EVENT - Events such as Earnings, and Company Conference Calls
* STAT - Static data, e.g. ISIN, description, security type





## US_COMP_LATEST

Database includes the following tick types:

* SNAP - Latest Trade & Quote / NBBO Prices for all Instruments in the venue
* SNAP_NBBO - Latest NBBO for all Instruments in the venue
* SNAP_TRD - Latest Trade Prices for all Traded Instruments in the venue





## US_COMP_MKT_SHARE

Database includes the following tick types:

* QTE_NBBO_DAY - Daily Quote Metrics by Venue related to the NBBO
* TRD_NBBO_DAY - Daily Trade Metrics by Venue related to the NBBO





## US_COMP_TCA

Database includes the following tick types:

* TRD_TCA - Trades enriched with pravailing quotes / nbbo and offsets


