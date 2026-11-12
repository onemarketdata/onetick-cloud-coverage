# US Consolidated Equities (exc. OTC) Sample

A sample of the US_COMP consolidated tape database covering a 500 symbol subset from the US SIP (CTA and UTP), consolidated across all US equity exchanges and FINRA trade reporting facilities, between January 2, 2024 and March 31, 2024. It includes trades, quotes, NBBO and bars for NMS stocks and ETFs, excluding OTC securities.  The full subscribed dataset has history from 1993.

* Country: USA United States [US]
* Mkt Hours: 09:30-16:00
* Time Zone: America/New_York
* Start Date: 20240102
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: SIP Consolidation Time
* Key Indices: S&P 500 Index [TDI_IDX::SP], Dow Jones Industrial Average Index [TDI_IDX::DJ], NASDAQ 100 Index [TDI_IDX::ND], NASDAQ Composite Index [TDI_IDX::NC]



Details are provided below

* `Table Schemas for US_COMP_SAMPLE`
* `Field Enumerations for US_COMP_SAMPLE`
* `Trading Hours for US_COMP_SAMPLE`
* `Recent Holidays for US_COMP_SAMPLE`



Includes the following coverage:

#### US_COMP_SAMPLE -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| ETF             |              1 | 0.2%         |
| Equity          |            501 | 99.8%        |
| Total           |            502 | 100%         |


Consists of 3 Databases

* `US_COMP_SAMPLE`  - Tick Data
* `US_COMP_SAMPLE_BARS`  - 1 Minute Bars
* `US_COMP_SAMPLE_DAILY`  - End of Day Metrics




## US_COMP_SAMPLE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* NBBO - National Best Bid / Offer quotes
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## US_COMP_SAMPLE_BARS

Database includes the following tick types:

* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## US_COMP_SAMPLE_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


