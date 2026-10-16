# Nasdaq PSX

Nasdaq PSX (Philadelphia Stock Exchange) is one of Nasdaq’s three U.S. equities exchanges. It utilizes a price/time priority model and features a Qualified Market Maker (QMM) Program that rewards market makers who actively quote at the National Best Bid or Offer (NBBO).  Full L1 history for Nasdaq PSX from the Consolidated Tape is available in the US_COMP dataset.

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
| ADR                |            404 | 3.04%        |
| Corporate Bond     |             58 | 0.44%        |
| ETF                |           5638 | 42.39%       |
| ETN                |             45 | 0.34%        |
| ETV                |             91 | 0.68%        |
| Equity             |           5223 | 39.27%       |
| Fund               |            337 | 2.53%        |
| Preferred Stock    |            429 | 3.23%        |
| Right              |            123 | 0.92%        |
| Structured Product |            155 | 1.17%        |
| Test               |             27 | 0.2%         |
| Unit               |            312 | 2.35%        |
| Unknown            |             23 | 0.17%        |
| Warrant            |            434 | 3.26%        |
| Total              |          13299 | 100%         |


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


