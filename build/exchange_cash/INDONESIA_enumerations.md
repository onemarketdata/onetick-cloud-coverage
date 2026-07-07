# Indonesia Stock Exchange Enumerations

The Indonesia Stock Exchange (IDX) offers trading in equities, bonds, ETFs, and derivatives issued by Indonesian companies.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |
|                4 | Special terms book        |

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

