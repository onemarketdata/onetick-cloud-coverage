# Indonesia Stock Exchange Enumerations

The Indonesia Stock Exchange (IDX) offers trading in equities, bonds, ETFs, and derivatives issued by Indonesian companies.

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
|                4 | Special terms book        |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description                       |
|------------------|-----------------------------------------------|
|                0 | Closed / Pre-Trading                          |
|                1 | Opening Auction Match                         |
|                2 | Continuous Trading (Session I)                |
|                3 | Intermission (Lunch Break)                    |
|                4 | Continuous Trading (Session II)               |
|                5 | Closing Auction Match                         |
|                6 | End of Day (EOD) / Post-Trading               |
|                7 | Post-Close (or After-Hours / Trading at Last) |
|                8 | Pre-Open (or Pre-Opening)                     |
|                9 | Pre-Closing                                   |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| C                | Closing auction           |
| O                | Opening auction           |
| T                | Trading at closing price  |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description           |
|------------------|-----------------------------------|
| ‘””’             | Regular trade                     |
| 0                | Regular trade                     |
| 0-TN             | Regular trade (Cash market)       |
| 1                | Unintentional cross               |
| 1-TN             | Unintentional cross (Cash market) |
| 2                | Auction trade                     |
| NG               | Negotiated trade                  |
| TN               | Cash trade                        |

