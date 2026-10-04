# Abu Dhabi Securities Exchange Enumerations

The Abu Dhabi Securities Exchange (ADX) facilitates trading in equities, bonds, ETFs, and other securities issued by UAE companies.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| C                | Closing auction           |
| O                | Opening auction           |
| T                | Trading at closing price  |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Regular trade             |
| 1                | Regular trade             |
| 2                | Block trade               |
| 3                | Auction trade             |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                8 | Pre-Close                 |
|               14 | Trade-At-Last / TAL       |
|               12 | Closed                    |
|                5 | Open / Ongoing Trading    |

