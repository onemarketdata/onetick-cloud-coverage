# TSX Alpha

Trades, Quotes and Book depth from TSX Alpha Exchange, a Canadian marketplace operated by TMX Group that trades TSX- and TSX Venture-listed securities, with history from May 2017. Alpha launched in 2015 with a randomised order-processing delay (speed bump), later replaced by a static delay, which makes its order book behave differently from other Canadian venues. For TMX’s newer Alpha-X and Alpha DRK books see ALPHA_X. Covered stocks include constituents of the S&P/TSX 60.  A consolidated tape for all Canadian equity markets is provided in the CA_COMP dataset.

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

* `Table Schemas for ALPHA`
* `Field Enumerations for ALPHA`
* `Trading Hours for ALPHA`
* `Recent Holidays for ALPHA`



Includes the following coverage:

#### ALPHA -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Depositary Receipt |            143 | 2.95%        |
| ETF                |           1869 | 38.56%       |
| Equity             |           2400 | 49.52%       |
| Fund               |             29 | 0.6%         |
| Preferred Stock    |            284 | 5.86%        |
| REIT               |             40 | 0.83%        |
| Right              |              5 | 0.1%         |
| Test               |             20 | 0.41%        |
| Warrant            |             57 | 1.18%        |
| Total              |           4847 | 100%         |


Consists of 2 Databases

* `ALPHA`  - Tick Data
* `ALPHA_DAILY`  - End of Day Metrics




## ALPHA

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## ALPHA_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


