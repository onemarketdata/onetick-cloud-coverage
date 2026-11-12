# Shanghai Futures Exchange Enumerations

Futures and options with Trades, Quotes and bars from the Shanghai Futures Exchange (SHFE), one of China’s main futures exchanges, with history from October 2015. SHFE lists China’s benchmark contracts for copper, aluminium, zinc, nickel, gold, silver, steel rebar, natural rubber and fuel oil.

The following fields have Enumerations:

* CALL_PUT_IND - “C” - Call option, “P” - Put option
* TRADE_PERIOD - Market period during which a trade was executed.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* TRADE_SESSION - Trading session from which a trade originates, e.g. “Day”, “Night”
* QUOTE_SESSION - Trading session from which the quote originates, e.g. “Day”, “Night”

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Regular trade             |

#### CALL_PUT_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call option               |
| P                | Put option                |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Not applicable            |
| O                | Opening auction           |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |

#### TRADE_SESSION - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| Day              | Day session               |
| Night            | Night session             |

#### QUOTE_SESSION - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| Day              | Day session               |
| Night            | Night session             |

