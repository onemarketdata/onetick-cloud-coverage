# Lynx ATS

Trades, Quotes and Book depth from Lynx ATS, a Canadian alternative trading system operated by Tradelogiq Markets Inc. alongside Omega ATS, which trades TSX- and TSX Venture-listed securities, with history from May 2017. Combined with the other Canadian venue databases, or CA_COMP for consolidated data, it shows how liquidity in Canadian stocks such as S&P/TSX 60 constituents is split across marketplaces.   A consolidated tape for all Canadian equity markets is provided in the CA_COMP dataset.

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

* `Table Schemas for LYNX`
* `Field Enumerations for LYNX`
* `Trading Hours for LYNX`
* `Recent Holidays for LYNX`



Includes the following coverage:

#### LYNX -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Debenture          |             61 | 1.01%        |
| Depositary Receipt |            216 | 3.57%        |
| ETF                |           2139 | 35.37%       |
| Equity             |           3272 | 54.1%        |
| Preferred Stock    |            286 | 4.73%        |
| Right              |              3 | 0.05%        |
| Unknown            |              4 | 0.07%        |
| Warrant            |             67 | 1.11%        |
| Total              |           6048 | 100%         |


Consists of 2 Databases

* `LYNX`  - Tick Data
* `LYNX_DAILY`  - End of Day Metrics




## LYNX

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## LYNX_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


