# Australian Stock Exchange Enumerations

The Australian Stock Exchange (ASX) offers trading in equities, bonds, ETFs, derivatives, and other securities issued by Australian companies.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_REPORT_TYPE - Additional detail on the source of an off-book (reported) trade
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |
|                2 | Dark book                 |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| C                | Closing auction           |
| O                | Opening auction           |
| T                | Trading at closing price  |
| U                | Unscheduled auction       |

#### TRADE_REPORT_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                      |
|------------------|----------------------------------------------|
| ‘””’             | Not applicable                               |
| 0                | Regular trade / not applicable               |
| 10               | Special crossing tier 1                      |
| 100              | NBBO cross                                   |
| 11               | Special crossing tier 2                      |
| 12               | Special crossing tier 3                      |
| 13               | Late trade report reason code a              |
| 14               | Late trade report reason code b              |
| 15               | Late trade report reason code c              |
| 16               | Late trade report reason code d              |
| 17               | Late trade report reason code e              |
| 2                | Cross                                        |
| 3                | Derivatives special cross                    |
| 30               | Equity/option combination                    |
| 31               | Tailor made combination                      |
| 32               | Tailor made combination crossing             |
| 33               | Late combination trade                       |
| 35               | OTC contingent equity trade                  |
| 4                | Late                                         |
| 40               | Buyback                                      |
| 41               | Booking purposes                             |
| 43               | Directed reporting                           |
| 44               | Option exercise (call)                       |
| 45               | Option exercise (put)                        |
| 46               | ETF special trade                            |
| 47               | Forward delivery                             |
| 5                | Overseas                                     |
| 50               | Loan                                         |
| 51               | Loan return                                  |
| 54               | Foreign to foreign                           |
| 58               | Price stabilisation                          |
| 59               | Price stabilisation late trade               |
| 60               | Portfolio special crossing                   |
| 61               | Price stabilisation late trade reason code a |
| 62               | Price stabilisation late trade reason code b |
| 63               | Price stabilisation late trade reason code c |
| 64               | Price stabilisation late trade reason code d |
| 65               | Price stabilisation late trade reason code e |
| 66               | Put-through special cross ($1M)              |
| 67               | Put-through special cross ($0.5M)            |
| 70               | Quote display board trade report             |
| 8                | Price stabilisation / green shoe order       |
| 9                | Special combo contingent                     |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                                                          |
|------------------|--------------------------------------------------------------------------------------------------|
| 0                | Regular trade                                                                                    |
| 1                | Trade report - Different participants [until 20250630]                                           |
| 10               | Internal trade + buy-write                                                                       |
