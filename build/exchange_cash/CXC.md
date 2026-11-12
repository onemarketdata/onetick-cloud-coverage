# Nasdaq CXC

Trades, Quotes and Book depth from Nasdaq CXC (formerly Chi-X Canada), Nasdaq Canada’s main lit order book, with history from May 2017. It trades TSX- and TSX Venture-listed securities and is one of the largest alternative venues in Canada. Covered stocks include constituents of the S&P/TSX 60.   A consolidated tape for all Canadian equity markets is provided in the CA_COMP dataset.

* Country: Canada [CA]
* Mkt Hours: 09:00-16:00
* Time Zone: America/Toronto
* Start Date: 20170529
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes
* Timestamp Type: Arrival
* Key Indices: S&P/TSX Composite Index [TDI_IDX::TS], S&P/TSX 60 [TSX_IDX::TX60]



Details are provided below

* `Table Schemas for CXC`
* `Field Enumerations for CXC`
* `Trading Hours for CXC`
* `Recent Holidays for CXC`



Includes the following coverage:

#### CXC -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Debenture          |             64 | 1.05%        |
| Depositary Receipt |            216 | 3.53%        |
| ETF                |           2139 | 34.96%       |
| Equity             |           3292 | 53.8%        |
| Preferred Stock    |            286 | 4.67%        |
| Right              |              5 | 0.08%        |
| Test               |             40 | 0.65%        |
| Unknown            |              3 | 0.05%        |
| Warrant            |             74 | 1.21%        |
| Total              |           6119 | 100%         |


Consists of 2 Databases

* `CXC`  - Tick Data
* `CXC_DAILY`  - End of Day Metrics




## CXC

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## CXC_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


