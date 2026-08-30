# Nasdaq PSX

Nasdaq PSX (Philadelphia Stock Exchange) is one of Nasdaq’s three U.S. equities exchanges. It utilizes a price/time priority model and features a Qualified Market Maker (QMM) Program that rewards market makers who actively quote at the National Best Bid or Offer (NBBO)

* Country: USA United States [US]
* Mkt Hours: 09:30-16:00
* Time Zone: America/New_York
* Start Date: 20250501
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for NASDAQ_PSX`
* `Field Enumerations for NASDAQ_PSX`
* `Trading Hours for NASDAQ_PSX`
* `Recent Holidays for NASDAQ_PSX`



Includes the following coverage:

#### NASDAQ_PSX -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| ADR                |            401 | 3.04%        |
| Corporate Bond     |             56 | 0.42%        |
| ETF                |           5528 | 41.86%       |
| ETN                |             44 | 0.33%        |
| ETV                |             90 | 0.68%        |
| Equity             |           5228 | 39.59%       |
| Fund               |            337 | 2.55%        |
| Preferred Stock    |            435 | 3.29%        |
| Right              |            120 | 0.91%        |
| Structured Product |            159 | 1.2%         |
| Test               |             23 | 0.17%        |
| Unit               |            312 | 2.36%        |
| Unknown            |             36 | 0.27%        |
| Warrant            |            437 | 3.31%        |
| Total              |          13206 | 100%         |


Consists of 2 Databases

* `NASDAQ_PSX`  - Tick Data
* `NASDAQ_PSX_DAILY`  - End of Day Metrics




## NASDAQ_PSX

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* MM_STATUS - Information on the market makers registered in each security
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* TRD - Trades





## NASDAQ_PSX_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


