# BIVA (Bolsa Institucional de Valores)

Trades and quotes from BIVA (Bolsa Institucional de Valores), Mexico’s second stock exchange, based in Mexico City, with history from June 2024. BIVA began operations in July 2018 as an alternative to the Bolsa Mexicana de Valores and trades the same Mexican-listed equities, as well as other instruments such as CKDs and FIBRAs. Its flagship benchmark is the FTSE BIVA index, calculated by FTSE Russell from the most liquid Mexican stocks.    A consolidated tape for both Mexican equity markets is provided in the MX_COMP dataset.

* Country: Mexico [MX]
* Mkt Hours: 08:30-15:11
* Time Zone: America/Mexico_City
* Start Date: 20240617
* Real Time Available: No
* Bars Available: No
* Book Depth Available: No
* Timestamp Type: Exchange (Matching Engine)
* Key Indices: BMV



Details are provided below

* `Table Schemas for BIVA`
* `Field Enumerations for BIVA`
* `Trading Hours for BIVA`
* `Recent Holidays for BIVA`



Includes the following coverage:

#### BIVA -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Bond            |              8 | 0.14%        |
| ETF             |             12 | 0.21%        |
| Equity          |           3980 | 69.22%       |
| Fund            |            393 | 6.83%        |
| REIT            |             35 | 0.61%        |
| Warrant         |           1322 | 22.99%       |
| Total           |           5750 | 100%         |


Consists of 2 Databases

* `BIVA`  - Tick Data
* `BIVA_DAILY`  - End of Day Metrics




## BIVA

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## BIVA_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


