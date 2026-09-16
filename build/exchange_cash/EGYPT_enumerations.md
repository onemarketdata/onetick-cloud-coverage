# Egyptian Exchange Enumerations

The Egyptian Exchange facilitates trading in equities, bonds, securitized mortgage and asset-backed securities of Egyptian companies.

The following fields have Enumerations:

* TRADE_TYPE - Type of trade
* TRADE_PERIOD - Market period during which a trade was executed.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                1 | Regular trade             |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Closing auction           |
| O                | Opening auction           |
| T                | Trading at last price     |
| -                | Regular trading           |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                1 | Pre-open                  |
|                2 | Pre-opening adjustment    |
|                3 | Trading                   |
|                4 | Adjustment                |
|                5 | Unavailable               |
|                7 | End of day                |
|                8 | Pre-close                 |
|                9 | Pre-closing adjustment    |
|               10 | Trading at closing price  |

