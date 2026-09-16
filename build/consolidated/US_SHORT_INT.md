# FINRA - US Equities Short Interest / Short Volume

FINRA US Equity short interest summary every two weeks, plus trade reports, and daily short volume through Trade Reporting Facilities.  FINRA Daily Short Sale Volume is stored in the DAY table.  This is populated daily.  Monthly Short Sale Volume is stored in the TRD and SHORT_INT tables, and is populated monthly, approximately 8 days after the month is complete.  The TRD table reports data per day, while the SHORT_INT table reports data twice per month.

* Country: USA United States [US]
* Mkt Hours: 09:30-16:00
* Time Zone: America/New_York
* Start Date: 20190201
* Real Time Available: No
* Bars Available: No
* Book Depth Available: No



Details are provided below

* `Table Schemas for US_SHORT_INT`
* `Field Enumerations for US_SHORT_INT`
* `Trading Hours for US_SHORT_INT`
* `Recent Holidays for US_SHORT_INT`



Includes the following coverage:

#### US_SHORT_INT -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| ADR                |            401 | 3.03%        |
| Corporate Bond     |             56 | 0.42%        |
| ETF                |           5556 | 41.98%       |
| ETN                |             45 | 0.34%        |
| ETV                |             90 | 0.68%        |
| Equity             |           5262 | 39.76%       |
| Fund               |            337 | 2.55%        |
| Preferred Stock    |            436 | 3.29%        |
| Right              |            125 | 0.94%        |
| Structured Product |            160 | 1.21%        |
| Unit               |            314 | 2.37%        |
| Unknown            |             12 | 0.09%        |
| Warrant            |            440 | 3.32%        |
| Total              |          13234 | 100%         |


Consists of 1 Databases

* `US_SHORT_INT`  - Tick Data




## US_SHORT_INT

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* SHORT_INT - Short Interest Statistics every 2 weeks
* TRD - Trades
* STAT - Static data, e.g. ISIN, description, security type


