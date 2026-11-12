# European Energy Exchange (EEX)

Futures with Trades, Quotes and bars from the European Energy Exchange (EEX), the Leipzig-based exchange in Deutsche Börse Group, with history from August 2019. EEX is the main European venue for power futures, such as German, French and Italian baseload and peakload contracts, and also lists natural gas, EU emissions allowances and freight contracts.

* Country: Germany [DE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Berlin
* Start Date: 20190809
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices:



Details are provided below

* `Table Schemas for EEX`
* `Field Enumerations for EEX`
* `Trading Hours for EEX`
* `Recent Holidays for EEX`



Includes the following coverage:

#### EEX -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |           3898 | 7.1%         |
| Futures Spread  |           2549 | 4.65%        |
| Option          |          48422 | 88.25%       |
| Total           |          54869 | 100%         |


Consists of 3 Databases

* `EEX`  - Tick Data
* `EEX_BARS`  - 1 Minute Bars
* `EEX_DAILY`  - End of Day Metrics




## EEX

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* QTE - Best bid / offer quotes





## EEX_BARS

Database includes the following tick types:

* QTE_1M - 1-minute quote bars





## EEX_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


