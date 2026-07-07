# Nagoya Stock Exchange Enumerations

The Nagoya Stock Exchange (NSE) offers trading in equities, bonds, and other securities issued by Japanese companies.

The following fields have Enumerations:

* ASK_COND - Quote condition applicable to the best ask
* BID_COND - Quote condition applicable to the best bid
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_SESSION - Trading session from which a trade originates, e.g. “Day”, “Night”
* TRADE_TYPE - Type of trade

#### ASK_COND - Enumeration

|   Enumeration ID | Enumeration Description                                                                                                                   |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
|                0 | No bid                                                                                                                                    |
|                1 | Regular ask                                                                                                                               |
|                2 | Regular ask (buying up) [intermediate quote when an incoming order trades through multiple price points]                                  |
|                3 | Pre-open ask                                                                                                                              |
|                4 | Special ask [circuit breaker to prevent an excessive drop in price from one trade to the next - ask set to the lower limit]               |
|                5 | Sequential execution ask [circuit breaker caused by a large drop in price from a rapid string of executions - ask set to the lower limit] |

#### BID_COND - Enumeration

|   Enumeration ID | Enumeration Description                                                                                                                    |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
|                0 | No bid                                                                                                                                     |
|                1 | Regular bid                                                                                                                                |
|                2 | Regular bid (selling down) [intermediate quote when an incoming order trades through multiple price points]                                |
|                3 | Pre-open bid                                                                                                                               |
|                4 | Special bid [circuit breaker to prevent an excessive increase in price from one trade to the next - bid set to the upper limit]            |
|                5 | Sequential execution bid [circuit breaker caused by a large price increase from a rapid string of executions - bid set to the upper limit] |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |

#### TRADE_PERIOD - Enumeration

