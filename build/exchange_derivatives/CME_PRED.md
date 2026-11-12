# CME Event Contracts / Prediction Markets

Event contracts (prediction markets) from CME Group, with Trades, Quotes book depth and history from May 2026. Each contract asks a yes/no question about an economic or market outcome, such as where an equity index, interest rate or commodity price will settle, and is priced between $0.01 and $0.99, paying $1 if correct. Prices can be read as the market’s implied probability of each outcome.

* Country: USA United States [US]
* Mkt Hours: 00:00-24:00
* Time Zone: America/Chicago
* Start Date: 20260501
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes
* Timestamp Type: Exchange (Matching Engine)
* Key Indices:



Details are provided below

* `Table Schemas for CME_PRED`
* `Field Enumerations for CME_PRED`
* `Trading Hours for CME_PRED`
* `Recent Holidays for CME_PRED`



Includes the following coverage:

#### CME_PRED -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |           1103 | 2.37%        |
| Futures Spread  |            177 | 0.38%        |
| Option          |          45297 | 97.25%       |
| Total           |          46577 | 100%         |


Consists of 2 Databases

* `CME_PRED`  - Tick Data
* `CME_PRED_DAILY`  - End of Day Metrics




## CME_PRED

Database includes the following tick types:

* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* QTE - Best bid / offer quotes
* TRD - Trades





## CME_PRED_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


