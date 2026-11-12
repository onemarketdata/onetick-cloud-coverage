# TSX Alpha-X / Alpha DRK

Trades, Quotes and Book depth from two TMX order books launched in November 2023: Alpha-X, a lit book with the same order types as TSX Alpha plus the Smart Limit order type, and Alpha DRK, a fully dark book with pegged (primary, market, minimum price improvement and midpoint) orders and the Smart Peg order type. Use it to compare lit and dark liquidity in TSX- and TSX Venture-listed securities.   A consolidated tape for all Canadian equity markets is provided in the CA_COMP dataset.

* Country: Canada [CA]
* Mkt Hours: 09:00-16:00
* Time Zone: America/Toronto
* Start Date: 20231106
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes
* Timestamp Type: Arrival
* Key Indices: S&P/TSX Composite Index [TDI_IDX::TS], S&P/TSX 60 [TSX_IDX::TX60]



Details are provided below

* `Table Schemas for ALPHA_X`
* `Field Enumerations for ALPHA_X`
* `Trading Hours for ALPHA_X`
* `Recent Holidays for ALPHA_X`



Includes the following coverage:

#### ALPHA_X -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Depositary Receipt |            143 | 2.97%        |
| ETF                |           1869 | 38.81%       |
| Equity             |           2369 | 49.19%       |
| Fund               |             29 | 0.6%         |
| Preferred Stock    |            284 | 5.9%         |
| REIT               |             39 | 0.81%        |
| Right              |              5 | 0.1%         |
| Test               |             22 | 0.46%        |
| Warrant            |             56 | 1.16%        |
| Total              |           4816 | 100%         |


Consists of 2 Databases

* `ALPHA_X`  - Tick Data
* `ALPHA_X_DAILY`  - End of Day Metrics




## ALPHA_X

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## ALPHA_X_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


