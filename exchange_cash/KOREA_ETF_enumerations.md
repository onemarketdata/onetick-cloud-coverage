# Korea Exchange - ETFs and ETNs Enumerations

The Korea Exchange (KRX) offers trading in exchange-traded funds (ETFs) and exchange-traded notes (ETNs).

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |
|                2 | Dark book                 |

#### CALL_PUT_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call option               |
| P                | Put option                |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description       |
|------------------|-------------------------------|
| -                | Regular trading               |
| C                | Closing auction               |
| E                | Outside hours (Early session) |
| L                | Outside hours (Late session)  |
| O                | Opening auction               |
| T                | Trading at closing price      |
| U                | Unscheduled auction           |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description                               |
|------------------|-------------------------------------------------------|
|                1 | Regular trade                                         |
|               10 | Pre-opening basket trade                              |
|               11 | K-Blox block trade                                    |
|               12 | Basket trade                                          |
