# Colombia Stock Exchange Enumerations

The Colombia Stock Exchange (BVC) offers trading in equities, bonds, derivatives, and other financial instruments issued by Colombian companies.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description               |
|------------------|---------------------------------------|
|                3 | Open Market (Mercado Abierto)         |
|                6 | Pre-Open / Pre-Trading (Pre-Apertura) |
|                7 | Opening Auction (Subasta de Apertura) |
|                8 | Closing Auction (Subasta de Cierre)   |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| C                | Closing auction           |
| I                | Intraday auction          |
| O                | Opening auction           |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Normal trade              |
|                1 | Small trade               |

