# Blue Ocean ATS

Blue Ocean ATS (BOATS) is a US-based Alternative Trading System (ATS) run by Blue Ocean Technologies, enabling trading of U.S. stocks (NMS) during non-traditional hours, specifically 8 PM to 4 AM ET, Sunday to Thursday, bridging the overnight gap

* Country: USA United States [US]
* Mkt Hours: 20:00-04:00
* Time Zone: America/New_York
* Start Date: 20251211
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for BLUE_OCEAN`
* `Field Enumerations for BLUE_OCEAN`
* `Trading Hours for BLUE_OCEAN`
* `Recent Holidays for BLUE_OCEAN`



Includes the following coverage:

#### BLUE_OCEAN -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| ADR                |            403 | 3.11%        |
| Corporate Bond     |             57 | 0.44%        |
| ETF                |           5321 | 41.0%        |
| ETN                |             51 | 0.39%        |
| ETV                |             87 | 0.67%        |
| Equity             |           5213 | 40.17%       |
| Fund               |            339 | 2.61%        |
| Preferred Stock    |            437 | 3.37%        |
| Right              |            112 | 0.86%        |
| Structured Product |            158 | 1.22%        |
| Test               |             53 | 0.41%        |
| Unit               |            297 | 2.29%        |
| Unknown            |             10 | 0.08%        |
| Warrant            |            440 | 3.39%        |
| Total              |          12978 | 100%         |


Consists of 2 Databases

* `BLUE_OCEAN`  - Tick Data
* `BLUE_OCEAN_DAILY`  - End of Day Metrics




## BLUE_OCEAN

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## BLUE_OCEAN_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


