# The Nasdaq

The Nasdaq is an American multinational financial services corporation that operates the world’s second-largest stock exchange by market capitalization.  Full L1 history for NASDAQ from the Consolidated Tape is available in the US_COMP dataset.

* Country: USA United States [US]
* Mkt Hours: 09:30-16:00
* Time Zone: America/New_York
* Start Date: 20250501
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for NASDAQ`
* `Field Enumerations for NASDAQ`
* `Trading Hours for NASDAQ`
* `Recent Holidays for NASDAQ`



Includes the following coverage:

#### NASDAQ -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| ADR                |            404 | 3.04%        |
| Corporate Bond     |             58 | 0.44%        |
| ETF                |           5638 | 42.39%       |
| ETN                |             45 | 0.34%        |
| ETV                |             91 | 0.68%        |
| Equity             |           5224 | 39.28%       |
| Fund               |            337 | 2.53%        |
| Preferred Stock    |            429 | 3.23%        |
| Right              |            123 | 0.92%        |
| Structured Product |            155 | 1.17%        |
| Test               |             27 | 0.2%         |
| Unit               |            312 | 2.35%        |
| Unknown            |             23 | 0.17%        |
| Warrant            |            434 | 3.26%        |
| Total              |          13300 | 100%         |


Consists of 2 Databases

* `NASDAQ`  - Tick Data
* `NASDAQ_DAILY`  - End of Day Metrics




## NASDAQ

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* MM_STATUS - Information on the market makers registered in each security
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* TRD - Trades





## NASDAQ_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


