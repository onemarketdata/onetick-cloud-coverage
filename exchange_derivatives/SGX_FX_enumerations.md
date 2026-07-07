# Singapore Exchange - FX Derivatives Enumerations

The Singapore Exchange ( SGX ) offers trading in foreign exchange derivatives

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* QUOTE_SESSION - Trading session from which the quote originates, e.g. “Day”, “Night”
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_SESSION - Trading session from which a trade originates, e.g. “Day”, “Night”
* TRADE_TYPE - Type of trade

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                                          |
|------------------|------------------------------------------------------------------|
| ‘””’             | Undefined (e.g. auction trades, implied trades, off-book trades) |
| B                | Buy                                                              |
| S                | Sell                                                             |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |

#### QUOTE_SESSION - Enumeration

| Enumeration ID   | Enumeration Description          |
|------------------|----------------------------------|
| T                | T session (current business day) |
| T+1              | T+1 session (next business day)  |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
