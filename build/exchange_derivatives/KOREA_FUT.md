# Korea Exchange - Derivatives

The Korea Exchange (KRX) Derivatives Market offers trading in futures and options on equities, indices, interest rates, commodities, and currencies.

* Country: Korea [KR]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Seoul
* Start Date: 20131022 - KOSPI, 20170424 - Everything else
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for KOREA_FUT`
* `Field Enumerations for KOREA_FUT`
* `Trading Hours for KOREA_FUT`
* `Recent Holidays for KOREA_FUT`



Includes the following coverage:

#### KOREA_FUT -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |           2348 | 44.72%       |
| Futures Spread  |           2902 | 55.28%       |
| Total           |           5250 | 100%         |


Consists of 3 Databases

* `KOREA_FUT`  - Tick Data
* `KOREA_FUT_BARS`  - 1 Minute Bars
* `KOREA_FUT_DAILY`  - End of Day Metrics




## KOREA_FUT

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## KOREA_FUT_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## KOREA_FUT_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type
* TRD_1D - Daily trade bars


