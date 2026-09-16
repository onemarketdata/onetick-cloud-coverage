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
| Debenture          |             64 | 1.05%        |
| Depositary Receipt |            205 | 3.36%        |
| ETF                |           2101 | 34.43%       |
| Equity             |           3315 | 54.33%       |
| Preferred Stock    |            289 | 4.74%        |
| Right              |              5 | 0.08%        |
| Test               |             40 | 0.66%        |
| Unknown            |              3 | 0.05%        |
| Warrant            |             80 | 1.31%        |
| Total              |           6102 | 100%         |


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


