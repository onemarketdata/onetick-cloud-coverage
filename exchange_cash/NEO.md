# Cboe Canada (formerly Neo Exchange)

Cboe Canada, formerly Neo Exchange, is an equities exchange in Canada operated by Cboe Global Markets.

* Country: Canada [CA]
* Mkt Hours: 09:00-16:00
* Time Zone: America/Toronto
* Start Date: 20171023
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for NEO`
* `Field Enumerations for NEO`
* `Trading Hours for NEO`
* `Recent Holidays for NEO`



Includes the following coverage:

#### NEO -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Debenture          |             65 | 1.02%        |
| Depositary Receipt |            205 | 3.21%        |
| ETF                |           2080 | 32.59%       |
| ETN                |              1 | 0.02%        |
| Equity             |           3353 | 52.54%       |
| Fund               |            203 | 3.18%        |
| Preferred Stock    |            293 | 4.59%        |
| REIT               |             43 | 0.67%        |
| Right              |              6 | 0.09%        |
| Test               |             43 | 0.67%        |
| Unknown            |              7 | 0.11%        |
| Warrant            |             83 | 1.3%         |
| Total              |           6382 | 100%         |


Consists of 2 Databases

* `NEO`  - Tick Data
* `NEO_DAILY`  - End of Day Metrics




## NEO

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_NEO_L - (Cboe Canada only) Full orderbook data for the Neo-L book
* PRL_NEO_N - (Cboe Canada only) Aggregated market depth for the Neo-N book
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## NEO_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


