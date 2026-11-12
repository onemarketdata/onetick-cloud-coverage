# Hong Kong Futures Exchange

Futures and spreads with Trades, Quotes and bars from the Hong Kong Futures Exchange (HKFE), part of HKEX, with history from November 2009. Key contracts include Hang Seng Index, Mini-Hang Seng Index, Hang Seng China Enterprises Index and Hang Seng TECH Index futures, and USD/CNH futures.

* Country: Hong Kong SAR China [HK]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Hong_Kong
* Start Date: 20091110
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices:



Details are provided below

* `Table Schemas for HKFE`
* `Field Enumerations for HKFE`
* `Trading Hours for HKFE`
* `Recent Holidays for HKFE`



Includes the following coverage:

#### HKFE -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |           1181 | 42.74%       |
| Futures Spread  |           1582 | 57.26%       |
| Total           |           2763 | 100%         |


Consists of 2 Databases

* `HKFE`  - Tick Data
* `HKFE_BARS`  - 1 Minute Bars




## HKFE

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type





## HKFE_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars


