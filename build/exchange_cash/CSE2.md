# CSE2 Exchange

CSE2 is the Canadian Securities Exchange’s alternative trading system, offering an unprotected market for trading securities listed on the CSE and other Canadian marketplaces.

* Country: Canada [CA]
* Mkt Hours: 09:00-16:00
* Time Zone: America/Toronto
* Start Date: 20221117
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for CSE2`
* `Field Enumerations for CSE2`
* `Trading Hours for CSE2`
* `Recent Holidays for CSE2`



Includes the following coverage:

#### CSE2 -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Debenture          |             65 | 1.08%        |
| Depositary Receipt |            205 | 3.42%        |
| ETF                |           2057 | 34.28%       |
| ETN                |              1 | 0.02%        |
| Equity             |           3288 | 54.8%        |
| Preferred Stock    |            290 | 4.83%        |
| Right              |              4 | 0.07%        |
| Test               |             11 | 0.18%        |
| Unknown            |              3 | 0.05%        |
| Warrant            |             76 | 1.27%        |
| Total              |           6000 | 100%         |


Consists of 2 Databases

* `CSE2`  - Tick Data
* `CSE2_DAILY`  - End of Day Metrics




## CSE2

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## CSE2_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


