# European Consolidated Equities

This is a consolidated feed providing trade data and best bid/offer across European equity markets, giving a unified view of the European equity landscape.

* Country: Austria Belgium Switzerland Czechia Germany Denmark Spain Finland France UK United Kindom Greece Hungary Ireland Iceland Italy Luxembourg Netherlands Norway Poland Portugal Sweden [AT BE CH CZ DE DK ES FI FR GB GR HU IE IS IT LU NL NO PL PT SE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Paris
* Start Date: 20150101
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for EU_COMP`
* `Field Enumerations for EU_COMP`
* `Trading Hours for EU_COMP`
* `Recent Holidays for EU_COMP`



Includes the following coverage:

#### EU_COMP -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Bond               |            119 | 0.4%         |
| Corporate Bond     |              4 | 0.01%        |
| Depository Receipt |            175 | 0.58%        |
| ETC                |            262 | 0.87%        |
| ETF                |           4577 | 15.23%       |
| ETN                |            414 | 1.38%        |
| Equity             |          18505 | 61.58%       |
| Fund               |           4685 | 15.59%       |
| Investment Fund    |           1277 | 4.25%        |
| Preferred Stock    |             18 | 0.06%        |
| Right              |             13 | 0.04%        |
| Unknown            |              1 | 0.0%         |
| Warrant            |              1 | 0.0%         |
| Total              |          30051 | 100%         |


Consists of 3 Databases

* `EU_COMP`  - Tick Data
* `EU_COMP_BARS`  - 1 Minute Bars
* `EU_COMP_DAILY`  - End of Day Metrics




## EU_COMP

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* NBBO - National Best Bid / Offer quotes
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## EU_COMP_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## EU_COMP_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


