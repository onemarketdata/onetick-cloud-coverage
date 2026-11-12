# Cboe Canada (formerly Neo Exchange)

Trades, Quotes and Book depth from Cboe Canada (formerly Neo Exchange), with history from October 2017, covering its lit book, its dark book and its speed-bumped book for natural investors, plus Cboe Canada-listed securities. NEO was acquired by Cboe Global Markets in 2022 and renamed Cboe Canada. Cboe Canada is also a listing venue, especially for ETFs and Canadian Depositary Receipts (CDRs) of large US companies.   A consolidated tape for all Canadian equity markets is provided in the CA_COMP dataset.

* Country: Canada [CA]
* Mkt Hours: 09:00-16:00
* Time Zone: America/Toronto
* Start Date: 20171023
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes
* Timestamp Type: Arrival
* Key Indices: S&P/TSX Composite Index [TDI_IDX::TS], S&P/TSX 60 [TSX_IDX::TX60]



Details are provided below

* `Table Schemas for NEO`
* `Field Enumerations for NEO`
* `Trading Hours for NEO`
* `Recent Holidays for NEO`



Includes the following coverage:

#### NEO -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Debenture          |             65 | 1.01%        |
| Depositary Receipt |            216 | 3.35%        |
| ETF                |           2151 | 33.32%       |
| ETN                |              1 | 0.02%        |
| Equity             |           3365 | 52.12%       |
| Fund               |            196 | 3.04%        |
| Preferred Stock    |            290 | 4.49%        |
| REIT               |             40 | 0.62%        |
| Right              |              6 | 0.09%        |
| Test               |             48 | 0.74%        |
| Unknown            |              4 | 0.06%        |
| Warrant            |             74 | 1.15%        |
| Total              |           6456 | 100%         |


Consists of 2 Databases

* `NEO`  - Tick Data
* `NEO_DAILY`  - End of Day Metrics




## NEO

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_NEO_L - (Cboe Canada only) Full orderbook data for the Neo-L book
* PRL_NEO_N - (Cboe Canada only) Aggregated market depth for the Neo-N book
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## NEO_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


