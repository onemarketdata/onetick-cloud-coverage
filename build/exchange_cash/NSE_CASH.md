# National Stock Exchange of India - Equities

The NSE is India’s largest stock exchange offering trading in Indian company stocks and equity products.

* Country: India [IN]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Kolkata
* Start Date: 20120102
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for NSE_CASH`
* `Field Enumerations for NSE_CASH`
* `Trading Hours for NSE_CASH`
* `Recent Holidays for NSE_CASH`



Includes the following coverage:

#### NSE_CASH -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Total           |           2180 | 100%         |


Consists of 2 Databases

* `NSE_CASH`  - Tick Data
* `NSE_CASH_BARS`  - 1 Minute Bars




## NSE_CASH

Database includes the following tick types:

* IDX - Index values
* PRL_ACTIVE - Shows all orders entered into the book, including aggressive orders that are matched immediately
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* PRL_INACTIVE - Shows dormant / inactive orders (e.g. unelected stop orders) that are parked outside the main order book
* QTE - Best bid / offer quotes
* TRD - Trades





## NSE_CASH_BARS

Database includes the following tick types:

* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars


