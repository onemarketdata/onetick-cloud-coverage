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
| ADR                |            401 | 3.03%        |
| Corporate Bond     |             56 | 0.42%        |
| ETF                |           5548 | 41.89%       |
| ETN                |             45 | 0.34%        |
| ETV                |             90 | 0.68%        |
| Equity             |           5230 | 39.49%       |
| Fund               |            337 | 2.54%        |
| Preferred Stock    |            435 | 3.28%        |
| Right              |            125 | 0.94%        |
| Structured Product |            160 | 1.21%        |
| Test               |             53 | 0.4%         |
| Unit               |            313 | 2.36%        |
| Unknown            |             10 | 0.08%        |
| Warrant            |            440 | 3.32%        |
| Total              |          13243 | 100%         |


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


