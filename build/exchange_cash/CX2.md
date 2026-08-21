# Nasdaq CX2

Nasdaq CX2 is Nasdaq’s alternative trading system (ATS) for trading NMS stocks using a price-time priority order book model.

* Country: Canada [CA]
* Mkt Hours: 09:00-16:00
* Time Zone: America/Toronto
* Start Date: 20170529
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for CX2`
* `Field Enumerations for CX2`
* `Trading Hours for CX2`
* `Recent Holidays for CX2`



Includes the following coverage:

#### CX2 -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Debenture          |             65 | 1.07%        |
| Depositary Receipt |            205 | 3.37%        |
| ETF                |           2090 | 34.32%       |
| Equity             |           3314 | 54.42%       |
| Preferred Stock    |            288 | 4.73%        |
| Right              |              6 | 0.1%         |
| Test               |             40 | 0.66%        |
| Unknown            |              3 | 0.05%        |
| Warrant            |             79 | 1.3%         |
| Total              |           6090 | 100%         |


Consists of 2 Databases

* `CX2`  - Tick Data
* `CX2_DAILY`  - End of Day Metrics




## CX2

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## CX2_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


