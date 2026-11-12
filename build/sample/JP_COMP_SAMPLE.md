# Japan Consolidated Equities Sample

A sample of the JP_COMP consolidated tape database covering a subset of symbols across all Japanese equity venues, including the Tokyo, Nagoya, Fukuoka and Sapporo exchanges and the Japannext and Cboe Japan PTSs, between January 2, 2024 and March 31, 2024. It includes consolidated trades, quotes and bars for measuring how PTS volume adds to exchange liquidity. The full database covers constituents of the Nikkei 225 and TOPIX.

* Country: Japan [JP]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Tokyo
* Start Date: 20240102
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: Nikkei 225 Index [TDI_IDX::NE]



Details are provided below

* `Table Schemas for JP_COMP_SAMPLE`
* `Field Enumerations for JP_COMP_SAMPLE`
* `Trading Hours for JP_COMP_SAMPLE`
* `Recent Holidays for JP_COMP_SAMPLE`



Includes the following coverage:

#### JP_COMP_SAMPLE -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| ETF             |            350 | 7.85%        |
| Equity          |           4104 | 92.06%       |
| Preferred Stock |              4 | 0.09%        |
| Total           |           4458 | 100%         |


Consists of 3 Databases

* `JP_COMP_SAMPLE`  - Tick Data
* `JP_COMP_SAMPLE_BARS`  - 1 Minute Bars
* `JP_COMP_SAMPLE_DAILY`  - End of Day Metrics




## JP_COMP_SAMPLE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* NBBO - National Best Bid / Offer quotes
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## JP_COMP_SAMPLE_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## JP_COMP_SAMPLE_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


