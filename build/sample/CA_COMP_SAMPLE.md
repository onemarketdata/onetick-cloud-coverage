# Canadian Consolidated Market Sample

A sample of the CA_COMP consolidated tape database covering a subset of symbols across all Canadian equity marketplaces, including TSX, TSX Venture, Cboe Canada, CSE, TSX Alpha, Nasdaq CXC/CX2 and Canadian ATSs, between January 2, 2024 and March 31, 2024. It includes consolidated trades, quotes, NBBO and bars for evaluating how liquidity in Canadian stocks is split across venues. The full database covers constituents of the S&P/TSX Composite and S&P/TSX 60.

* Country: Canada [CA]
* Mkt Hours: 09:00-16:00
* Time Zone: America/Toronto
* Start Date: 20240102
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: S&P/TSX Composite Index [TDI_IDX::TS]



Details are provided below

* `Table Schemas for CA_COMP_SAMPLE`
* `Field Enumerations for CA_COMP_SAMPLE`
* `Trading Hours for CA_COMP_SAMPLE`
* `Recent Holidays for CA_COMP_SAMPLE`



Includes the following coverage:

#### CA_COMP_SAMPLE -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Debenture          |            105 | 1.91%        |
| Depositary Receipt |             47 | 0.86%        |
| ETF                |           1369 | 24.91%       |
| ETN                |              3 | 0.05%        |
| Equity             |           3380 | 61.51%       |
| Investment Fund    |             43 | 0.78%        |
| Preferred Stock    |            347 | 6.31%        |
| REIT               |             48 | 0.87%        |
| Right              |              3 | 0.05%        |
| Test               |             43 | 0.78%        |
| Warrant            |            107 | 1.95%        |
| Total              |           5495 | 100%         |


Consists of 3 Databases

* `CA_COMP_SAMPLE`  - Tick Data
* `CA_COMP_SAMPLE_BARS`  - 1 Minute Bars
* `CA_COMP_SAMPLE_DAILY`  - End of Day Metrics




## CA_COMP_SAMPLE

Database includes the following tick types:

* NBBO - National Best Bid / Offer quotes
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## CA_COMP_SAMPLE_BARS

Database includes the following tick types:

* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## CA_COMP_SAMPLE_DAILY

Database includes the following tick types:

* STAT - Static data, e.g. ISIN, description, security type


