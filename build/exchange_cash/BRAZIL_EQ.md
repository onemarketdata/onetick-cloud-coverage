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
| Corporate Bond     |             25 | 0.02%        |
| Depository Receipt |           1134 | 0.73%        |
| ETF                |            214 | 0.14%        |
| Equity             |           4212 | 2.73%        |
| Forward            |            677 | 0.44%        |
| Index              |            119 | 0.08%        |
| Option             |         147497 | 95.6%        |
| Preferred Stock    |            239 | 0.15%        |
| Right              |              7 | 0.0%         |
| Test               |             62 | 0.04%        |
| Unit               |             41 | 0.03%        |
| Unknown            |             10 | 0.01%        |
| Warrant            |             56 | 0.04%        |
| Total              |         154293 | 100%         |


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


