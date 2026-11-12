# CSE - TSX/Venture Listed (formerly Pure Trading)

Trades, Quotes and Book depth from the Canadian Securities Exchange’s PURE order book (formerly Pure Trading), with history from May 2017. Unlike the CSE database, PURE covers trading in securities listed on the TSX and TSX Venture rather than CSE listings. Use it with CSE and CSE2 to cover all of the Canadian Securities Exchange’s books.

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

* `Table Schemas for PURE`
* `Field Enumerations for PURE`
* `Trading Hours for PURE`
* `Recent Holidays for PURE`



Includes the following coverage:

#### PURE -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Debenture          |             63 | 1.18%        |
| Depositary Receipt |            216 | 4.06%        |
| ETF                |           2121 | 39.87%       |
| Equity             |           2555 | 48.03%       |
| Preferred Stock    |            285 | 5.36%        |
| Right              |              5 | 0.09%        |
| Test               |             11 | 0.21%        |
| Unknown            |              3 | 0.06%        |
| Warrant            |             61 | 1.15%        |
| Total              |           5320 | 100%         |


Consists of 2 Databases

* `PURE`  - Tick Data
* `PURE_DAILY`  - End of Day Metrics




## PURE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## PURE_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


