# Mexico Stock Exchange (BMV)

The Mexican Stock Exchange, commonly known as Mexican Bolsa, Mexbol, or BMV, is one of two stock exchanges in Mexico, the other being BIVA - Bolsa Institucional de Valores.

* Country: Mexico [MX]
* Mkt Hours: 08:00-17:00
* Time Zone: America/Mexico_City
* Start Date: 20140102
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for MEXICO`
* `Field Enumerations for MEXICO`
* `Trading Hours for MEXICO`
* `Recent Holidays for MEXICO`



Includes the following coverage:

#### MEXICO -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| ETF             |           1639 | 16.9%        |
| Equity          |           2675 | 27.59%       |
| Mutual Fund     |           4105 | 42.34%       |
| Unknown         |             29 | 0.3%         |
| Warrant         |           1248 | 12.87%       |
| Total           |           9696 | 100%         |


Consists of 2 Databases

* `MEXICO`  - Tick Data
* `MEXICO_BARS`  - 1 Minute Bars




## MEXICO

Database includes the following tick types:

* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## MEXICO_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars


