# Cboe Canada (formerly Neo Exchange) Enumerations

Trades, Quotes and Book depth from Cboe Canada (formerly Neo Exchange), with history from October 2017, covering its lit book, its dark book and its speed-bumped book for natural investors, plus Cboe Canada-listed securities. NEO was acquired by Cboe Global Markets in 2022 and renamed Cboe Canada. Cboe Canada is also a listing venue, especially for ETFs and Canadian Depositary Receipts (CDRs) of large US companies.   A consolidated tape for all Canadian equity markets is provided in the CA_COMP dataset.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* AUCTION_TYPE - Type of auction from which an indicative auction price / auction imbalance originates.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* BYPASS - Identifies whether the trade resulted from a Bypass order
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* ODD_LOT - Indicates whether a trade was an odd lot
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* ORDER_TYPE - Type of order.
* REASON_CODE - Reason for an instrument status update
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

#### AUCTION_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                 |
|------------------|-----------------------------------------|
| A                | Unspecified auction                     |
| C                | Closing auction                         |
| I                | Intraday auction                        |
| O                | Opening auction                         |
| P                | IPO / Public offering auction           |
| S                | Settlement (EDSP) auction               |
| U                | Unscheduled auction                     |
| c                | Post-close auction                      |
| o                | Opening auction (extended hours)        |
| p                | Auction initiated by market participant |
| u                | Unscheduled auction (extended hours)    |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |
|                2 | Dark book                 |
|                3 | Odd lot book              |
|                4 | Special terms book        |

#### BYPASS - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Not a bypass trade        |
| Y                | Bypass trade              |

#### MKT_PHASE - Enumeration

| Enumeration ID   | Enumeration Description                                |
|------------------|--------------------------------------------------------|
| 2                | Suspended [until 20250228]                             |
| 9                | MOC imbalance [until 20250228]                         |
| A                | Opening auction call                                   |
| a                | Pre-open [until 20250228]                              |
| b                | Closed [until 20250228]                                |
| c                | End of day [until 20250228]                            |
| d                | Closing auction call [until 20250228]                  |
| e                | No matching halt - auction [until 20250228]            |
| F                | Full halt [no order entry or modification]             |
| H                | Halted                                                 |
| J                | Halted (matching partition suspended) [until 20250228] |
| K                | Halted (system suspended) [until 20250228]             |
| l                | No matching halt [until 20250228]                      |
| M                | Delayed close                                          |
| O                | Pre-close                                              |
| o                | Pre-open [until 20250228]                              |
| P                | Post-close                                             |
| r                | Pre-close [until 20250228]                             |
| S                | Suspended                                              |
| T                | Regular trading                                        |
| u                | Extended trading [until 20250228]                      |
| X                | Extended hours                                         |
| y                | Pre-trading [until 20250228]                           |

#### ODD_LOT - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Board lot                 |
| Y                | Odd lot                   |

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

#### ORDER_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| L                | Limit order               |
| M                | Market order              |

#### REASON_CODE - Enumeration

| Enumeration ID   | Enumeration Description                                    |
|------------------|------------------------------------------------------------|
| 0                | Scheduled transition [until 20250228]                      |
| 1                | Extended By Market Ops [until 20250228]                    |
| 2                | Shortened By Market Ops [until 20250228]                   |
| 3                | Market order imbalance [until 20250228]                    |
| 4                | Price outside executable range [until 20250228]            |
| 5                | Circuit breaker [until 20250228]                           |
| 50               | Single Stock Circuit Breaker (SSCB) [until 20250228]       |
| 51               | SSCB Extended [until 20250228]                             |
| 52               | Market maker delayed opening / re-opening [until 20250228] |
| 53               | Auction execution [until 20250228]                         |
| 9                | Unspecified [until 20250228]                               |
| C                | Closing offset phase (Closing auction book)                |
| D                | Delayed opening                                            |
| I                | Imbalance phase (Closing auction book)                     |
| O                | Opening rescheduled                                        |
| R                | Re-opening rescheduled                                     |
| ‘””’             | No reason / unspecified                                    |

#### SPECIAL_TERMS - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Standard settlement       |
| Y                | Special settlement terms  |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| A                | Auction                   |
| C                | Closing auction           |
| O                | Opening auction           |
| T                | Trading at closing price  |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                |
|------------------|----------------------------------------|
| 0                | Regular trade                          |
| 11               | Basis cross                            |
| 12               | Contingent cross                       |
| 14               | VWAP cross                             |
| 15               | Regular cross                          |
| 16               | Bypass cross [until 20250228]          |
| 18               | Derivative cross                       |
| 5                | Internal cross                         |
| 20               | NAV cross                              |
| H                | Regular Trade against hidden liquidity |

#### UPDATE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| A                | Add                       |
| D                | Delete                    |
| M                | Modify                    |
| F                | Fill                      |
| P                | Partial fill              |

