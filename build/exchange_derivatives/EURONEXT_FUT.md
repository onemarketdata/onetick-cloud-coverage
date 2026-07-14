# Euronext Equity + Index Derivatives

Euronext Equity + Index Derivatives offers trading in futures and options on European equities and indices.

* Country: France Netherlands Belgium Portugal Norway [FR NL BE PT NO]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Paris
* Start Date: 20110104 - Futures, 20230320 - Options
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for EURONEXT_FUT`
* `Field Enumerations for EURONEXT_FUT`
* `Trading Hours for EURONEXT_FUT`
* `Recent Holidays for EURONEXT_FUT`



Includes the following coverage:

#### EURONEXT_FUT -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |           7112 | 4.25%        |
| Futures Spread  |             52 | 0.03%        |
| Option          |         160048 | 95.72%       |
| Total           |         167212 | 100%         |


Consists of 2 Databases

* `EURONEXT_FUT`  - Tick Data
* `EURONEXT_FUT_BARS`  - 1 Minute Bars




## EURONEXT_FUT

Database includes the following tick types:

* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## EURONEXT_FUT_BARS

Database includes the following tick types:

* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars


