# European Consolidated Equities Sample

A sample of the EU_COMP consolidated tape database covering a subset of symbols across more than 150 European exchange, MTF and trade reporting segments in 21 countries, between January 2, 2024 and March 31, 2024. It includes trades, NBBO, quotes and bars, giving a cross-venue view of each European stock on primary markets, Cboe Europe, Aquis, Turquoise and APAs. The full database covers constituents of the EURO STOXX 50, STOXX Europe 600, FTSE 100, DAX and CAC 40.

* Country: Austria Belgium Switzerland Czechia Germany Denmark Spain Finland France UK United Kindom Greece Hungary Ireland Iceland Italy Luxembourg Netherlands Norway Poland Portugal Sweden [AT BE CH CZ DE DK ES FI FR GB GR HU IE IS IT LU NL NO PL PT SE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Paris
* Start Date: 20240102
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: STOXX 50 Index [TDI_IDX::VH], Euro STOXX 50 Index [TDI_IDX::XX]



Details are provided below

* `Table Schemas for EU_COMP_SAMPLE`
* `Field Enumerations for EU_COMP_SAMPLE`
* `Trading Hours for EU_COMP_SAMPLE`
* `Recent Holidays for EU_COMP_SAMPLE`



Includes the following coverage:

#### EU_COMP_SAMPLE -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
|                    |              1 | 0.0%         |
| Bond               |             20 | 0.08%        |
| Convertible Bond   |              1 | 0.0%         |
| Corporate Bond     |             24 | 0.09%        |
| Depository Receipt |            101 | 0.38%        |
| ETC                |            198 | 0.75%        |
| ETF                |           3531 | 13.32%       |
| ETN                |            142 | 0.54%        |
| Equity             |          16640 | 62.77%       |
| Fund               |           4774 | 18.01%       |
| Investment Fund    |           1048 | 3.95%        |
| Preferred Stock    |             20 | 0.08%        |
| Right              |              1 | 0.0%         |
| Structured Product |              1 | 0.0%         |
| Warrant            |              8 | 0.03%        |
| Total              |          26510 | 100%         |


Consists of 2 Databases

* `EU_COMP_SAMPLE`  - Tick Data
* `EU_COMP_SAMPLE_BARS`  - 1 Minute Bars




## EU_COMP_SAMPLE

Database includes the following tick types:

* QTE - Best bid / offer quotes
* TRD - Trades





## EU_COMP_SAMPLE_BARS

Database includes the following tick types:

* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars


