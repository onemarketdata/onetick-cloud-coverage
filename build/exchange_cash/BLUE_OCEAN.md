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
| ADR                |            404 | 3.03%        |
| Corporate Bond     |             58 | 0.44%        |
| ETF                |           5638 | 42.33%       |
| ETN                |             45 | 0.34%        |
| ETV                |             91 | 0.68%        |
| Equity             |           5224 | 39.23%       |
| Fund               |            337 | 2.53%        |
| Preferred Stock    |            429 | 3.22%        |
| Right              |            123 | 0.92%        |
| Structured Product |            155 | 1.16%        |
| Test               |             57 | 0.43%        |
| Unit               |            312 | 2.34%        |
| Unknown            |             11 | 0.08%        |
| Warrant            |            434 | 3.26%        |
| Total              |          13318 | 100%         |


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


