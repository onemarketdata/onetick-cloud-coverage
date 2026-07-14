# B3 - Derivatives (BM&F)

B3’s Bovespa equities segment is Brazil’s main Derivatives exchange for trading futures and equity options.

* Country: Brazil [BR]
* Mkt Hours: 10:00-18:15
* Time Zone: America/Sao_Paulo
* Start Date: 20091211
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for BRAZIL_FUT`
* `Field Enumerations for BRAZIL_FUT`
* `Trading Hours for BRAZIL_FUT`
* `Recent Holidays for BRAZIL_FUT`



Includes the following coverage:

#### BRAZIL_FUT -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Commodity       |              2 | 0.02%        |
| FRA             |             90 | 0.97%        |
| Forward         |              2 | 0.02%        |
| Future          |            643 | 6.91%        |
| Futures Spread  |            936 | 10.05%       |
| Option          |           7637 | 82.03%       |
| Total           |           9310 | 100%         |


Consists of 3 Databases

* `BRAZIL_FUT`  - Tick Data
* `BRAZIL_FUT_BARS`  - 1 Minute Bars
* `BRAZIL_FUT_DAILY`  - End of Day Metrics




## BRAZIL_FUT

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## BRAZIL_FUT_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## BRAZIL_FUT_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type
* TRD_1D - Daily trade bars


