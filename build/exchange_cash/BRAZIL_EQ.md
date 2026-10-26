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
| Depository Receipt |           1145 | 1.13%        |
| ETF                |            242 | 0.24%        |
| Equity             |           4379 | 4.34%        |
| Forward            |            851 | 0.84%        |
| Index              |            134 | 0.13%        |
| Option             |          93596 | 92.77%       |
| Preferred Stock    |            357 | 0.35%        |
| Right              |              4 | 0.0%         |
| Test               |             62 | 0.06%        |
| Unit               |             41 | 0.04%        |
| Unknown            |              5 | 0.0%         |
| Warrant            |             50 | 0.05%        |
| Total              |         100886 | 100%         |


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


