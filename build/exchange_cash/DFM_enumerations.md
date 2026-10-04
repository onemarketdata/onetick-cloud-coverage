# Dubai Financial Market Enumerations

The Dubai Financial Market (DFM) offers trading in equities, bonds, ETFs, and derivatives of UAE and international companies.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description           |
|------------------|-----------------------------------|
|                1 | Pre-Trading / Enquiry             |
|                2 | Pre-Opening Session               |
|                5 | Post-Trading                      |
|               20 | Continuous Trading (Main Session) |
|               21 | Trading at Last (TAL)             |
|               36 | Pre-Closing Session               |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| C                | Closing auction           |
| O                | Opening auction           |
| T                | Trading at closing price  |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Regular trade             |
| 0                | Regular trade             |
| 1                | Direct trade              |

