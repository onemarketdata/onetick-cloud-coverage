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
| ADR                |            403 | 3.03%        |
| Corporate Bond     |             57 | 0.43%        |
| ETF                |           5662 | 42.51%       |
| ETN                |             45 | 0.34%        |
| ETV                |             90 | 0.68%        |
| Equity             |           5267 | 39.54%       |
| Fund               |            335 | 2.52%        |
| Preferred Stock    |            430 | 3.23%        |
| Right              |            121 | 0.91%        |
| Structured Product |            155 | 1.16%        |
| Unit               |            310 | 2.33%        |
| Unknown            |             13 | 0.1%         |
| Warrant            |            432 | 3.24%        |
| Total              |          13320 | 100%         |


Consists of 1 Databases

* `US_SHORT_INT`  - Tick Data




## US_SHORT_INT

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* SHORT_INT - Short Interest Statistics every 2 weeks
* TRD - Trades
* STAT - Static data, e.g. ISIN, description, security type


