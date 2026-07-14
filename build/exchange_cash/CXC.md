# Nasdaq CXC

Nasdaq CXC is Nasdaq’s dark pool ATS that allows participants to execute orders anonymously at or better than the NBBO without displaying quotes.

* Country: Canada [CA]
* Mkt Hours: 09:00-16:00
* Time Zone: America/Toronto
* Start Date: 20170529
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for CXC`
* `Field Enumerations for CXC`
* `Trading Hours for CXC`
* `Recent Holidays for CXC`



Includes the following coverage:

#### CXC -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Debenture          |             65 | 1.07%        |
| Depositary Receipt |            205 | 3.39%        |
| ETF                |           2071 | 34.21%       |
| Equity             |           3300 | 54.51%       |
| Preferred Stock    |            289 | 4.77%        |
| Right              |              5 | 0.08%        |
| Test               |             35 | 0.58%        |
| Unknown            |              3 | 0.05%        |
| Warrant            |             81 | 1.34%        |
| Total              |           6054 | 100%         |


Consists of 2 Databases

* `CXC`  - Tick Data
* `CXC_DAILY`  - End of Day Metrics




## CXC

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## CXC_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


