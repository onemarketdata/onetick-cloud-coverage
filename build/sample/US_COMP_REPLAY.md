# US Consolidated Equity Replay for Intraday / CEP

A real-time replay of consolidated US equity trades and quotes from the SIP, published as if live so you can test intraday queries and complex event processing (CEP) / streaming subscriptions without a live feed. Data covers all US equity exchanges and FINRA trade reporting facilities and appears for the current day.

* Country: USA United States [US]
* Mkt Hours: 09:30-16:00
* Time Zone: America/New_York
* Start Date: TODAY
* Real Time Available: Yes
* Bars Available: No
* Book Depth Available: No
* Timestamp Type: SIP Consolidation Time
* Key Indices: S&P 500 Index [TDI_IDX::SP], Dow Jones Industrial Average Index [TDI_IDX::DJ], NASDAQ 100 Index [TDI_IDX::ND], NASDAQ Composite Index [TDI_IDX::NC]



Details are provided below

* `Table Schemas for US_COMP_REPLAY`
* `Field Enumerations for US_COMP_REPLAY`
* `Trading Hours for US_COMP_REPLAY`
* `Recent Holidays for US_COMP_REPLAY`



Includes the following coverage:

#### US_COMP_REPLAY -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Total           |            502 | 100%         |


Consists of 1 Databases

* `US_COMP_REPLAY`  - Tick Data




## US_COMP_REPLAY

Database includes the following tick types:

* MKT - Market phase / instrument status information
* NBBO - National Best Bid / Offer quotes
* QTE - Best bid / offer quotes
* TRD - Trades


