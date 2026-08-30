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
| ADR                |            401 | 3.04%        |
| Corporate Bond     |             56 | 0.42%        |
| ETF                |           5528 | 41.9%        |
| ETN                |             44 | 0.33%        |
| ETV                |             90 | 0.68%        |
| Equity             |           5229 | 39.63%       |
| Fund               |            337 | 2.55%        |
| Preferred Stock    |            435 | 3.3%         |
| Right              |            120 | 0.91%        |
| Structured Product |            159 | 1.21%        |
| Test               |             21 | 0.16%        |
| Unit               |            312 | 2.36%        |
| Unknown            |             24 | 0.18%        |
| Warrant            |            437 | 3.31%        |
| Total              |          13193 | 100%         |


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


