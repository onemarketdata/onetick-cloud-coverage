# Osaka Exchange - Commodity Derivatives (formerly TOCOM) Enumerations

The Osaka Exchange, formerly the Tokyo Commodity Exchange (TOCOM), offers trading in commodity futures and options, including metals, energy, and agricultural products.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_SESSION - Trading session from which a trade originates, e.g. “Day”, “Night”
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |

#### CALL_PUT_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call option               |
| P                | Put option                |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| A                | Auction                   |
| C                | Closing auction           |
| O                | Opening auction           |
