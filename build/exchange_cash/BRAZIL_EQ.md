# B3 (Bovespa) - Equities + Equity Options

B3’s Bovespa equities segment is Brazil’s main stock exchange for trading stocks and equity options.

* Country: Brazil [BR]
* Mkt Hours: 08:00-17:00
* Time Zone: America/Sao_Paulo
* Start Date: 20080506 - Equities, 20140120 - Indices
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for BRAZIL_EQ`
* `Field Enumerations for BRAZIL_EQ`
* `Trading Hours for BRAZIL_EQ`
* `Recent Holidays for BRAZIL_EQ`



Includes the following coverage:

#### BRAZIL_EQ -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Corporate Bond     |             20 | 0.02%        |
| Depository Receipt |           1146 | 1.0%         |
| ETF                |            238 | 0.21%        |
| Equity             |           4372 | 3.81%        |
| Forward            |            848 | 0.74%        |
| Index              |            132 | 0.12%        |
| Option             |         107528 | 93.75%       |
| Preferred Stock    |            240 | 0.21%        |
| Right              |              3 | 0.0%         |
| Test               |             62 | 0.05%        |
| Unit               |             41 | 0.04%        |
| Unknown            |             12 | 0.01%        |
| Warrant            |             50 | 0.04%        |
| Total              |         114692 | 100%         |


Consists of 2 Databases

* `BRAZIL_EQ`  - Tick Data
* `BRAZIL_EQ_BARS`  - 1 Minute Bars




## BRAZIL_EQ

Database includes the following tick types:

* IDX - Index values
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades
* TRD_ODD_LOT - Trades from the odd lot book





## BRAZIL_EQ_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars


