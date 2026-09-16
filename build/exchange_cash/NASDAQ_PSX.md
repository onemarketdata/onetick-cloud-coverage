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
| ADR                |            401 | 3.03%        |
| Corporate Bond     |             56 | 0.42%        |
| ETF                |           5534 | 41.87%       |
| ETN                |             45 | 0.34%        |
| ETV                |             90 | 0.68%        |
| Equity             |           5225 | 39.53%       |
| Fund               |            337 | 2.55%        |
| Preferred Stock    |            435 | 3.29%        |
| Right              |            124 | 0.94%        |
| Structured Product |            160 | 1.21%        |
| Test               |             23 | 0.17%        |
| Unit               |            313 | 2.37%        |
| Unknown            |             36 | 0.27%        |
| Warrant            |            439 | 3.32%        |
| Total              |          13218 | 100%         |


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


