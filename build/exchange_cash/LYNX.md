# Lynx ATS

Lynx is an alternative trading system (ATS) or dark pool operated by Cboe Global Markets in Canada.

* Country: Canada [CA]
* Mkt Hours: 09:00-16:00
* Time Zone: America/Toronto
* Start Date: 20170529
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for LYNX`
* `Field Enumerations for LYNX`
* `Trading Hours for LYNX`
* `Recent Holidays for LYNX`



Includes the following coverage:

#### LYNX -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Debenture          |             61 | 1.01%        |
| Depositary Receipt |            205 | 3.4%         |
| ETF                |           2101 | 34.85%       |
| Equity             |           3295 | 54.65%       |
| Preferred Stock    |            289 | 4.79%        |
| Right              |              4 | 0.07%        |
| Unknown            |              3 | 0.05%        |
| Warrant            |             71 | 1.18%        |
| Total              |           6029 | 100%         |


Consists of 2 Databases

* `LYNX`  - Tick Data
* `LYNX_DAILY`  - End of Day Metrics




## LYNX

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## LYNX_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


