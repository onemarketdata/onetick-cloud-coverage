# Korea Exchange - Derivatives

Futures and spreads with Trades, Quotes and bars from the Korea Exchange derivatives market, with KOSPI derivatives from October 2013 and other contracts from April 2017. KOSPI 200 futures are among Asia’s most actively traded index futures, and the market also lists KOSDAQ 150 futures, Korean Treasury bond futures and USD/KRW futures.

* Country: Korea [KR]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Seoul
* Start Date: 20131022 - KOSPI, 20170424 - Everything else
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices:



Details are provided below

* `Table Schemas for KOREA_FUT`
* `Field Enumerations for KOREA_FUT`
* `Trading Hours for KOREA_FUT`
* `Recent Holidays for KOREA_FUT`



Includes the following coverage:

#### KOREA_FUT -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |           2147 | 57.67%       |
| Futures Spread  |           1576 | 42.33%       |
| Total           |           3723 | 100%         |


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


