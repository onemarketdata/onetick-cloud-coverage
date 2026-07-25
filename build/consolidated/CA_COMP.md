# Canadian Consolidated Equities (all Trades, Quotes, NBBO)

Consolidated data from all Canadian equities exchanges, covering Trades, Quotes and NBBO.

* Country: Canada [CA]
* Mkt Hours: 09:00-16:00
* Time Zone: America/Toronto
* Start Date: 20170529
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for CA_COMP`
* `Field Enumerations for CA_COMP`
* `Trading Hours for CA_COMP`
* `Recent Holidays for CA_COMP`



Includes the following coverage:

#### CA_COMP -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Debenture          |             59 | 1.02%        |
| Depositary Receipt |            205 | 3.56%        |
| ETF                |           2042 | 35.43%       |
| ETN                |              1 | 0.02%        |
| Equity             |           2992 | 51.91%       |
| Investment Fund    |             31 | 0.54%        |
| Preferred Stock    |            286 | 4.96%        |
| REIT               |             41 | 0.71%        |
| Right              |              3 | 0.05%        |
| Test               |             39 | 0.68%        |
| Unknown            |              3 | 0.05%        |
| Warrant            |             62 | 1.08%        |
| Total              |           5764 | 100%         |


Consists of 3 Databases

* `CA_COMP`  - Tick Data
* `CA_COMP_BARS`  - 1 Minute Bars
* `CA_COMP_DAILY`  - End of Day Metrics




## CA_COMP

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* NBBO - National Best Bid / Offer quotes
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## CA_COMP_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## CA_COMP_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


