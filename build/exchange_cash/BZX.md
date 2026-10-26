# Cboe BZX Equities

Cboe BZX is one of Cboe Global Markets’ four U.S. equities exchanges, operating as a distinct electronic order book for trading NMS securities with its own unique fee schedule and market model. BYX is primarily known for its distinct inverted maker-taker pricing model, which charges a fee for providing liquidity and offers a rebate for removing it, incentivizing aggressive order flow.  Full L1 history for Cboe BZX (BATS) from the Consolidated Tape is available in the US_COMP dataset.

* Country: USA United States [US]
* Mkt Hours: 09:30-16:00
* Time Zone: America/New_York
* Start Date: 20250501
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for BZX`
* `Field Enumerations for BZX`
* `Trading Hours for BZX`
* `Recent Holidays for BZX`



Includes the following coverage:

#### BZX -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| ADR                |            403 | 3.03%        |
| Corporate Bond     |             57 | 0.43%        |
| ETF                |           5648 | 42.49%       |
| ETN                |             45 | 0.34%        |
| ETV                |             90 | 0.68%        |
| Equity             |           5231 | 39.35%       |
| Fund               |            335 | 2.52%        |
| Preferred Stock    |            429 | 3.23%        |
| Right              |            121 | 0.91%        |
| Structured Product |            155 | 1.17%        |
| Test               |             25 | 0.19%        |
| Unit               |            310 | 2.33%        |
| Unknown            |             13 | 0.1%         |
| Warrant            |            431 | 3.24%        |
| Total              |          13293 | 100%         |


Consists of 2 Databases

* `BZX`  - Tick Data
* `BZX_DAILY`  - End of Day Metrics




## BZX

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## BZX_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


