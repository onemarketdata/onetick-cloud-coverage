# Canadian Securities Exchange

Trades, Quotes and Book depth from the Canadian Securities Exchange (CSE), Canada’s third listing exchange, with history from May 2017. CSE focuses on emerging and small-cap companies, including many junior mining, technology, cannabis and crypto issuers, and this database covers trading in CSE-listed securities. For CSE’s other books see PURE and CSE2.   A consolidated tape for all Canadian equity markets is provided in the CA_COMP dataset.

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

* `Table Schemas for CSE`
* `Field Enumerations for CSE`
* `Trading Hours for CSE`
* `Recent Holidays for CSE`



Includes the following coverage:

#### CSE -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Debenture       |              1 | 0.13%        |
| ETF             |              1 | 0.13%        |
| ETN             |              1 | 0.13%        |
| Equity          |            739 | 98.4%        |
| Preferred Stock |              2 | 0.27%        |
| Unknown         |              1 | 0.13%        |
| Warrant         |              6 | 0.8%         |
| Total           |            751 | 100%         |


Consists of 2 Databases

* `CSE`  - Tick Data
* `CSE_DAILY`  - End of Day Metrics




## CSE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## CSE_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


