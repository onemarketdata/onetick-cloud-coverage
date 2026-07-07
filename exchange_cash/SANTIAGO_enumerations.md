# Santiago Stock Exchange Enumerations

The Santiago Stock Exchange (BCS) offers trading in equities, bonds, derivatives, and other financial instruments issued by Chilean companies.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* STAT_INCLUSION_FLAG - “Y” - Trade counts towards price stats, “N” - Trade should be excluded from price stats
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description       |
|------------------|-------------------------------|
|                0 | Lit order book                |
|                1 | Off-book [until 20210615]     |
|                6 | Auction book [until 20210615] |

#### STAT_INCLUSION_FLAG - Enumeration

| Enumeration ID   | Enumeration Description                 |
|------------------|-----------------------------------------|
| N                | Trade is excluded from price statistics |
| Y                | Trade is included in price statistics   |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description                       |
|------------------|-----------------------------------------------|
| -                | Regular trading                               |
| A                | Other auction                                 |
| C                | Closing auction                               |
| I                | Intraday auction                              |
