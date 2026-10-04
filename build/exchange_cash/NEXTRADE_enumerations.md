# Nextrade ATS Enumerations

Nextrade (NXT) is South Korea’s first licensed Alternative Trading System (ATS), operating alongside the traditional Korea Exchange.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* TRADE_TYPE - Type of trade
* TRADE_PERIOD - Market period during which a trade was executed.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                          |
|------------------|--------------------------------------------------|
| ‘””’             | Undefined (e.g. auction trades, off-book trades) |
| B                | Buy                                              |
| S                | Sell                                             |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Regular trade             |
| BLK              | Block trade               |
| BKT              | Basket trade              |
| CL               | Trade at closing price    |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description              |
|------------------|--------------------------------------|
| E                | Extended hours (early session)       |
| L                | Extended hours (late session)        |
| T                | Trading at last price                |
| U                | Unscheduled auction                  |
| o                | Opening auction (extended hours)     |
| u                | Unscheduled auction (extended hours) |
| -                | Regular trading                      |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |

