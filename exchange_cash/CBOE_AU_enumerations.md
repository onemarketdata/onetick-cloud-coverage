# Cboe Australia (CXA) Enumerations

Cboe Australia, formerly Chi-X Australia, is an alternative trading system providing trading in Australian equities, ETFs, and other listed securities.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |
|                2 | Dark book                 |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| T                | Trading at closing price  |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                   |
|------------------|-------------------------------------------|
| 0                | Regular trade                             |
| 112              | Portfolio trade (delayed)                 |
| 116              | Large principal trade (delayed)           |
