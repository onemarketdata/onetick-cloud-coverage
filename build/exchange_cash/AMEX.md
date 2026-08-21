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
| ADR                |            401 | 3.04%        |
| Corporate Bond     |             56 | 0.42%        |
| ETF                |           5515 | 41.78%       |
| ETN                |             44 | 0.33%        |
| ETV                |             89 | 0.67%        |
| Equity             |           5235 | 39.66%       |
| Fund               |            337 | 2.55%        |
| Preferred Stock    |            438 | 3.32%        |
| Right              |            121 | 0.92%        |
| Structured Product |            159 | 1.2%         |
| Test               |             51 | 0.39%        |
| Unit               |            312 | 2.36%        |
| Warrant            |            441 | 3.34%        |
| Total              |          13199 | 100%         |


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


