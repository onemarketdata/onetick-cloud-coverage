# Taiwan Consolidated Equities

Consolidated data from all Taiwan equities exchanges.

* Country: Taiwan [TW]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Taipei
* Start Date: 20160602
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for TW_COMP`
* `Field Enumerations for TW_COMP`
* `Trading Hours for TW_COMP`
* `Recent Holidays for TW_COMP`



Includes the following coverage:

#### TW_COMP -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Depository Receipt |              6 | 0.22%        |
| ETF                |            339 | 12.3%        |
| ETN                |             23 | 0.83%        |
| Equity             |           2337 | 84.83%       |
| Investment Fund    |              3 | 0.11%        |
| Preferred Stock    |             29 | 1.05%        |
| REIT               |              6 | 0.22%        |
| Unknown            |             12 | 0.44%        |
| Total              |           2755 | 100%         |


Consists of 3 Databases

* `TW_COMP`  - Tick Data
* `TW_COMP_BARS`  - 1 Minute Bars
* `TW_COMP_DAILY`  - End of Day Metrics




## TW_COMP

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* QTE - Best bid / offer quotes
* QTE_ODD_LOT - BBO quotes from the Odd Lot book, for exchanges that have a separate order book for odd lots
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





