# Nodal Exchange Enumerations

Futures, options and spreads with Trades, Quotes and book depth from Nodal Exchange, with history from August 2026. Nodal, part of EEX Group, is the leading North American power futures exchange, holding more than half of US power futures open interest. It also lists natural gas futures and one of the largest suites of environmental futures and options, including carbon contracts, all cleared through its subsidiary Nodal Clear.

The following fields have Enumerations:

* TRADE_TYPE - Type of trade
* TRADE_PERIOD - Market period during which a trade was executed.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Regular trade             |
| BLK              | Block trade               |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |

