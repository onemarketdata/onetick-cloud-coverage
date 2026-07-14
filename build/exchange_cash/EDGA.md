# Cboe EDGA

Cboe EDGA Exchange (EDGA) is a U.S. equities market that transitioned from an inverted to a tier-free, maker-taker pricing structure. It offers unique features like hidden price improvement, retail priority, and periodic auctions to optimize order execution

* Country: USA United States [US]
* Mkt Hours: 09:30-16:00
* Time Zone: America/New_York
* Start Date: 20250501
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for EDGA`
* `Field Enumerations for EDGA`
* `Trading Hours for EDGA`
* `Recent Holidays for EDGA`



Includes the following coverage:

#### EDGA -  Coverage

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

* `EDGA`  - Tick Data
* `EDGA_DAILY`  - End of Day Metrics




## EDGA

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## EDGA_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


