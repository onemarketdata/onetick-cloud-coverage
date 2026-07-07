# TSX Alpha Enumerations

TSX Alpha Exchange (Alpha) is a trading venue owned and operated by TMX Group (TMX) trading Toronto Stock Exchange (TSX) and TSX Venture Exchange (TSXV) listed securities.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* BYPASS - Identifies whether the trade resulted from a Bypass order
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* ODD_LOT - Indicates whether a trade was an odd lot
* ORDER_TYPE - Type of order.
* SPECIAL_TERMS - Indicates any non-standard settlement / execution terms associated with a trade
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade
* UPDATE_TYPE - Type of update

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                          |
|------------------|--------------------------------------------------|
| ‘””’             | Undefined (e.g. auction trades, off-book trades) |
| B                | Buy                                              |
| S                | Sell                                             |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |
|                3 | Odd lot book              |
|                4 | Special terms book        |

#### BYPASS - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Not a bypass trade        |
| Y                | Bypass trade              |

#### MKT_PHASE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| AS               | Halted                    |
| C                | Closed                    |
| F                | Extended hours close      |
| I                | Inhibited                 |
| IS               | Inhibited, halted         |
| N                | Extended hours CXLs       |
| O                | Opening                   |
| P                | Pre-open                  |
| S                | Open                      |

#### ODD_LOT - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Board lot                 |
| Y                | Odd lot                   |

#### ORDER_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| L                | Limit order               |
| M                | Market order              |

#### SPECIAL_TERMS - Enumeration

| Enumeration ID   | Enumeration Description                |
|------------------|----------------------------------------|
| ‘””’             | No special terms (standard settlement) |
| C                | Cash                                   |
| CT               | Cash today                             |
| DC               | Derivative-related contingent trade    |
| DD               | Delayed delivery                       |
| NN               | Non-net                                |
| NR               | Non-resident                           |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description       |
