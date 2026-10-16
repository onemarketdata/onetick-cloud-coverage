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
| Debenture          |             64 | 0.99%        |
| Depositary Receipt |            205 | 3.17%        |
| ETF                |           2151 | 33.21%       |
| ETN                |              1 | 0.02%        |
| Equity             |           3388 | 52.31%       |
| Fund               |            198 | 3.06%        |
| Preferred Stock    |            289 | 4.46%        |
| REIT               |             41 | 0.63%        |
| Right              |              6 | 0.09%        |
| Test               |             48 | 0.74%        |
| Unknown            |              3 | 0.05%        |
| Warrant            |             83 | 1.28%        |
| Total              |           6477 | 100%         |


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


