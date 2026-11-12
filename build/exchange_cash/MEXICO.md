# Mexico Stock Exchange (BMV)

Trades, quotes and bars from the Bolsa Mexicana de Valores (BMV), Mexico’s largest stock exchange, with history from January 2014. It covers Mexican stocks, FIBRAs and the SIC (Sistema Internacional de Cotizaciones), where foreign securities trade in Mexico. Covered stocks include constituents of the S&P/BMV IPC; for trading on both BMV and BIVA, use MX_COMP.

* Country: Mexico [MX]
* Mkt Hours: 08:00-17:00
* Time Zone: America/Mexico_City
* Start Date: 20140102
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: BMV



Details are provided below

* `Table Schemas for MEXICO`
* `Field Enumerations for MEXICO`
* `Trading Hours for MEXICO`
* `Recent Holidays for MEXICO`



Includes the following coverage:

#### MEXICO -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| ETF             |           1699 | 17.25%       |
| Equity          |           2699 | 27.4%        |
| Mutual Fund     |           4095 | 41.58%       |
| Unknown         |             34 | 0.35%        |
| Warrant         |           1322 | 13.42%       |
| Total           |           9849 | 100%         |


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


