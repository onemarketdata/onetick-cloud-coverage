# A3 Markets - Matba Rofex Enumerations

A3 Mercados is Argentina’s largest financial exchange platform, created from the merger of Matba Rofex and Mercado Abierto Electrónico (MAE).

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* TRADE_TYPE - Type of trade
* TRADE_PERIOD - Market period during which a trade was executed.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                          |
|------------------|--------------------------------------------------|
| ‘””’             | Undefined (e.g. auction trades, off-book trades) |
| B                | Buy                                              |
| S                | Sell                                             |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                                                                                      |
|------------------|------------------------------------------------------------------------------------------------------------------------------|
| ‘””’             | Regular trade                                                                                                                |
| BLK              | Block trade                                                                                                                  |
| LEG              | Strategy leg trade [Synthetic trade reported on each outright leg when two spread orders are matched - price is always null] |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |

#### MKT_PHASE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| 0                | Pre-trading               |
| 1                | Trading                   |
| 2                | Post-trading              |
| 3                | After hours               |
| 4                | Closed                    |
| 8                | Closing price crossing    |
| H                | Halted                    |

