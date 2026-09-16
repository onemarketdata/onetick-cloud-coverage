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
| ADR                |            401 | 3.04%        |
| Corporate Bond     |             56 | 0.42%        |
| ETF                |           5534 | 41.91%       |
| ETN                |             45 | 0.34%        |
| ETV                |             90 | 0.68%        |
| Equity             |           5226 | 39.58%       |
| Fund               |            337 | 2.55%        |
| Preferred Stock    |            435 | 3.29%        |
| Right              |            124 | 0.94%        |
| Structured Product |            160 | 1.21%        |
| Test               |             21 | 0.16%        |
| Unit               |            314 | 2.38%        |
| Unknown            |             22 | 0.17%        |
| Warrant            |            439 | 3.32%        |
| Total              |          13204 | 100%         |


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


