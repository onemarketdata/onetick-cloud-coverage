# Bursa Malaysia - Derivatives Enumerations

Futures and spreads with Trades, Quotes and bars from Bursa Malaysia Derivatives, with history from December 2009. Its crude palm oil futures (FCPO) are the global price benchmark for palm oil, and it also lists FTSE Bursa Malaysia KLCI index futures (FKLI) and interest rate futures.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| A                | Auction                   |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description             |
|------------------|-------------------------------------|
| 0                | Regular trade                       |
| 4                | Strategy leg trade [until 20150810] |
| LEG              | Strategy leg trade                  |

