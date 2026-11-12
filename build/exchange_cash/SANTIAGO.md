# Santiago Stock Exchange

Trades, quotes and bars from the Santiago Stock Exchange (Bolsa de Comercio de Santiago), Chile’s main exchange, with equities from November 2008 and indices from August 2021. Index data includes the IPSA, Chile’s main equity benchmark, which has been calculated by MSCI as the MSCI IPSA since September 2026 after being run by S&P Dow Jones Indices. The exchange is now part of the nuam regional exchange group with the Lima and Colombia exchanges.

* Country: Chile [CL]
* Mkt Hours: 08:00-17:00
* Time Zone: America/Santiago
* Start Date: 20081110 - Equities, 20210803 - Indices
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: IPSA [SANTIAGO::MXIPSAPC]



Details are provided below

* `Table Schemas for SANTIAGO`
* `Field Enumerations for SANTIAGO`
* `Trading Hours for SANTIAGO`
* `Recent Holidays for SANTIAGO`



Includes the following coverage:

#### SANTIAGO -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| ETF             |           1734 | 10.13%       |
| Equity          |          15273 | 89.23%       |
| Index           |             15 | 0.09%        |
| Mutual Fund     |             88 | 0.51%        |
| Unknown         |              6 | 0.04%        |
| Total           |          17116 | 100%         |


Consists of 3 Databases

* `SANTIAGO`  - Tick Data
* `SANTIAGO_BARS`  - 1 Minute Bars
* `SANTIAGO_DAILY`  - End of Day Metrics




## SANTIAGO

Database includes the following tick types:

* IDX - Index values
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## SANTIAGO_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## SANTIAGO_DAILY

Database includes the following tick types:

* STAT - Static data, e.g. ISIN, description, security type


