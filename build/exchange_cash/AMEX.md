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
| ADR                |            401 | 3.03%        |
| Corporate Bond     |             56 | 0.42%        |
| ETF                |           5538 | 41.89%       |
| ETN                |             45 | 0.34%        |
| ETV                |             90 | 0.68%        |
| Equity             |           5233 | 39.58%       |
| Fund               |            337 | 2.55%        |
| Preferred Stock    |            435 | 3.29%        |
| Right              |            120 | 0.91%        |
| Structured Product |            160 | 1.21%        |
| Test               |             51 | 0.39%        |
| Unit               |            314 | 2.38%        |
| Warrant            |            440 | 3.33%        |
| Total              |          13220 | 100%         |


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


