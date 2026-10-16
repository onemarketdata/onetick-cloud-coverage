# Cboe EDGA

Cboe EDGA Exchange (EDGA) is a U.S. equities market that transitioned from an inverted to a tier-free, maker-taker pricing structure. It offers unique features like hidden price improvement, retail priority, and periodic auctions to optimize order execution.  Full L1 history for Cboe EDGA from the Consolidated Tape is available in the US_COMP dataset.

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
| ADR                |            404 | 3.04%        |
| Corporate Bond     |             58 | 0.44%        |
| ETF                |           5638 | 42.44%       |
| ETN                |             45 | 0.34%        |
| ETV                |             91 | 0.68%        |
| Equity             |           5224 | 39.32%       |
| Fund               |            337 | 2.54%        |
| Preferred Stock    |            429 | 3.23%        |
| Right              |            123 | 0.93%        |
| Structured Product |            155 | 1.17%        |
| Test               |             25 | 0.19%        |
| Unit               |            312 | 2.35%        |
| Unknown            |             10 | 0.08%        |
| Warrant            |            434 | 3.27%        |
| Total              |          13285 | 100%         |


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


