# New Zealand Exchange (NZX) Enumerations

Trades, quotes and bars from NZX, New Zealand’s stock exchange, with history from December 2014, covering the NZX Main Board, debt market and funds. Covered stocks include constituents of the S&P/NZX 50; index values are in NZX_IDX.

The following fields have Enumerations:

* AUCTION_TYPE - Type of auction from which an indicative auction price / auction imbalance originates.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

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

#### MKT_PHASE - Enumeration

| Enumeration ID   | Enumeration Description                                                                                         |
|------------------|-----------------------------------------------------------------------------------------------------------------|
| ADJUST           | Adjust (orders cannot be entered, existing orders can be cancelled or modified to a worse price / smaller size) |
| ENDOFDAY         | End of day                                                                                                      |
| ENQUIRY          | Enquiry (no orderbook access or trade reporting)                                                                |
| H                | Halted                                                                                                          |
| HALT             | Halted                                                                                                          |
| PRECLOSE         | Closing auction                                                                                                 |
| PREOPEN          | Opening auction                                                                                                 |
| S                | Suspended                                                                                                       |
| TRADING          | Continuous trading                                                                                              |

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

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| C                | Closing auction           |
| O                | Opening auction           |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Regular trade             |
| BT               | Block trade               |
| IN               | International trade       |
| LA               | Late trade                |
| LT               | Late reported             |
| MP               | Midpoint trade            |
| OL               | Odd lot                   |
| PF               | Portfolio crossing        |
| PT               | Put through               |
| SP               | Off market                |
| WA               | VWAP trade                |

