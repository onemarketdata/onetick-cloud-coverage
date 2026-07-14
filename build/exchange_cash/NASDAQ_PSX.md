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
| ADR                |            404 | 3.1%         |
| Corporate Bond     |             57 | 0.44%        |
| ETF                |           5361 | 41.19%       |
| ETN                |             51 | 0.39%        |
| ETV                |             87 | 0.67%        |
| Equity             |           5214 | 40.06%       |
| Fund               |            339 | 2.6%         |
| Preferred Stock    |            437 | 3.36%        |
| Right              |            114 | 0.88%        |
| Structured Product |            158 | 1.21%        |
| Test               |             23 | 0.18%        |
| Unit               |            299 | 2.3%         |
| Unknown            |             28 | 0.22%        |
| Warrant            |            443 | 3.4%         |
| Total              |          13015 | 100%         |


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


