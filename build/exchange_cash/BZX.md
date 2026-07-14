# Cboe BZX Equities

Cboe BZX is one of Cboe Global Markets’ four U.S. equities exchanges, operating as a distinct electronic order book for trading NMS securities with its own unique fee schedule and market model. BYX is primarily known for its distinct inverted maker-taker pricing model, which charges a fee for providing liquidity and offers a rebate for removing it, incentivizing aggressive order flow.

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
| ADR                |            404 | 3.11%        |
| Corporate Bond     |             57 | 0.44%        |
| ETF                |           5361 | 41.22%       |
| ETN                |             51 | 0.39%        |
| ETV                |             87 | 0.67%        |
| Equity             |           5216 | 40.11%       |
| Fund               |            339 | 2.61%        |
| Preferred Stock    |            437 | 3.36%        |
| Right              |            114 | 0.88%        |
| Structured Product |            158 | 1.21%        |
| Test               |             21 | 0.16%        |
| Unit               |            299 | 2.3%         |
| Unknown            |             18 | 0.14%        |
| Warrant            |            443 | 3.41%        |
| Total              |          13005 | 100%         |


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


