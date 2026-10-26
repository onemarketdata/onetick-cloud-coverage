# NYSE Arca Equities

NYSE Arca is a fully electronic U.S. securities exchange and a subsidiary of the New York Stock Exchange (NYSE) Group. Originally founded as the Archipelago Exchange (ArcaEx), it merged with the NYSE in 2006. Today, it is the global market leader in trading Exchange-Traded Products (ETPs) like ETFs and ETNs.  Full L1 history for ARCA from the Consolidated Tape is available in the US_COMP dataset.

* Country: USA United States [US]
* Mkt Hours: 09:30-16:00
* Time Zone: America/New_York
* Start Date: 20250501
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for ARCA`
* `Field Enumerations for ARCA`
* `Trading Hours for ARCA`
* `Recent Holidays for ARCA`



Includes the following coverage:

#### ARCA -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| ADR                |            403 | 3.03%        |
| Corporate Bond     |             57 | 0.43%        |
| ETF                |           5652 | 42.43%       |
| ETN                |             45 | 0.34%        |
| ETV                |             90 | 0.68%        |
| Equity             |           5233 | 39.29%       |
| Fund               |            335 | 2.52%        |
| Preferred Stock    |            429 | 3.22%        |
| Right              |            121 | 0.91%        |
| Structured Product |            155 | 1.16%        |
| Test               |             57 | 0.43%        |
| Unit               |            310 | 2.33%        |
| Unknown            |              1 | 0.01%        |
| Warrant            |            432 | 3.24%        |
| Total              |          13320 | 100%         |


Consists of 2 Databases

* `ARCA`  - Tick Data
* `ARCA_DAILY`  - End of Day Metrics




## ARCA

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## ARCA_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


