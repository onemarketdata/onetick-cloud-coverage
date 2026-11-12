# US Consolidated Equities (exc. OTC)

Consolidated trades, NBBO and exchange quotes, plus bars for US stocks and ETFs from the US SIPs (CTA and UTP), covering all US equity exchanges, including newer venues such as 24X National Exchange and the Texas Stock Exchange, plus FINRA trade reporting facilities. History is available from January 1993 and data is also available in real time. OTC-traded securities are excluded, and are found in the US_OTC dataset.

* Country: USA United States [US]
* Mkt Hours: 09:30-16:00
* Time Zone: America/New_York
* Start Date: 19930104
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: SIP Consolidation Time
* Key Indices: S&P 500 Index [TDI_IDX::SP], NASDAQ 100 Index [TDI_IDX::ND], NASDAQ Composite Index [TDI_IDX::NC]



Details are provided below

* `Table Schemas for US_COMP`
* `Field Enumerations for US_COMP`
* `Trading Hours for US_COMP`
* `Recent Holidays for US_COMP`



Includes the following coverage:

#### US_COMP -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| ADR                |            403 | 3.03%        |
| Corporate Bond     |             57 | 0.43%        |
| ETF                |           5662 | 42.51%       |
| ETN                |             45 | 0.34%        |
| ETV                |             90 | 0.68%        |
| Equity             |           5267 | 39.54%       |
| Fund               |            335 | 2.52%        |
| Preferred Stock    |            430 | 3.23%        |
| Right              |            121 | 0.91%        |
| Structured Product |            155 | 1.16%        |
| Unit               |            310 | 2.33%        |
| Unknown            |             13 | 0.1%         |
| Warrant            |            432 | 3.24%        |
| Total              |          13320 | 100%         |


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
* LAT_1M - 1-minute Latency bars for real time delivered data
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


