# NYSE American Equities

The AMEX (American Stock Exchange) is a prominent US stock and options exchange based in New York City, which is now officially known as the NYSE American. Acquired by the NYSE’s parent company, it functions as an electronic exchange primarily focused on listing and trading small-cap stocks and ETFs (Exchange Traded Funds)

* Country: USA United States [US]
* Mkt Hours: 09:30-16:00
* Time Zone: America/New_York
* Start Date: 20250501
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for AMEX`
* `Field Enumerations for AMEX`
* `Trading Hours for AMEX`
* `Recent Holidays for AMEX`



Includes the following coverage:

#### AMEX -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| ADR                |            404 | 3.1%         |
| Corporate Bond     |             57 | 0.44%        |
| ETF                |           5372 | 41.23%       |
| ETN                |             51 | 0.39%        |
| ETV                |             87 | 0.67%        |
| Equity             |           5216 | 40.03%       |
| Fund               |            339 | 2.6%         |
| Preferred Stock    |            437 | 3.35%        |
| Right              |            114 | 0.87%        |
| Structured Product |            158 | 1.21%        |
| Test               |             51 | 0.39%        |
| Unit               |            301 | 2.31%        |
| Warrant            |            443 | 3.4%         |
| Total              |          13030 | 100%         |


Consists of 2 Databases

* `AMEX`  - Tick Data
* `AMEX_DAILY`  - End of Day Metrics




## AMEX

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## AMEX_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


