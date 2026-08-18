# Nasdaq CX2 Enumerations

Nasdaq CX2 is Nasdaq’s alternative trading system (ATS) for trading NMS stocks using a price-time priority order book model.

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
| ‘””’             | Undefined (e.g. off-book trades, auction trades) |
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

| Enumeration ID   | Enumeration Description                  |
|------------------|------------------------------------------|
| C                | End of transmission                      |
| E                | End of system hours                      |
| H                | Halted                                   |
| M                | End of market hours                      |
| O                | Start of messages                        |
| Q                | Start of market hours                    |
| R                | Resume after market-wide circuit breaker |
| S                | Start of system hours                    |
| T                | Trading                                  |
| W                | Market-wide circuit breaker              |

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
| CT               | Cash today                             |
| DD               | Delayed delivery                       |
| ND               | Next day                               |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Regular trade             |
| B                | Basis cross               |
| C                | Contingent cross          |
| D                | Derivative-related cross  |
| H                | Hidden order execution    |
| I                | Internal cross            |
| N                | NAV cross                 |
| V                | VWAP cross                |
| X                | Intentional cross         |

#### UPDATE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| A                | Add                       |
| D                | Delete                    |
| F                | Fill                      |
| M                | Modify                    |
| P                | Partial fill              |

