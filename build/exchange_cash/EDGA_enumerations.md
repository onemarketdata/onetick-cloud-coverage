# Cboe EDGA Enumerations

Trades, Quotes and Book depth from Cboe EDGA, a U.S. equities exchange operated by Cboe Global Markets, with history from May 2025. In November 2024 EDGA switched from an inverted venue to a maker-taker venue with a high-rebate, tier-free pricing model, and Cboe positions it as a thinner book offering faster fills and shorter queues. Full L1 history for Cboe EDGA from the Consolidated Tape is available in the US_COMP dataset.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* TRADE_TYPE - Type of trade
* TRADE_TYPE_EXT - Extended trade type code
* ODD_LOT - Indicates whether a trade was an odd lot
* TRADE_PERIOD - Market period during which a trade was executed.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* RPI - Indicates the presence of Retail Price Improvement interest on bid and/or ask side
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
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
| H                | Halted                      |
| Q                | Quote only                  |
| S                | Closed                      |
| T                | Trading                     |

#### OMD_STATUS - Enumeration

| Enumeration ID   | Enumeration Description       |
|------------------|-------------------------------|
| A                | Auction                       |
| B                | Break / Pause                 |
| C                | Closing auction               |
| D                | Delisted / Pending deletion   |
| H                | Halted                        |
| I                | Scheduled intraday auction    |
| M                | Mandatory quoting period      |
| N                | New instrument / Pre-listing  |
| O                | Opening auction               |
| P                | Pre-market                    |
| Q                | Indicative quoting period     |
| R                | Off-book trade reporting      |
| S                | Suspended                     |
| T                | Continuous trading            |
| U                | Unscheduled auction           |
| c                | Closed                        |
| i                | IPO / Public offering auction |
| n                | No market phase / Unspecified |
| o                | Order management              |
| p                | Post-market                   |
| t                | Trading at last price         |

#### UPDATE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| A                | Add                       |
| D                | Delete                    |
| F                | Fill                      |
| M                | Modify                    |
| P                | Partial fill              |

#### ORDER_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| L                | Limit order               |

