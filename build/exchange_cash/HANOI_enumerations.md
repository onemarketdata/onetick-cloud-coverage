# Hanoi Stock Exchange Enumerations

The Hanoi Stock Exchange (HNX) is Vietnam’s second securities trading center after HOSE. It handles trading of stocks, bonds and derivatives. Recently, it had 345 listed companies.[4][5]

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

|   Enumeration ID | Enumeration Description                |
|------------------|----------------------------------------|
|                0 | Pre-Open / Day Start                   |
|                1 | Periodic Opening Session               |
|                4 | Continuous Trading Session (Morning)   |
|               12 | Intermission (Lunch Break)             |
|               14 | Continuous Trading Session (Afternoon) |
|               16 | Periodic Closing Session (ATC)         |
|               18 | PLO After-Hours Trading Session        |
|               97 | Market Closed                          |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| A                | Auction                   |
| C                | Closing auction           |
| T                | Trading at closing price  |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Regular trade             |
|                1 | Put-through trade         |
|                3 | Auction trade             |

