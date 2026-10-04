# Kuwait Stock Exchange (Boursa Kuwait) Enumerations

Boursa Kuwait is the official stock exchange of Kuwait where Kuwaiti companies’ shares, bonds, investment funds and Islamic financial instruments are traded.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                5 | Buy-in                    |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description          |
|------------------|----------------------------------|
|                1 | Enquiry (Pre-Market)             |
|                2 | Opening Auction (Pre-Open)       |
|                4 | Trading Halt                     |
|                5 | Circuit Breaker                  |
|               12 | Continuous Trading               |
|               18 | Closing Auction                  |
|               20 | Trade at Last                    |
|               21 | Close of Trading                 |
|               25 | End of Day (System Finalisation) |
|               99 | Close of Day / Market Offline    |

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

