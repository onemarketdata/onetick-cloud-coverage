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
| ADR                |            404 | 3.11%        |
| Corporate Bond     |             57 | 0.44%        |
| ETF                |           5338 | 41.1%        |
| ETN                |             51 | 0.39%        |
| ETV                |             87 | 0.67%        |
| Equity             |           5251 | 40.43%       |
| Fund               |            339 | 2.61%        |
| Preferred Stock    |            438 | 3.37%        |
| Right              |            113 | 0.87%        |
| Structured Product |            158 | 1.22%        |
| Unit               |            299 | 2.3%         |
| Unknown            |             12 | 0.09%        |
| Warrant            |            442 | 3.4%         |
| Total              |          12989 | 100%         |


Consists of 5 Databases

* `US_COMP`  - Tick Data
* `US_COMP_BARS`  - 1 Minute Bars
* `US_COMP_DAILY`  - End of Day Metrics
* `US_COMP_LATEST`  - Real Time Latest Values
* `US_COMP_MKT_SHARE`  - Market Share End of Day Metrics




## US_COMP

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* NBBO - National Best Bid / Offer quotes
* QTE - Best bid / offer quotes
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

* TRD - Trades
* QTE - Best bid / offer quotes





## US_COMP_MKT_SHARE

Database includes the following tick types:

* QTE_NBBO_DAY - Daily Quote Metrics by Venue related to the NBBO
* TRD_NBBO_DAY - Daily Trade Metrics by Venue related to the NBBO


