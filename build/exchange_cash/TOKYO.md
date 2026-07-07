# Tokyo Stock Exchange (+ Fukuoka / Sapporo)

The Tokyo Stock Exchange (TSE) offers trading in equities, bonds, ETFs, and derivatives. It also includes regional exchanges in Fukuoka and Sapporo.

* Country: Japan [JP]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Tokyo
* Start Date: 20081001
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for TOKYO`
* `Field Enumerations for TOKYO`
* `Trading Hours for TOKYO`
* `Recent Holidays for TOKYO`



Includes the following coverage:

#### TOKYO -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| ETF             |            470 | 10.11%       |
| Equity          |           4102 | 88.22%       |
| Preferred Stock |              9 | 0.19%        |
| REIT            |             64 | 1.38%        |
| Test            |              5 | 0.11%        |
| Total           |           4650 | 100%         |


Consists of 3 Databases

* `TOKYO`  - Tick Data
* `TOKYO_BARS`  - 1 Minute Bars
* `TOKYO_DAILY`  - End of Day Metrics




## TOKYO

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## TOKYO_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## TOKYO_DAILY

Database includes the following tick types:

* STAT - Static data, e.g. ISIN, description, security type


