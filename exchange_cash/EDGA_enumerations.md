# Cboe EDGA Enumerations

Cboe EDGA Exchange (EDGA) is a U.S. equities market that transitioned from an inverted to a tier-free, maker-taker pricing structure. It offers unique features like hidden price improvement, retail priority, and periodic auctions to optimize order execution

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* TRADE_TYPE - Type of trade
* TRADE_TYPE_EXT - Extended trade type code
* ODD_LOT - Indicates whether a trade was an odd lot
* TRADE_PERIOD - Market period during which a trade was executed.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* RPI - Indicates the presence of Retail Price Improvement interest on bid and/or ask side
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* UPDATE_TYPE - Type of update
* ORDER_TYPE - Type of order.

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                                          |
|------------------|------------------------------------------------------------------|
| ‘””’             | Undefined (e.g. auction trades, trades against hidden liquidity) |
| B                | Buy                                                              |
| S                | Sell                                                             |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                |
|------------------|----------------------------------------|
| ‘””’             | Regular trade                          |
| H                | Regular trade against hidden liquidity |
| R                | Routed trade                           |

#### TRADE_TYPE_EXT - Enumeration

| Enumeration ID   | Enumeration Description      |
|------------------|------------------------------|
| ‘””’             | Unspecified [for future use] |

#### ODD_LOT - Enumeration

| Enumeration ID   | Enumeration Description      |
|------------------|------------------------------|
| ‘””’             | Unspecified [for future use] |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description        |
|------------------|--------------------------------|
| -                | Regular trading                |
| E                | Extended hours (Early session) |
| L                | Extended hours (Late session)  |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                9 | Off-exchang               |

#### RPI - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | No retail interest        |

#### MKT_PHASE - Enumeration

| Enumeration ID   | Enumeration Description     |
|------------------|-----------------------------|
| A                | Accepting order for queuing |
